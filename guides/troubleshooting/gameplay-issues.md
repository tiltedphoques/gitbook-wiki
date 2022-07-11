# Gameplay issues troubleshooting

### Enemies not dying

Some enemies might not die if they were killed by a kill move. Install this mod to disable kill moves, essentially solving this issue: [https://www.nexusmods.com/skyrimspecialedition/mods/13395](https://www.nexusmods.com/skyrimspecialedition/mods/13395)

### UI not showing

If the UI does not load, or the screen is covered with white boxes when pressing right control, exit to the main menu and load your save again. If that does not work, try restarting your game until it works.

### Crashing on connect

We are not sure what causes this yet exactly, but one possible cause is custom skyrim INI files. Delete your INI files in "**Documents\My Games\Skyrim Special Edition**" and launch Skyrim through Steam once to regenerate vanilla INI files.

### Crashing on connect (AES-NI)
The mod will crash without any error message (in the client and/or the server) if the processor support for AES-NI is not enabled. Note that most of new processors support AES-NI (see [list](https://en.wikipedia.org/wiki/AES_instruction_set#Intel)). You can enable support for AES-NI in the BIOS menu.

If you are not familiar with how to open the BIOS menu you can go throw the following steps:

Option 1 (Windows 10 only):
 - Hold the key *shift* while clicking the *restart* button in Windows.

Option 2:
 - Go to *Settings*
 - Select *Update and Security*
 - Select *Recovery*
 - Click *Restart*
<img src="https://i.imgur.com/oCLT22b.png" alt="Advanced restart" width="50%"/>
 
 - Click *Troubleshoot*
 - Select *Advanced Options*
 - Select *UEFI Firmware Settings*

Once you are within the BIOS menu:
 - BIOS differs depending on Firmware. Search for *AES*, *AES-NI*, *Data Protection Technology* or *Advanced Encryption Standard*, and enable it.
 - Do not alter anything else. You can *probably* press F10 to save your settings and exit.

Context: the reason why this is needed in the client and server is because they depend on libsodium lib which relies on AES. Therefore, we need to wait until libsodium stop relying on AES (which is unlikely, [see](https://github.com/ValveSoftware/GameNetworkingSockets/issues/243)) or reimplement some parts with OpenSSL (time consuming).
