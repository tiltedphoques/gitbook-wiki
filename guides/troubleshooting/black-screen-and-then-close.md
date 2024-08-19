# Black Screen and Crash

## My game opens to a black screen for a few seconds and then crashes!

Often this is caused by not launching **Skyrim Special Edition** via Steam at least once before starting the modding process. The steps to solve this issue vary depending on which mod manager you used:

### Vortex

Vortex, by default, uses the same location for configuration/INI files as unmodded Skyrim. You simply need to close Vortex, open Skyrim Special Edition Launcher via Steam, click `Options`, set your graphical properties, and then exit the Launcher. When you re-open SkyrimTogether via Vortex your problem should be solved.

### Mod Organizer 2

MO2, on the other hand, defaults to using custom INI location per profile. In the top-left of the MO2 window is a drop-down list of launch targets for Skyrim. One of the options should be **Skyrim Special Edition Launcher**: select this option and click `Run`. Once the Launcher is open, click `Options`, set your graphical properties, and then exit the Launcher. Chagne your launch target back to **SkyrimTogether** and click `Run`.

##

#### If when launching STR, you have black screen or experience crashes. Disable the NVIDIA overlay on GeForce Experience or NVIDIA APP.

**A:** If you have an NVIDIA Card, please disable the NVIDIA App's Overlay, or GeForce Experience Overlay. Some of its features interfere since the summer of 2024. You can also rollback to an earlier driver and see if the game runs better with it.
- GeForce Game Ready Driver WHQL 552.22 from April - https://www.nvidia.com/Download/Find.aspx

**A:** If the game still crashes or is showing a black screen, try uninstalling Community Shaders or any ENB or ReShade enhancements you have. Then see if Skyrim Together can launch with it disabled.

**A:** If you have a Windows version higher than 22H2 or you get DLL crash popups, try the following steps below.
- If it is EngineFixes.dll, uninstall that mod. It is not compatible with STR so you can't use mods depending on it
- If it is something that used to work in STR 1.5, downgrade conflicting Windows update 24H2 to 23H2 or 22H2
- If the DLL from a mod is still crashing, it is probably incompatible and should be disabled, like SmoothCam.dll

