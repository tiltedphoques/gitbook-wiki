# Docker setup

In this guide, we'll assume you're running Ubuntu 22.04 LTS. Because we won't be covering many distros, the guide will only use the most popular one.

## Installing Docker

1. Open your terminal
2. Do a `sudo apt update`
3. Then we must install the following prerequisites:\
   `sudo apt install -y apt-transport-https ca-certificates curl software-properties-common`
4. Then we need to add the GPG key from the official Docker repository to our system:\
   `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`
5. Then we will add the Docker repository to our APT sources:\
   `echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`
6. Do another `sudo apt update` to let the system update the packages, now including the Docker repository.
7. Let's install Docker and docker-compose:\
   `sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin`
8. After that's done, let's add the current user to the docker group, so we don't need to write `sudo` all the time while using docker:\
   `sudo usermod -aG docker ${USER}`
9. You will need to re-log your user, for this to take effect (open and close your terminal, if you're using a headless Ubuntu server)

## Creating paths for the Skyrim Together Reborn server

I like to put my stuff in `/opt/` so that's what we will do for now

1. Let's create the folders needed. We will need sudo privilige to create folders in `/opt/`.\
   `sudo mkdir -p /opt/docker/skyrimserver/{config,Data,logs}`
2. Now let us take ownership of the folders\
   `sudo chown -R ${USER}:${USER} /opt/docker`

## Starting the server using Docker

1. Docker is extremely simple to get up and running
2. We just need to run this command, and Docker will take care of the rest:\
   `docker run -d -it --name skyrimserver -p 10578:10578/udp -v /opt/docker/skyrimserver/config:/home/server/config -v /opt/docker/skyrimserver/Data:/home/server/Data -v /opt/docker/skyrimserver/logs:/home/server/logs tiltedphoques/st-reborn-server:latest`
3. Docker will now download the latest server image, and run it afterwards.
4. If you want to see the logs in your terminal, you can use this command:\
   `docker logs -tf "skyrimserver"`
5. Now your server is up and running.

### Start/Stopping your docker server

1. To stop your `skyrimserver`, simply run this command in your console
2. `docker stop skyrimserver` and it will stop your Skyrim Together Reborn server.
3. To start it again, simply run this command in your console
4. `docker start skyrimserver` and it will start your Skyrim Together Reborn server again

## I want to use docker-compose, what is the template?

```
version: "3.9"

services:
  skyrimserver:
    container_name: skyrimserver
    image: tiltedphoques/st-reborn-server:latest
    ports:
      - "10578:10578/udp"
    volumes:
     - /opt/docker/skyrimserver/config:/home/server/config
     - /opt/docker/skyrimserver/logs:/home/server/logs
     - /opt/docker/skyrimserver/Data:/home/server/Data
    restart: unless-stopped
```

#### Onwards to the next step!
