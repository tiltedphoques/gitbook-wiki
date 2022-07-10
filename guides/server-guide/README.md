# Server guide

## Hosting a server

To host a server, you have two options: you can use a (free) server provider or you can host your own server.

### Third party server hosting

If you decide to go with a server provider, we recommend you go with [playtogether.gg](https://playtogether.gg/) (a free, Skyrim Together specific server hosting website). The setup for server hosting is significantly easier, so consider this option if you are not very handy with computers.

{% hint style="danger" %}
Due to the high load of people wanting to play on release day, playtogether.gg might not be available. Use the Hamachi tutorial with the Windows executable for the easiest way to set up a server on your own.
{% endhint %}

### Hosting your own server

You can also choose to run the server yourself. You can either run the server exe on Windows, `SkyrimTogetherServer.exe`, or you can use the docker image provided [here](https://hub.docker.com/r/tiltedphoques/st-reborn-server/tags) to run the server on Linux. By default, the server runs on port **10578**.

To host a server for people outside of your local network to connect to, you need to use Hamachi (scroll down for a hamachi guide below), or you need to port forward ([port forward guide](https://www.youtube.com/watch?v=ExrSULINq9c)).

{% hint style="warning" %}
Running the server makes it show up on the server list. This does **not** mean that people can connect to it. You will have to port forward to the port that the server is running on first.
{% endhint %}

#### Hamachi guide

Download Hamachi from [https://www.vpn.net/](https://www.vpn.net/) and follow the tutorial linked here: [https://www.youtube.com/watch?v=bWbo0gcFqA8](https://www.youtube.com/watch?v=bWbo0gcFqA8). Once you open Hamachi and log in, copy your IPv4 from Hamachi and add :10578 to the end of it. After this, run the server exe file. Following this, load up your game (with a fresh save, after Helgen) and hit right control (rctrl), go to the connect tab and enter with localhost. Have others join with the IPv4 with the port :10578 (if the localhost doesn't work, try using the IPv4 you got from Hamachi and use that instead.)

#### Windows hosting

To host a server within your local network (aka playing with other people in your house), simply launch the server application, `SkyrimTogetherServer.exe`, and have other people in your house connect to your local IP address (a guide on how to find your local IP address can be found [here](https://lifehacker.com/how-to-find-your-local-and-external-ip-address-5833108)).

#### Docker hosting

{% hint style="warning" %}
If you are using docker, we expect a certain level of proficiency with docker from you. We are not going to teach you how to use docker, as there are hundreds of tutorials on how to do that already. If this is too difficult for you, we recommend you either run the Windows server executable, or you use third party server hosting.
{% endhint %}

You can use the docker image provided [here](https://hub.docker.com/r/tiltedphoques/st-reborn-server/tags) to run the server on Linux. To run the server in its default configuration, run the following command:

`docker run -it -p 10578:10578/udp tiltedphoques/st-reborn-server:latest`

To use a custom server configuration file, you need to use docker volumes. You need to create a folder that contains the `STServer.ini` config file provided with the mod. Then, you need to point docker to that file. If, for example, you are on Windows, and you put the config file in `C:\config\`, then you would use the following command:

`docker run -it -p 10578:10578/udp -v C:\config\:/home/server/config/ tiltedphoques/st-reborn-server:latest`
