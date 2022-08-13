# Explaining bEnableModcheck

## What does `bEnableModcheck` do?

The `bEnableModcheck` parameter allows you to enable or disable the option of enforcing a mod policy.

If you **enable** `bEnableModcheck`, everyone who connects to your server will go through the following process:

1. Player A connects to your server, which has modcheck enabled.
2. Your server will examine Player A's `loadorder.txt` file.
3. If the `loadorder.txt` file on the server matches, Player A will now join your server.
4. If the `loadorder.txt` file does not match the one on the server, Player A will be denied access to the server.

If you **disable**`bEnableModcheck`, everyone who connects to your server will go through the following process:

1. Player A connects to your server, which has modcheck disabled.
2. Your server will not examine Player A's `loadorder.txt` file.
3. Even if you use different mods, the player will be allowed to join.

The reason for enabling this is to increase the chances of having a more stable gaming session and/or playthrough.

It is not necessary to use if you and your friends are not using mods (or if you are only using `Address Library for SKSE`).

## Oh! I want that! I want my server to kick players, that doesn't use the mods that I choose!

Alright! To do so, we must obtain your `loadorder.txt` from MO2 or VMM and place it in the correct location.

## [Option1: Using MO2](explaining-benablemodcheck.md#using-mo2) | [Option2: Using VMM](explaining-benablemodcheck.md#using-vortex-mod-manager)

### Using **ModOrganizer2**

1. Open MO2
2. Enable the mods you want to enforce.
3. **Make sure** they're in the load order that you want to enforce.
4. In my case, I only have 3 mods, so it'll look like this:

![](https://sxcu.net/5BAiKMkPL.png)

5\. Go to the folder, where the `loadorder.txt` is located:\
`C:\Modding\MO2\profiles\Skyrim Together Reborn`

6\. Find the file named `loadorder.txt`

7\. Right click it, and select `Copy`

8\. Go back to the Skyrim Together Reborn folder:\
`C:\Modding\MO2\mods\Skyrim Together Reborn\SkyrimTogetherReborn`

9\. Create a folder named `Data` (important with uppercase D)

10\. Inside the `Data` folder, paste the `loadorder.txt` that we copied before.

11\. Go back to the `config` folder, where `STServer.ini` is located.

12\. Open the `STServer.ini` and change `bEnableModcheck` from `false` to `true`

13\. Save the file

14\. Run `SkyrimTogetherServer.exe` again

15\. It should now say `ModPolicy is active` and your mod policy will now be enforced.

![Here's the whole process of how to do it](https://sxcu.net/5BAmnL9Ni.gif)

### Using Vortex Mod Manager

1. Open Vortex/VMM
2. Go to the `Mods` menu
3. Select the folder icon that says `Open...`
4. Select `Open Game Application Data Folder`\
   ![](https://sxcu.net/5BO\_roz5c.png)
5. Find the file named `loadorder.txt`
6. Right click it, and select `Copy`
7. Go back to the Skyrim Together Reborn folder:\
   `C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition\Data\SkyrimTogetherReborn`
8. Create a folder named `Data` (important with uppercase D)
9. Inside the `Data` folder, paste the `loadorder.txt` that we copied before.
10. Go back to the `config` folder, where `STServer.ini` is located.
11. Open the `STServer.ini` and change `bEnableModcheck` from `false` to `true`
12. Save the file
13. Run `SkyrimTogetherServer.exe` again
14. It should now say `ModPolicy is active` and your mod policy will now be enforced.

![](https://sxcu.net/5BP1nld8D.gif)

#### Onwards to the next step!
