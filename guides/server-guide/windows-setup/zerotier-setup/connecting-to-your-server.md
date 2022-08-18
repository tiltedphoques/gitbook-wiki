# Connecting to your server

## How to connect to the server

This page is intended to show the host's friend(s) how to connect to his or her server.

## **Installing ZeroTier**

It's actually quite easy. We only need to download the ZeroTier client.

1. Go to the download page, and select `Windows`.\
   ![](https://i.imgur.com/oieSSOF.png)
2. Open the `ZeroTier One.msi` file\
   ![](https://i.imgur.com/LGMBfam.png)
3. There will be no installation prompts or instructions.
4. When it's finished, you should see this icon ![](https://i.imgur.com/y7wP8VV.png) in your system tray.

## Joining your host's network

We now need to join the ZeroTier network of the server host.

1. Find the little ![](https://i.imgur.com/y7wP8VV.png) icon in your system tray
2. Right click and select `Join New Network...`\
   ![](https://i.imgur.com/CRa9JrG.png)
3. Get the `Network ID` from your **host**!\
   ![](https://i.imgur.com/0mOvowr.png)
4. You can now confirm that you have joined the network by right-clicking the ZeroTier tray icon:\
   ![](https://i.imgur.com/dJdPrSU.png)
5. Remind your server host that you need to be authorized. They will understand what it means!

## Using the Skyrim Together Reborn UI (STRUI)

Now to connect to your friends Skyrim Together Reborn server.

1. To access the Skyrim Together Reborn UI, press `F2` or `Right-CTRL`. From now on, the guide will refer to it as the `STRUI`.
2. Open up the `STRUI` by pressing either `F2` or `Right-CTRL`.
	- If `STRUI` does not open, please see [this page](../../../troubleshooting/the-strui-doesnt-appear-when-i-press-right-ctrl-or-f2.md) for help.
3. Press the `Connect` button to start connecting to a server

![](https://i.imgur.com/EYwwO6P.png)

## Connecting to a server

**Please make sure you have finished the Helgen intro sequence / tutorial before following these steps.**

1. Before you press `Connect`, you will need to enter your server's connection information.
2. There will be an `Address` field and a `Password` field.
3. In the `Address` field, you should put your server's managed IPv4 address.
   - If you're the one hosting it on your PC, you will enter the IP address `127.0.0.1`.
   - If you're a friend of the host, trying to connect to their ZeroTier hosted server, you will need to enter [the managed IP address](./authorizing-users-in-zerotier-network.md#what-ip-address-should-i-send-to-my-friend).
4. Press `Connect` to connect to the server; there should be a visual and an audial confirmation that you're connected.
5. It should say `Succesfully connected to a server` in the little chat window.
6. Now you should be connected and ready to play Skyrim Together Reborn with your friends. :thumbsup:

![Visit the Server setup section of this wiki to learn how to host a server!](https://i.imgur.com/X6INNOZ.gif)

{% hint style="warning" %}
Read the [playguide](../../../../general-information/playguide.md) to learn how to properly complete quests with your friends!

If you want to do quests with your friends, you must first read the [playguide](../../../../general-information/playguide.md).
{% endhint %}



## **Notes:**

1. If you have any problems, take a look through the [Troubleshooting pages](../../../troubleshooting/) on this wiki.
2. If the troubleshooting pages were ineffective in helping you, you can always ask questions on the [Discord server](https://discord.com/invite/skyrimtogether).
3. If your connection times out, make sure you have ZeroTier open, on both the **server host** and on your PC.

#### That was it, for the ZeroTier server setup.
