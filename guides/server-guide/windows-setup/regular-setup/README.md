---
description: Using port forwarding
---

# Regular setup

This will setup a server using the `SkyrimTogetherServer.exe` and I'll try and walk you through the different config options that we have, and what they do.

It's very important that you've followed the guide so far, so that we share the same paths. If not, you'll have to figure out the paths yourselves.

If you've used this guide so far, you can use the exact same paths as I use, which makes everything easier.



### Initial setup

1. Open MO2
2. Right click the mod `Skyrim Together Reborn`
3. Select `Open in Explorer`
4. &#x20;![](https://shx.is/5BzT3n7WX.png)
5. Inside will be a file called `meta.ini` and a folder named `Skyrim Together Reborn`
6. Enter the folder named `Skyrim Together Reborn`
7. &#x20;Open the `SkyrimTogetherServer.exe`
8. A firewall popup will show mark, mark it both allowed for both private and public networks.
9. ![](https://shx.is/5BzTNr2rT.png)
10. If the popup doesn't show up, don't worry, we'll figure it out in a minute.
11. Now you can see the server is actually running:\
    ![](https://shx.is/5BzUvqRTO.png)\

12. For now, **only you** can connect to it, and it's not configured. We'll also figure that out in a minute.
13. Close the `SkyrimTogetherServer.exe` for now.

![](https://shx.is/5BzWiRKr7.gif)

14\. If you want to test if it works, **only you** can now connect to your server now.

15\. Launch `Skyrim Together Reborn` using MO2, and connect using `127.0.0.1` as your IP address, and using no password.

### If your firewall _did_ popup, then onwards to the next step!

###

### The firewall didn't popup! Help!

I'm using Windows 11, so the UI will reflect that. I think it's fairly the same as in Windows 10.

1. Press the `Windows Key`
2. Search for `firewall`
3. Select the `Windows Defender Firewall with Advanced Security`
4. ![](https://shx.is/5BzXk19Mc.png)
5. Select `Inbound Rules`
6. Verify the rules have not been created before. If they **have** been created before, there will be two rules named `Multiplayer Server for Bethesda games`. If they are there, you can safely continue.
7. If they are not there, we will now create them manually.
8. To the right side of the `Windows Defender Firewall`, there'll be a button named ![](https://shx.is/5BzYyMbqm.png)
9. Select `New Rule`. A new window will appear.
10. Select `Program`, then `Next`.
11. Select `This program path` and press the ![](https://shx.is/5BzZ2ocvz.png) button
12. Go to the folder location:\
    `C:\Modding\MO2\mods\Skyrim Together Reborn\SkyrimTogetherReborn`
13. Select the `SkyrimTogetherServer.exe`
14. Press `Next`
15. Select `Allow the connection`
16. Select `Private` and `Public` but leave `Domain` unchecked
17. Give it a name. I recommend `Multiplayer Server for Bethesda games`.
18. Done for now.

![](https://shx.is/5Bz\_DM9wr.gif)

### Onwards to the next step!
