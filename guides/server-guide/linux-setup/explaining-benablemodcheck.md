# Explaining bEnableModcheck

## What does `bEnableModcheck` do?

The parameter `bEnableModcheck` can enable or disable the option of enforcing a mod policy.

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

## Oh! I want that! I want my server to kick players, that doesn't use the mods that I choose!

Alright. For that, we need to get your `loadorder.txt` . If you use a Linux server to host, but a Windows PC to play Skyrim, you can use [this page](../windows-setup/zerotier-setup/explaining-benablemodcheck.md#oh-i-want-that-i-want-my-server-to-kick-players-that-doesnt-use-the-mods-that-i-choose), to grab your `loadorder.txt` from MO2 or VMM and then use that.

1. Put your `loadorder.txt` in the `/opt/docker/skyrimserver/Data` directory.
2. Edit your `STServer.ini` using `nano`, e.g. `nano /opt/docker/skyrimserver/config/STServer.ini`
3. Find `bEnableModCheck` and set it to `true`.
4. Close and save the file by pressing `CTRL-X` and then `Y` and then `Enter`.

#### Onwards to the next step!
