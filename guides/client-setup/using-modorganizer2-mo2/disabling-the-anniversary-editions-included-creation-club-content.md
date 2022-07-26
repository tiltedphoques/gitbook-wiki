# Disabling the included Creation Club content

{% hint style="info" %}
When Bethesda released the Anniversary Upgrade DLC, the game version was updated to v1.6.

Whether you had purchased the DLC or not, they included four Creation Club items in that update.

These CC items have been shown to make the Skyrim Together Reborn experience more unstable, and prone to crashing more frequently.

This guide will demonstrate how to remove the included CC content using either MO2 or VMM.
{% endhint %}

{% hint style="danger" %}
If you remove the Creation Club content, your existing savegame(s) may become unloadable.

Regardless, it is **strongly advised** that they be removed!
{% endhint %}

## Disabling the included Creation Club content

You can't actually disable them, so we'll have two options to choose from:

Pick only one of these.

1. Moving the files and letting MO2 handle it
2. Deleting the files manually

Remember, no matter what option you pick:

Steam will try and redownload those files. E.g. if Skyrim has an update, or you reinstall the game, or if you `Verify the integrity of the game files` through Steam.

### Option 1: Moving the files and letting MO2 handle it

1. Close MO2
2. Open this directory:\
   `C:\Modding\MO2\mods`
3. Create a folder in there, named `CreationClubContent`
4. Full path should be:\
   `C:\Modding\MO2\mods\CreationClubContent`
5. Now, open this directory:
6. `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data`
7. Find these files:\
   `ccBGSSSE001-Fish.bsa`\
   `ccBGSSSE001-Fish.esm`\
   `ccBGSSSE025-AdvDSGS.bsa`\
   `ccBGSSSE025-AdvDSGS.esm`\
   `ccBGSSSE037-Curios.bsa`\
   `ccBGSSSE037-Curios.esl`\
   `ccQDRSSE001-SurvivalMode.bsa`\
   `ccQDRSSE001-SurvivalMode.esl`
8. Move the files into this folder:\
   `C:\Modding\MO2\mods\CreationClubContent`
9. Re-open MO2
10. Now you can enable/disable the `CreationClubContent` as you would any other mod.

![Option 1](https://shx.is/5BsA4biJa.gif)

### Option 2: Deleting the files

1. Close MO2
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
5. Re-open MO2, and the mods will not be listed anymore.

![Option 2](https://shx.is/5BsA\_LBe2.gif)

## I need the Creation Club files back, what do I do?

If you chose the **2nd option**, and want the files again you can always `Verify integrity of game files` through Steam:

1. Find `The Elder Scrolls V: Skyrim Special Edition`
2. Right click and select `Properties`
3. Select `Local Files`
4. Select `Verify integrity of game files...`
5. Steam will re-download the Creation Club mods that you deleted
