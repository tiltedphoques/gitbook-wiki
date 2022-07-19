# Using ModOrganizer2

## Removing the Creation Club content

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
