# Address Library error

## Q: I get all types of errors regarding the address library

There are several different causes for the "address library not loading" error. This page covers those, and how to solve it.

### Wrong address library version

You need to install **All in one (1.6.X)**, not **All in one (1.5.X)**.

### Skyrim v1.5

You have Skyrim Special Edition v1.5 and have used a downgrading patcher. If you did, go to Steam and validate Skyrim's game files in order to install the most recent Special Edition, v1.6.

### Wrong game selection

When you launched Skyrim Together for the first time, you did not select SkyrimSE.exe when the selection popped up. You can fix this by going to SkyrimTogether.exe and double clicking it while holding spacebar. This should reopen the selection menu. Select **SkyrimSE.exe** this time.

If you require additional assistance, please see [this page](help-i-selected-the-wrong-.exe-when-first-launching-skyrimtogether.md).

### **Mod Organizer 2**

Go to Mo2, right click Address Library for SKSE Plugins, open file explorer, once there - copy the SKSE folder, go to `\SteamLibrary\steamapps\common\Skyrim Special Edition\Data`, and paste the SKSE folder into the **DATA FOLDER.**

### Other

If you still get this error, check the path located at the bottom of the error, and verify that address library is actually installed there.

## Any of that didn't work for me, what do I do?

If none of it works for you, you can start anew with the [client setup tutorial](../getting-started.md). Then it should surely work. It has been thoroughly tested and works for the majority of people.
