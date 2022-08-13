# Port forwarding

## How to port forward

This step will be vastly different for each person. Simply because everyone has a different router and they all look (very) different.

I'll do my best to demonstrate how to do it on my router, but it may look drastically different on yours.

You can use a website like this to learn how to do it on your router:

1. Visit [PortForward.com](https://portforward.com/router.htm#1)
2. Locate your router
3. If your exact model isn't listed, try another from the same brand and see if the router UI matches yours. Then the same procedure should apply.

## What ports need to be forwarded?

By default, SkyrimTogetherServer.exe connects to port `10578`. You can change this in the `STServer.ini` file, but I recommend leaving it alone.

Your router will prompt you to specify which protocol it should forward. If you have the option of selecting `Both`, you should do so.

If you can only choose between `TCP` and `UDP`, create two port forwarding rules: one for `10578` UDP and one for `10578` TCP.

## How to port-forward (in my personal router)

_I'm using an ASUS AX86U router._

1. Navigate to your router's configuration page using the IP address you obtained in the previous step. In my case, the address will be `192.168.50.1`.
2. Go to `Open NAT`
3. Select `Enable port forwarding`
4. Select `+ Add` under `Game Profile`
5. Under `1) Game List` choose `Manual`
6. The `2) Protocol` step will probably be empty. If there is an option for you, select `PC`.
7. Now to fill out the settings.
8. **Service Name:** `Skyrim Reborn Together`
9. **Protocol:** `Both`
10. **External Port:** `10578`
11. **Internal Port:** `10578`
12. **Internal IP Address:** `192.168.50.104` <- the local IPv4
13. **Source IP:** leave empty
14. Press the `OK` button

![How to port forward on my AX68U router](https://i.imgur.com/ZsDMhaw.gif)

#### Onwards to the next step!
