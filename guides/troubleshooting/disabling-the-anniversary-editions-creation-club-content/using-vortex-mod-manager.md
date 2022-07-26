# Using Vortex Mod Manager

{% hint style="danger" %}
If you remove the Creation Club content, your existing savegame(s) may become unloadable.

Regardless, it is **strongly advised** that they be removed!
{% endhint %}

## Removing the Creation Club content

You can't actually disable them, so we'll have to delete them

Vortex Mod Manger (VMM) supports "ghosting" the files, which basically means renaming the files, but in my testing, it didn't work very well. So deleting the files is the best option.

You will need to remember this though:

Steam will try and redownload those files. E.g. if Skyrim has an update, or you reinstall the game, or if you `Verify the integrity of the game files` through Steam.

### Delete the files

1. Close Vortex Mod Manager (VMM)
2. Open this directory:\
   `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data`
3. Find these files:\
   `ccBGSSSE001-Fish.bsa`\
   `ccBGSSSE001-Fish.esm`\
   `ccBGSSSE025-AdvDSGS.bsa`\
   `ccBGSSSE025-AdvDSGS.esm`\
   `ccBGSSSE037-Curios.bsa`\
   `ccBGSSSE037-Curios.esl`\
   `ccQDRSSE001-SurvivalMode.bsa`\
   `ccQDRSSE001-SurvivalMode.esl`
4. And delete them.
5. Re-open VMM
6. Go to the `Plugins` menu, and the mods/plugins will not be listed anymore

![](https://shx.is/5CjqL0HvJ.gif)

## I need the Creation Club files back, what do I do?

If you want to restore the files, you can always `Verify integrity of game files` through Steam:

1. Find `The Elder Scrolls V: Skyrim Special Edition`
2. Right click and select `Properties`
3. Select `Local Files`
4. Select `Verify integrity of game files...`
5. Steam will re-download the Creation Club mods that you deleted
