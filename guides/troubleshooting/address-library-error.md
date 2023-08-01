# Address Library error

## Q: I get all types of errors regarding the Address Library

There are several different causes for the "Address Library not loading" error. This page covers the most common, and how to solve them.

### Wrong address library version

You need to install **All in one (Anniversary Edition)**, not **All in one (Special Edition)** even if you do not have the Anniversary Edition upgrade.

### Skyrim v1.5

You have Skyrim Special Edition v1.5 and have used a downgrading patcher. If you did, go to Steam and validate Skyrim's game files in order to install the most recent Special Edition, v1.6. Make sure to [disable/delete the included CC Content](disabling-the-anniversary-editions-creation-club-content/).

### Wrong game selection

When you launched Skyrim Together for the first time, you did not select SkyrimSE.exe when the selection popped up. You can fix this by going to SkyrimTogether.exe and double-clicking it while holding the spacebar. This should reopen the selection menu. Select **SkyrimSE.exe** this time.

If you require additional assistance, please see [this page](help-i-selected-the-wrong-.exe-when-first-launching-skyrimtogether.md).

### **Mod Organizer 2**

Go to Mo2, right-click Address Library for SKSE Plugins, open file explorer, once there - copy the SKSE folder, go to `\SteamLibrary\steamapps\common\Skyrim Special Edition\Data`, and paste the SKSE folder into the **DATA FOLDER.**

### Other

If you still get this error, check the path located at the bottom of the error, and verify that Address Library is actually installed there.

## None of that worked for me, what do I do?

If none of it works for you, you can start anew with the [client setup tutorial](../getting-started.md). It should surely work, it has been thoroughly tested and works for the majority of people.
