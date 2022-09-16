---
description: Using port forwarding
---

# Regular setup

This section of the guide will walk you through the various config options and what they do, as well as how to set up a server using `SkyrimTogetherServer.exe`.

It's critical that you've followed the guide so far, so that we're using the same paths. Otherwise, you'll have to figure out the paths for yourself.

If you've followed this guide so far, you can take the same paths the guide does, making everything easier.

## Initial setup

## [Option 1: Using MO2](./#using-modorganizer2) | [Option 2: Using VMM](./#using-vortex-mod-manager)



### **Using ModOrganizer2**

1. Open MO2
2. Right click the mod `Skyrim Together Reborn`
3. Select `Open in Explorer`
4. <img src="https://i.imgur.com/7ngdTQh.png" alt="" data-size="original">
5. Inside will be a file called `meta.ini` and a folder named `Skyrim Together Reborn`
6. Enter the folder named `Skyrim Together Reborn`
7. Open the `SkyrimTogetherServer.exe`
8. A firewall popup will show mark, mark it both allowed for both private and public networks.
9. <img src="https://i.imgur.com/8AWbvA3.png" alt="" data-size="original">
10. If the popup did not appear, visit [this page](../../../troubleshooting/during-server-setup-my-firewall-didnt-ask-for-network-permission.md) in the troubleshooting section.
11. Now you can see the server is actually running:\
    ![](https://i.imgur.com/katpGFn.png)
12. If you want to test if it works, **only you** can now connect to your server now, and it's not configured. We'll also figure that out in a minute.\
      * To test if it works, launch `Skyrim Together Reborn` using MO2, and connect using `127.0.0.1` as your IP address, and using no password.
13. Close the `SkyrimTogetherServer.exe` for now.

![](https://i.imgur.com/vgRaDVA.gif)



### **Using Vortex Mod Manager**

1. Open Vortex
2. Go to the `Mods` menu
3. Make sure `Skyrim Together Reborn` is installed and `Enabled`
4. Press `Windows Key + R` and enter this path in the `Run` window:\
   `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data\SkyrimTogetherReborn`
5. In that folder, open the `SkyrimTogetherServer.exe`
6. A firewall popup will show mark, mark it both allowed for both private and public networks.
7. ![](https://i.imgur.com/1ze68ZW.png)
8. If the popup doesn't show up, don't worry, we'll figure it out in a minute.
9. Now you can see the server is actually running:\
   ![](https://i.imgur.com/1ljV2pk.png)
10. If you want to test if it works, **only you** can now connect to your server now, and it's not configured. We'll also figure that out in a minute.
      * To test if it works, launch `Skyrim Together Reborn` using MO2, and connect using `127.0.0.1` as your IP address, and using no password.
11. Close the `SkyrimTogetherServer.exe` for now.

![](https://i.imgur.com/U2xVDa7.gif)

{% hint style="warning" %}
If the firewall notice **did** show up, you can safely continue the guide

If your firewall notice **did not** appear, visit [this page](../../../troubleshooting/during-server-setup-my-firewall-didnt-ask-for-network-permission.md)!
{% endhint %}

#### Onwards to the next step!
