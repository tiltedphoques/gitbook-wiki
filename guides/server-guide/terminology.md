# Terminology

## Terminology

We also need to establish some terminology. Specifically, ip addresses and networks.

I'm no networking expert, but these are the fundamentals that everyone should know and that will be used throughout the guide.

### **Local network**

Your home network is known as your local network. Everyone in your home who is connected to the router is a member of your **local network**.

### **"Outside" network**

Everyone who is not connected to your local network is considered to be on the **outside network**. That is, everyone who isn't connected to your home's router.

### **Local IPv4**

Your local IPv4 address is the one assigned to you by the router in your local network.

In some router software, the local IPv4 address is also referred to as the **Internal IP address.**

On Windows machines, it can be found by:

1. Pressing `Windows Key + R` to open the `Run` prompt
2. Write `cmd` and press `Enter`
3. Type `ipconfig /all`
4. Find the part where it says `IPv4 Address`.
5. In my case, my **local** IPv4 address is `192.168.50.209`

![](https://shx.is/5BxOG8FiU.gif)

### **Public IPv4**

Any of the following websites can help you find your local IPv4 address:

1. [ICanHazIP.com](https://icanhazip.com/)
2. [WhatIsMyIP.com](https://www.whatismyip.com/)
3. [WhatIsMyIPAddress.com](https://whatismyipaddress.com/)
4. [WhatIsMyIp.net](https://www.whatismyip.net/)

These websites will display your public IPv4 address. In most cases, this is the address that people should use to connect to you from any outside network.&#x20;

Except when using services such as Radmin, ZeroTier, or Hamachi. VPN software, such as the ones mentioned, generally uses a "managed IP", which only works with people on the same VPN network as you.

On some router software, the public IPv4 address is also referred to as the **External IP address**.

### **Managed IP**

This is the IP address that will be assigned to you by ZeroTier, Radmin, and/or Hamachi.

The managed IP address of the host is the IP address that you must use to connect to your server.

### **Localhost**

Localhost usually refers to or is a synonym for the IP address used by your own computer. `Localhost` is an IP address that is equivalent to `127.0.0.1`.

Every PC has its own `localhost` / `127.0.0.1` IP address to which only it can connect. This IP is typically used for testing.

For example, if you're hosting a server on the same PC that you play SkyrimSE on and want to make sure it's actually working.

### **Port forwarding**

Simply put, it means opening ports on your router, allowing people from outside your local network to connect to you via the port(s) you specify.

For example, the game server will be hosted on the standard port 10578. Your router's default setting is to close that port. That means no one from outside your local network will be able to connect.

If we forward port 10578 in our router, people outside of your local network will now be able to connect to your server via that port.

#### Onwards to the next step!
