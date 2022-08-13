# Launching SkyrimTogether through MO2

## Launching `SkyrimTogether.exe` for the first time

1. Open MO2
2. Make sure `Skyrim Together Reborn` has been selected in the launch option dropdown menu
3. ![](https://i.imgur.com/r3mYNJL.png)
4. Press `Run`
5. A popup window should appear, prompting you to choose an executable from the Skyrim root folder.
6. **This is extremely important! Select SkyrimSE.exe and press the Open button.**

![](https://i.imgur.com/Cw1qkJF.png)

7\. It may display an error like this, but you can safely disregard it by pressing `Close`. It's looking for the `Address Library for the SKSE` mod, but that won't be loaded until the game starts.

![](https://i.imgur.com/NwvLd60.png)

8\. Return to MO2 and press `Run`.

9\. Skyrim will now launch, but you can close it for the time being.

![](https://i.imgur.com/r55et7l.gif)

## Nothing pops up,when I open `SkyrimTogether.exe` / I chose the wrong .exe

You have three options

### **Option 1**

1. Press the `WindowsKey + R` and copy & paste this into the `Run` prompt:\
   `C:\Modding\MO2\mods\Skyrim Together Reborn\SkyrimTogetherReborn\SkyrimTogether.exe -r`
2. Then select the right executable (`SkyrimSE.exe`)

### **Option 2**

1. Head to the Skyrim Together Reborn mod folder location:\
   `C:\Modding\MO2\mods\Skyrim Together Reborn\SkyrimTogetherReborn`
2. Hold down your `Spacebar` and then double click the `SkyrimTogether.exe`. It shoud allow you to choose another executable.

### **Option 3**

1. Press `Windows Key + R` to open the `Run` menu
2. Type `regedit` to open the Registry Editor.
3. Select the folder `HKEY_CURRENT_USER`
4. Select the folder `Software`
5. Delete the folder called `TiltedPhoques`
6. This will remove the `SkyrimTogether.exe`'s default preference and prompt you again when you reopen the `SkyrimTogether.exe`.

#### Onwards to the next step!
