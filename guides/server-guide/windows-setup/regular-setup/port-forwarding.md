# Port forwarding

## How to port forward

This step is going to be wildly different from each person. Simply because each person has a different router, and they all look (very) different from eachother.

I will try to do my best at showing you how to do it on my router, but chances are it might look wildly different from yours.

To find out how to do it on **your** router, you can use a website like this:

1. Visit [PortForward.com](https://portforward.com/router.htm#1)
2. Locate your router
3. If your exact model isn't present on the list, try another one from the same brand name, and see if the router UI matches yours. Then it should be the same procedure.

## What ports need to be forwarded?

The `SkyrimTogetherServer.exe` uses the port `10578` by default. You can change this in the `STServer.ini`, but I recommend just leaving the default as is.

Your router will ask you what protocol it needs to forward. If you have the option choosing `Both`, then that's what you should do.

If you only have the option of choosing **either** `TCP` or `UDP`, create two port forwarding rules: One for `10578` UDP and one for `10578` TCP.

## How to port-forward (in my personal router)

_I'm using an ASUS AX86U router._

1. Go to your router's configuration page, with the IP you gathered from the last step. In my case, it'll be `192.168.50.1`.
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

![How to port forward on my AX68U router](https://shx.is/5BDuK3yHR.gif)

#### Onwards to the next step!
