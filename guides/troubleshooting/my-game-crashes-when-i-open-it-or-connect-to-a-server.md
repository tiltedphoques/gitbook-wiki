# My game crashes when I open it or connect to a server

## Q: My game crashes when I open it, or when I connect to a server

**A:** Your CPU needs support for AES-NI (AES New Instructions). The reason why this is needed in the client and server is because they depend on libsodium lib, which relies on AES. Therefore, we need to wait until libsodium stops relying on AES (which is unlikely) or reimplement some parts with OpenSSL (time-consuming).

**A:** If you are experiencing this issue on an older AMD Phenom processor (users reporting the issue were using either an AMD Phenom II X4, AMD Phenom II X6, or an AMD Phenom Athlon II X4), unfortunately, it seems that line of CPUs is not supported.

**A:** If you are on a version earlier than 1.3.0, you **must** update your game as these versions are no longer supported.

##

## The issue still persists. What do I do?

**A:** When connecting, make sure you're using the correct IP address and port. It's a little detail, but I mistakenly misspelled my IP address, which crashed me to my desktop (CTD).

**A:** Delete your INI files from the `Skyrim Special Edition` folder in `My Games`. Then, relaunch SkyrimSE through Steam (not through MO2 or VMM) to allow it to regenerate the vanilla config files.

##
