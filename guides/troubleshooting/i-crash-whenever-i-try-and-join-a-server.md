# I crash whenever I try and join a server

### Q: I crash whenever I join my friends server, but other people can join it just fine

**A:** You can try enabling `AES-NI` in your BIOS. This is apparently especially relevant for Intel CPUs. This is hard to guide you through, since almost every BIOS looks different.

#### Windows 10

To get to your BIOS, if you're using Windows 10, do the following steps:

1. Go to `Settings`
2. Select `Update and Security`
3. Select `Recovery`
4. Click `Restart`
5. Click `Troubleshoot`
6. Select `Advanced Options`
7. Select `UEFI Firmware Settings`
8. You should now enter your BIOS
9. Use whatever search function you have to find something related to `AES-NI`.
10. You can use the following keywords:\
    `AES`\
    `AES-NI`\
    `Data Protection Technology`\
    `Advanced Encryption Standard`
11. Enable `AES`/`AES-NI`
12. Save your settings and restart your PC - usually use the `F10` key.

#### Windows 11

To get to your BIOS, if you're using Windows 11, do the following steps:

1. Go to `Settings`
2. Select `System`
3. Select `Recovery`
4. Select `Restart now` right beside `Advanced startup`
5. Click `Troubleshoot`
6. Select `Advanced Options`
7. Select `UEFI Firmware Settings`
8. You should now enter your BIOS
9. Use whatever search function you have to find something related to `AES-NI`.
10. You can use the following keywords:\
    `AES`\
    `AES-NI`\
    `Data Protection Technology`\
    `Advanced Encryption Standard`
11. Enable `AES`/`AES-NI`
12. Save your settings and restart your PC - usually use the `F10` key.

**A:** Make sure that you're using the right IP address and port when connecting. Trivial thing, but I accidentally miswrote the ip address and that sent me straight to my desktop (CTD).

**A:** Try and delete your INI files from the `My Games\Skyrim Special Edition` folder. Then relaunch SkyrimSE normally through Steam (not through MO2), to let it regenerate the vanilla config files.



**Context:**

The reason why this is needed in the client and server is because they depend on libsodium lib which relies on AES. Therefore, we need to wait until libsodium stop relying on AES (which is unlikely, see) or reimplement some parts with OpenSSL (time consuming).
