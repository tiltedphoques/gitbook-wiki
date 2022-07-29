# During server setup, my firewall didn't ask for network permission!

## The firewall didn't popup! Help!

Because the guide is written using Windows 11, the UI will reflect that. I believe it is similar to Windows 10's UI.

## [Option 1: Using MO2](during-server-setup-my-firewall-didnt-ask-for-network-permission.md#using-modorganizer2) | [Option 2: Using VMM](during-server-setup-my-firewall-didnt-ask-for-network-permission.md#undefined)



### Using ModOrganizer2

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

### Using Vortex Mod Manager <a href="#undefined" id="undefined"></a>

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
    `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data\SkyrimTogetherReborn`
13. Select the `SkyrimTogetherServer.exe`
14. Press `Next`
15. Select `Allow the connection`
16. Select `Private` and `Public` but leave `Domain` unchecked
17. Give it a name. I recommend `Multiplayer Server for Bethesda games`.
18. Done for now.
