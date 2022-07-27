# Using Vortex Mod Manager (VMM)

## Using NVIDIA Control Panel

We must configure NVIDIA Control Panel to use your dedicated GPU rather than your integrated graphics unit (iGPU). Simply follow the steps below to accomplish this.

1. Navigate to your `NVIDIA Control Panel`.
2. Select `Manage 3D Settings`
3. Select `Program Settings`
4. Press the `Add` button
5. Navigate to the folder:\
   `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data\SkyrimTogetherReborn`
6. Select the `SkyrimTogether.exe` and press `Open`
7. Find the `2. Select the preferred graphics processor for this program`
8. Select `High-performance NVIDIA processor` from the drop-down menu
9. Press the `Apply` button.
10. Your system should now use the proper GPU, when playing Skyrim Together Reborn.

![](https://shx.is/5CXcBI8Al.gif)

## Using Windows 11

Even though Windows 11 claims to be able to control your graphics processor natively via their new "Graphics settings" menu, the NVIDIA Control Panel solution is still the recommended approach.

* Open `Settings`
* Go to `Display`
* Find the `Graphics` menu
* Under the `Custom options for apps`, select `Browse`
* Navigate to the folder:\
  `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data\SkyrimTogetherReborn`
* Select the `SkyrimTogether.exe` and press `Add`
* Select `Options`
* Choose the `High performance` option and press `Save`
* Your system should now use the proper GPU, when playing Skyrim Together Reborn.

![](https://shx.is/5CXivFvB8.gif)
