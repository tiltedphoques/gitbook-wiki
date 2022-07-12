# Explaining bEnableModcheck

### What does `bEnableModcheck` do?

The parameter `bEnableModcheck` can enable or disable the possibility of enforcing a mod policy.

If you **enable** `bEnableModcheck`, that means that everyone connecting to your server will go through this process:

1. Player A connects to your server, that has **enabled** modcheck
2. Your server will check Player A's `loadorder.txt`
3. If the `loadorder.txt` matches the one on the server, Player A will now join your server
4. If the `loadorder.txt` **doesn't** match the one on the server, Player A will not be allowed to join the server.



If you **disable** `bEnableModcheck`, that means that everyone connecting to your server will go through this process:

1. Player A connects to your server, that has **disabled** modcheck
2. Your server will not check Player A's `loadorder.txt`
3. The player will be allowed to join, even though you play with different mods

The reason why it can be good idea to enable this, is to increase chances of having a more stable gaming session and/or playthrough.

It is **not** necessary to use, if you and your friends are playing **without** mods (or if you're just playing with `Address Library for SKSE`)



### Oh! I want that! I want my server to kick players, that doesn't use the mods that I choose!

Alright. For that, we need to get your `loadorder.txt` from MO2 and put it in the right location.

1. Open MO2
2. Enable the mods you want to enforce.
3. **Make sure** they're in the load order that you want to enforce.
4. In my case, I only have 3 mods, so it'll look like this:

![](https://shx.is/5BAiKMkPL.png)

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

![Here's the whole process of how to do it](https://shx.is/5BAmnL9Ni.gif)

### Onwards to the next step!
