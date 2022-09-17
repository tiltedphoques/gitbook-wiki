# Build Docker server image

**This is an advanced guide. If you have not worked with `docker` before, it is best that you [follow the Docker setup guide](../../guides/server-guide/linux-setup/docker-setup.md) to pull the official docker image from the tiltedphoques repository on Docker Hub.**

This guide is primarily for those who want to build a dev branch of the server for use with Docker/Linux or for using `docker buildx` to build the server for different architectures/platforms. If you have not yet setup Docker, follow the [Installing Docker](../../guides/server-guide/linux-setup/docker-setup.md#installing-docker) instructions.

In order to follow these instructions, you will need to have an account on [Docker Hub](https://hub.docker.com) and you will need to be logged into that account using `docker login`. Instructions for such can be found [here](https://docs.docker.com/engine/reference/commandline/login/).

Below, we will be referring to your docker hub repository as `username/image_name` when we push images. Please note that anywhere you see `username` it needs to be your Docker Hub username.

## Gathering Requirements for Building Server Container

We only require Dockerfile and Dockerfile.builder to build the image, but we are going to clone the full repository. It does include files unecessary for this process, but it makes sure everything is up to date. Once this is done once, you can pull updates with `git fetch && git pull`.

1. Run the following command to clone the repository into ~/str:\
    `git clone --recursive https://github.com/tiltedphoques/TiltedEvolution.git ~/str`
    * If you encounter an error about login status, install gh `sudo apt install gh` and login `gh auth login` to your github account.
2. Change directory ~/str:\
    `cd ~/str`


## Building the Multiarch Builder with Buildx

This builder image is based off of Ubuntu 22.04 and installs the necessary requirements to build the server docker image later. This step is only required once, since any time you build the server image afterwards your multiarch-builder image can be pulled from Docker Hub.

1. First we are going to set up the multi-architecture builder with `docker buildx`:\
    `docker buildx create --name str-multiarch --use`
2. And verify that it is loaded:\
    `docker buildx inspect --bootstrap`
3. For some reason, buildx can occasionally have a bug where it won't build emulated architectures, but we can get around that with the command:\
    `docker run --rm --privileged multiarch/qemu-user-static --reset -p yes`
    * Remember this command: if you have a build error in the future, try running this command and then attempt the build again. I have had it fix issues on more than one occasion.
4. Now we will create the multi-architecture builder for both linux/amd64 and linux/arm64 architectures. This will create the builder image for use on PCs with AMD/Intel CPU and also for RaspberryPi/equivalent running x64 Linux:\
    `docker buildx build --platform linux/amd64,linux/arm64 -f Dockerfile.builder -t username/multiarch-builder:latest --push .`


## Building the Multiarch Server Container with Buildx

Everything above this header need only be done once. This step is where we actually build the server image, and should be done any time you wish to update your server image.

1. Since you're following these instructions, I assume you want to pull the multiarch-builder we just built from your Docker Hub repository. If that is the case, edit the first line of Dockerfile to read:\
    `FROM username/multiarch-builder:latest as builder`
2. Now we'll use our multiarch-builder to create the server docker container:\
    `docker buildx build --platform linux/amd64,linux/arm64 -f Dockerfile -t username/st-reborn-server:latest --push .`
    * If you want to build a specific repository/branch, you can pass `REPO` or `BRANCH` as a `--build-arg`, like so:\
        `docker buildx build --build-arg BRANCH=master --build-arg REPO=http://github.com/tiltedphoques/TiltedEvolution.git --platform linux/amd64,linux/arm64 -f Dockerfile -t username/st-reborn-server:latest --push .`

This will create a manifest with two containers, one for linux/amd64 (Intel/AMD PCs) and one for linux/arm64 (RaspberryPi/equivalent), and push them to your docker hub. If you want to build only the server for your architecture, you can omit the other one. Alternatively, you could simply `docker build .` to build the server without buildx, but it will only build for your current architecture. As of writing, `docker build .` will only work with linux/amd64 and linux/aarch64 architectures.