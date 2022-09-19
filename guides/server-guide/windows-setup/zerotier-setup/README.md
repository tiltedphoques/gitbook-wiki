---
description: Using the ZeroTier application instead of port forwarding
---

# ZeroTier setup

This guide will help you create a Skyrim Together Reborn server, using the **ZeroTier** software.

The wonderful thing about ZeroTier is that it can connect people without the need for port forwarding. This is essentially the same as how Hamachi or Radmin works.

Before we begin installing and configuring ZeroTier, we must first configure the server. We will locate and launch `SkyrimTogetherServer.exe`, and the guide will walk you through the various configuration options and what they do.

It's critical that you've followed the guide so far, so that we're on the same page. Otherwise, you'll have to figure out the paths for yourself. If you've followed this guide so far, you can take the same paths I do, making everything easier.

## Initial setup

## [Option 1: Using MO2](./#using-modorganizer2) | [Option 2: Using VMM](./#using-vortex-mod-manager)

### ****

### **Using ModOrganizer2**

1. Open MO2
2. Right click the mod `Skyrim Together Reborn`
3. Select `Open in Explorer`
4. <img src="https://i.imgur.com/p3SxhRQ.png" alt="" data-size="original">
5. Inside will be a file called `meta.ini` and a folder named `Skyrim Together Reborn`
6. Enter the folder named `Skyrim Together Reborn`
7. Open the `SkyrimTogetherServer.exe`
8. A firewall popup will show mark, mark it both allowed for both private and public networks.
9. <img src="https://i.imgur.com/JQYlZSF.png" alt="" data-size="original">
10. If the popup did not appear, visit [this page](../../../troubleshooting/during-server-setup-my-firewall-didnt-ask-for-network-permission.md) in the troubleshooting section.
11. Now you can see the server is actually running:\
    ![](https://i.imgur.com/Fma2Sbe.png)\
12. As currently configured, **only you** can connect to your server for now, and we have yet to change any server options. We'll also figure that out in a minute.
      * To test if it works, launch `Skyrim Together Reborn` using MO2, and connect using `127.0.0.1` as your IP address, and using no password.
13. Close the `SkyrimTogetherServer.exe` for now.

![](https://i.imgur.com/JCAPct7.gif)



### **Using Vortex Mod Manager**

1. Open Vortex
2. Go to the `Mods` menu
3. Make sure `Skyrim Together Reborn` is installed and `Enabled`
4. Press `Windows Key + R` and enter this path in the `Run` window:\
   `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data\SkyrimTogetherReborn`
5. In that folder, open the `SkyrimTogetherServer.exe`
6. A firewall popup will show mark, mark it both allowed for both private and public networks.
7. ![](https://i.imgur.com/5haVkRt.png)
8. If the popup doesn't show up, don't worry, we'll figure it out in a minute.
9. Now you can see the server is actually running:\
   ![](https://i.imgur.com/837hau4.png)
10. As currently configured, **only you** can connect to your server for now, and we have yet to change any server options. We'll also figure that out in a minute.
      * To test if it works, launch `Skyrim Together Reborn` using Vortex, and connect using `127.0.0.1` as your IP address, and using no password.
11. Close the `SkyrimTogetherServer.exe` for now.

![](https://i.imgur.com/wpQwuDP.gif)

{% hint style="warning" %}
If the firewall notice **did** show up, you can safely continue the guide

If your firewall notice **did not** appear, visit [this page](../../../troubleshooting/during-server-setup-my-firewall-didnt-ask-for-network-permission.md)!
{% endhint %}

#### Onwards to the next step!
