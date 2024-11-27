# My game crashes when I open it or connect to a server

## Q: My game crashes when I open it, or when I connect to a server

**A:** Your CPU needs support for AES-NI (AES New Instructions). The reason why this is needed in the client and server is because they depend on libsodium lib, which relies on AES. Therefore, we need to wait until libsodium stops relying on AES (which is unlikely) or reimplement some parts with OpenSSL (time-consuming).

**A:** If you are experiencing this issue on an older AMD Phenom processor (users reporting the issue were using either an AMD Phenom II X4, AMD Phenom II X6, or an AMD Phenom Athlon II X4), unfortunately, it seems that line of CPUs is not supported.

**A:** If you are on a version earlier than 1.3.0, you **must** update your game as these versions are no longer supported.

##

## Q: My game crashes when I open it, or just shows a black screen

**A:** If you have an NVIDIA Card, please disable the NVIDIA App's Overlay, or GeForce Experience Overlay. Some of its features interfere since the summer of 2024. You can also rollback to an earlier driver and see if the game runs better with it.
- GeForce Game Ready Driver WHQL 552.22 from April - https://www.nvidia.com/Download/Find.aspx

**A:** If the game still crashes or is showing a black screen, try uninstalling Community Shaders or any ENB or ReShade enhancements you have. Then see if Skyrim Together can launch with it disabled.

**A:** If you have a Windows version higher than 22H2 or you get DLL crash popups, try the following steps below.
- If it is EngineFixes.dll, uninstall that mod. It is not compatible with STR so you can't use mods depending on it
- If it is something that used to work in STR 1.5, downgrade conflicting Windows update 24H2 to 23H2 or 22H2
- If the DLL from a mod is still crashing, it is probably incompatible and should be disabled, like SmoothCam.dll

##

## The issue still persists. What do I do?

**A:** When connecting, make sure you're using the correct IP address and port. It's a little detail, but I mistakenly misspelled my IP address, which crashed me to my desktop (CTD).

**A:** Delete your INI files from the `Skyrim Special Edition` folder in `My Games`. Then, relaunch SkyrimSE through Steam (not through MO2 or VMM) to allow it to regenerate the vanilla config files.

##
