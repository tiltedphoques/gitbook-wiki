# Build Docker server image

**This is an advanced guide. If you have not worked with `docker` before, it is best that you [follow the Docker setup guide](docker-setup.md) to pull the official docker image from the tiltedphoques repository on Docker Hub.**

This guide is primarily for those who want to build a dev branch of the server for use with Docker/Linux or for using `docker buildx` to build the server for different architectures/platforms. If you have not yet setup Docker, follow the [Installing Docker](docker-setup.md#installing-docker) instructions.

In order to follow these instructions, you will need to have an account on [Docker Hub](https://hub.docker.com) and you will need to be logged into that account using `docker login`. Instructions for such can be found [here](https://docs.docker.com/engine/reference/commandline/login/).

Below, we will be referring to your docker hub repository as `username/image_name` when we push images. Please note that anywhere you see `username` it needs to be your Docker Hub username.

## Gathering Requirements for Building Server Container

We only need `Dockerfile` and `Dockerfile.builder` in order to build the image. We have three options to retrieve these files, you only need to choose and follow the steps in one of them.

#### Option 1: Clone the TiltedEvolution Repository

This is the writer's preference, since it will always pull the latest Dockerfile and Dockerfile.builder, and it's simple. It does download the full repo, however, which includes files unecessary for this process.

1. Run the following command to clone the repository into ~/str:\
    `git clone https://github.com/tiltedphoques/TiltedEvolution.git ~/str`
    * We will not be building this project directly so we do not require the submodules/dependencies.
    * If you encounter an error about login status, install gh `sudo apt install gh` and login `gh auth login` to your github account.
2. Change directory ~/str:\
    `cd ~/str`

#### Option 2: Download just Dockerfile and Dockerfile.builder

This option does not download any unecessary files, though it is a few more commands and it links directly to the necessary files. If these file names change in the future, these links may break.

1. Make sure `curl` is installed:\
    `sudo apt update && sudo apt install curl`
2. Make a directory to hold the files and change to it:\
    `mkdir ~/str && cd ~/str`
3. Download `Dockerfile`:\
    `curl -fsSL https://raw.githubusercontent.com/tiltedphoques/TiltedEvolution/master/Dockerfile -o Dockerfile`
4. Download `Dockerfile.builder`:\
    `curl -fsSL https://raw.githubusercontent.com/tiltedphoques/TiltedEvolution/master/Dockerfile.builder -o Dockerfile.builder`

#### Option 3: Copy and Paste

1. Make a directory to hold the files and change to it:\
    `mkdir ~/str && cd ~/str`
2. Create the two files we need:\
    `touch Dockerfile Dockerfile.builder`
3. Open Dockerfile for editing:\
    `nano Dockerfile`
4. Copy the following contents into Dockerfile and save:
```
FROM username/multiarch-builder:latest as builder

ARG REPO=https://github.com/tiltedphoques/TiltedEvolution.git
ARG BRANCH=master

WORKDIR /home/builder

ENV XMAKE_ROOT=y

RUN git clone --recursive -b ${BRANCH} ${REPO} ./str && \
    cd str && xmake config -m release -y && xmake -y && xmake install -o package -y


# Building for x86_64
FROM builder as amd64builder

RUN cp /usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.30 /home/builder/libstdc++.so.6


# Building for arm64/v8
FROM builder as arm64builder

RUN cp /usr/lib/aarch64-linux-gnu/libstdc++.so.6.0.30 /home/builder/libstdc++.so.6


# Intermediate image that has the library specific to our $TARGETARCH
FROM ${TARGETARCH}builder as intermediate
# If a user has built without buildx, attempt to save them
RUN if [ "${TARGETARCH}" = "" ]; then export LIBFILE="/usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.30"; if [ ! -e ${LIBFILE} ]; then export LIBFILE=/usr/lib/aarch64-linux-gnu/libstdc++.so.6.0.30; fi ; cp ${LIBFILE} /home/builder/libstdc++.so.6; fi


# Build actual server image
FROM ubuntu:22.04

COPY --from=intermediate /home/builder/str/package/lib/libSTServer.so /home/server/libSTServer.so
COPY --from=intermediate /home/builder/str/package/bin/crashpad_handler /home/server/crashpad_handler
COPY --from=intermediate /home/builder/str/package/bin/SkyrimTogetherServer /home/server/SkyrimTogetherServer

COPY --from=intermediate /home/builder/libstdc++.so.6 /home/server/libstdc++.so.6

WORKDIR /home/server
ENTRYPOINT ["./SkyrimTogetherServer"]

EXPOSE 10578/udp
```
* Open Dockerfile.builder for editing:\
    `nano Dockerfile.builder`
* Copy the following contents into Dockerfile.builder and save:
```
FROM ubuntu:22.04

WORKDIR /home/builder

RUN apt update && apt install \
    cmake \
    unzip \
    git \
    gcc-12 \
    g++-12 \
    build-essential \
    ca-certificates \
    curl \
    --no-install-recommends -y && \
    git clone --recursive https://github.com/xmake-io/xmake.git ./xmake && \
    cd xmake && \
    make build && \
    make install && \
    cd .. && rm -rf xmake/ && \
    update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-12 110 --slave /usr/bin/g++ g++ /usr/bin/g++-12 --slave /usr/bin/gcov gcov /usr/bin/gcov-12 && \
    rm -rf /var/lib/apt/lists/*
```


## Building the Multiarch Builder with Buildx

This builder image is based off of Ubuntu 22.04 and installs the necessary requirements to build the server docker image later. This step is only required once, since any time you build the server image afterwards your multiarch-builder image can be pulled from Docker Hub.

1. First we are going to set up the multi-architecture builder with `docker buildx`:\
    `docker buildx create --name str-multiarch --use`
2. And verify that it is loaded:\
    `docker buildx inspect --bootstrap`
3. For some reason, buildx can occasionally have a bug where it won't build emulated architectures, but we can get around that with the command:\
    `docker run --rm --privileged multiarch/qemu-user-static --reset -p yes`
4. Now we will create the multi-architecture builder for both linux/amd64 and linux/arm64 architectures. This will create the builder image for use on PCs with AMD/Intel CPU and also for RaspberryPi/equivalent running x64 Linux:\
    `docker buildx build --platform linux/amd64,linux/arm64 -f Dockerfile.builder -t username/multiarch-builder:latest --push .`


## Building the Multiarch Server Container with Buildx

Everything above this header need only be done once. This step is where we actually build the server image, and should be done any time you wish to update your server image.

1. Since you're following these instructions, I assume you want to pull the multiarch-builder we just built from your Docker Hub repository. If that is the case, edit the first line of Dockerfile to read:\
    `FROM username/multiarch-builder:latest as builder`
2. Now we'll use our multiarch-builder to create the server docker container:\
    `docker buildx build --platform linux/amd64,linux/arm64 -f Dockerfile -t username/st-reborn-server:latest --push .`
    * If you want to build a specific repository/branch, you can pass `REPO` or `BRANCH` as a `--build-arg`, like so:
        `docker buildx build --build-arg BRANCH=master --build-arg REPO=http://github.com/tiltedphoques/TiltedEvolution.git --platform linux/amd64,linux/arm64 -f Dockerfile -t username/st-reborn-server:latest --push .`

This will create a manifest with two containers, one for linux/amd64 (Intel/AMD PCs) and one for linux/arm64 (RaspberryPi/equivalent), and push them to your docker hub. If you want to build only the server for your architecture, you can omit the other one. Alternatively, you could simply `docker build .` to build the server without buildx, but it will only build for your current architecture. As of writing, `docker build .` will only work with linux/amd64 and linux/aarch64 architectures.