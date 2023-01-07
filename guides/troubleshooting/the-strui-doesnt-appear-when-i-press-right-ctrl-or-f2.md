# The STRUI doesn't appear when I press RIGHT CTRL or F2

## Q: The STRUI doesn't appear when I press either `Right CTRL` or `F2`

**A:** First, ensure that you have followed this guide from beginning to end. If that's the case, it shouldn't happen in the first place. Check that your Skyrim Together Reborn mod folder, which contains the `SkyrimTogether.exe`, is placed at:

**For MO2 users:**\
`C:\Modding\MO2\mods\Skyrim Together Reborn\SkyrimTogetherReborn`

**For VMM users:**

`C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data\SkyrimTogetherReborn`

**A:** If the UI does not load, or the screen is covered with white boxes when pressing right control, exit to the main menu and load your save again. If that does not work, try restarting your game until it works.

**A:** Try running SkyrimSE in Windowed mode or Windowed Borderless.

**A:** Try restarting your PC. That has worked for some.

**A:** If you're using MO2, make sure the folder `C:\Modding\MO2\overwrite` is empty. If not, delete everything inside the folder, and start over.

**A:** You can try launching the game with `skse64_loader.exe`, loading your most recent savegame, and then exiting the game. Return to MO2 or VMM, and launch the game using the custom Skyrim Together Reborn launcher; it should now work. If you don't use SKSE, then try and launch SkyrimSE normally through Steam.

## None of that worked for me, what do I do?

**A:** You could try [removing the game](../client-setup/initial-setup/removing-the-old-setup.md), then [removing the mod](how-do-i-uninstall-the-mod/), and then re-doing the [entire guide](../getting-started.md).

**A:** You can use the cursor from F2/right control with the [F3 Debuggers menu](../../general-information/playguide.md#debugger-menu).
