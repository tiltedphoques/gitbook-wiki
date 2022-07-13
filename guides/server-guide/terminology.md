# Terminology

### Terminology

We also need to get some terminology in place. Mostly regarding ip addresses and networks.

I'm no expert in networking, but these are the basics, that are good to know, and that will be used throughout the guide.

#### **Local network**

Your local network is the network that you have at your home. Everyone who's connected to the router in your home, is part of your **local network**.

#### **"Outside" network**

Is basically everyone who's **not** connected to your local network. Meaning, everyone who's **not** connected to the router in your house.

#### **Local IPv4**

Your local IPv4 is the ip address that the router in your local network will assign to you.

The local IPv4 is sometimes named as I**nternal IP** as well in some router software.

On Windows machines, it can be found by:

1. Pressing `Windows Key + R` to open the `Run` promt
2. Write `cmd` and press `Enter`
3. Type `ipconfig /all`
4. Find the part where it says `IPv4 Address`.
5. In my case, my **local** IPv4 address is `192.168.50.209`

![](https://shx.is/5BxOG8FiU.gif)

#### **Public IPv4**

Your local IPv4 can be easily found using websites, like any of these:

1. [ICanHazIP.com](https://icanhazip.com/)
2. [WhatIsMyIP.com](https://www.whatismyip.com/)
3. [WhatIsMyIPAddress.com](https://whatismyipaddress.com/)
4. [WhatIsMyIp.net](https://www.whatismyip.net/)

These site will show your **public** IPv4. This will be the address that people should use, in most cases, to connect to you from any outside network. Except if you are using services like Radmin, ZeroTier or Hamachi.

The public IPv4 is sometimes named as **External IP** as well on some router software.

#### **Managed IP**

This is the IP address that ZeroTier will assign to you.

The managed IP of the host, is the IP address that you will have to use, to connect to your server.

#### **Localhost**

Localhost usually refers to, or is a synonym, to the IP used by your own PC only. The `localhost` is an IP address equivilant to `127.0.0.1`.

Every PC has their own `localhost` / `127.0.0.1` IP address, that only they can connect to. This IP is usually used in testing.

E.g. if you're hosting a server on the same PC as you play SkyrimSE with, and you want to check it's actually working.

#### **Port forwarding**

Basically means opening ports on your router, enabling people from outside your local network to connect to you, using the port(s) you choose.

E.g. the game server will be hosted on the default port of `10578`. That port is **closed** by default on your router. Which means that no-one from the **outside** of your local network, will be able to connect.

If we forward the port `10578` in our router, that means that people from the **outside** of your local network, will now be able to connect to your server, using that port.

### Onwards to the next step!
