# My game crashes when I open it, or connect to a server

## Q: My game crashes when I open it, or when I connect to a server

**A:** Your CPU needs support for AES-NI (AES New Instructions). The reason why this is needed in the client and server, is because they depend on libsodium lib, which relies on AES. Therefore, we need to wait until libsodium stop relying on AES (which is unlikely), or reimplement some parts with OpenSSL (time consuming).

## How do I know if my CPU supports AES-NI? (Intel)

1. Find the name of your CPU, using this method:
2. Press your `Windows key` and search for `System information`
3. Find the line where it says `Processors` and write down the name.
4. Then visit the [this page](https://ark.intel.com) from Intel.
5. Use the search function:\
   ![](https://shx.is/5BFtNOIfU.png)
6. Type in your CPU, e.g. `i7-9700K` and select it:\
   ![](https://shx.is/5BFwpTD8m.png)
7. Search for `AES New Instructions` on the page that opens
8. If it says `Yes`, it's supported on your CPU. If it says `No`, it's not supported on your CPU.

## How do I know if `AES-NI` enabled?

We need to download a tool named `CPU-Z`.

1. Download CPU-Z [here](https://www.cpuid.com/softwares/cpu-z.html).
2. Select the version you prefer (setup or portable version)
3. Download and install it
4. Open CPU-Z and look for `AES` under `Instructions`:\
   ![](https://shx.is/5BFxts8CR.png)
5. If you can find `AES`, it should be enabled.

## How do I enable it in my BIOS?

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

## I have AES-NI enabled, but the issue still persists. What do I do?

**A:** Make sure that you're using the right IP address and port when connecting. Trivial thing, but I accidentally miswrote the ip address and that sent me straight to my desktop (CTD).

**A:** Try and delete your INI files from the `My Games\Skyrim Special Edition` folder. Then relaunch SkyrimSE normally through Steam (not through MO2), to let it regenerate the vanilla config files.

##
