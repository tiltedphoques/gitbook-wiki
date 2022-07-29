# Launching SkyrimTogether through VMM

## Launching `SkyrimTogether.exe` for the first time

1. Open Vortex/VMM
2. Locate the custom launcher we created in the previous step and click the play button.
3. ![](https://shx.is/5BKQYt5oq.png)
4. A popup window should appear, prompting you to choose an executable from the Skyrim root folder.
5. **This is extremely important! Select SkyrimSE.exe and press the Open button.**

![It's very important to select SkyrimSE.exe!](https://shx.is/5BlEBHSqt.png)

6\. Skyrim Together Reborn will now launch.

7\. Close it after you reached the main menu.

![](https://shx.is/5BKRNVIxA.gif)

## Nothing pops up,when I open `SkyrimTogether.exe` / I chose the wrong .exe

You have three options

### **Option 1 (using VMM)**

1. Press the `WindowsKey + R` and copy & paste this into the `Run` prompt:\
   `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data\SkyrimTogetherReborn\SkyrimTogether.exe -r`
2. Then select the right executable (`SkyrimSE.exe`)

### **Option 2 (using VMM)**

1. Head to the Skyrim Together Reborn mod folder location:\
   `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data\SkyrimTogetherReborn`
2. Hold down your `Spacebar` and then double click the `SkyrimTogether.exe`. It shoud allow you to choose another executable.

### **Option 3 (works regardless of mod manager choice)**

1. Press `Windows Key + R` to open the `Run` menu
2. Type `regedit` to open the Registry Editor.
3. Select the folder `HKEY_CURRENT_USER`
4. Select the folder `Software`
5. Delete the folder called `TiltedPhoques`
6. This will remove the default preference of the `SkyrimTogether.exe`, and it will ask you again upon reopening the `SkyrimTogether.exe`.

#### Onwards to the next step!
