# Launching SkyrimTogether through MO2

We are very close now :thumbsup:

### Launching `SkyrimTogether.exe` for the first time

1. Open MO2
2. Make sure `Skyrim Together Reborn` has been selected in the launch option dropdown menu
3. ![](https://shx.is/5BlD3wkRM.png)
4. Press `Run`
5. A popup should appear, asking you to select an executable in the Skyrim root folder.
6. **Very important! Select `SkyrimSE.exe` and press Open**

![](https://shx.is/5BlEBHSqt.png)

7\. It might give you an error like so, but you can safely ignore it by pressing `Close`.\
It's looking for the `Address Library for SKSE` mod, but that will only be loaded upon launch.

![](https://shx.is/5BlGCrk0m.png)

8\. Return to MO2 and press `Run`.

9\. Skyrim will now launch, but you can close it again for now.

![](https://shx.is/5BlILHGmw.gif)

### Oh shit! I selected the wrong `.exe` file, what do I do??

You have three options

#### Option 1

1. Press the `WindowsKey + R` and copy & paste this into the `Run` prompt:\
   `C:\Modding\MO2\mods\Skyrim Together Reborn\SkyrimTogetherReborn\SkyrimTogether.exe -r`
2. Then select the right executable (`SkyrimSE.exe`)

#### Option 2

1. Head to the Skyrim Together Reborn mod folder location:\
   `C:\Modding\MO2\mods\Skyrim Together Reborn\SkyrimTogetherReborn`
2. Hold down your `Spacebar` and then double click the `SkyrimTogether.exe`. It shoud allow you to choose another executable.

#### Option 3

1. Press `Windows Key + R` to open the `Run` menu
2. Type `regedit` to open the Registry Editor.
3. Select the folder `HKEY_CURRENT_USER`
4. Select the folder `Software`
5. Delete the folder called `TiltedPhoques`
6. This will remove the default preference of the `SkyrimTogether.exe`, and it will ask you again upon reopening the `SkyrimTogether.exe`.



### Onwards to the next step!
