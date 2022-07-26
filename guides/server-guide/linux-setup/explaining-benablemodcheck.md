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

Alright. We'll need your `loadorder.txt` for this. If you host on a Linux server, but play Skyrim on a Windows PC, you can use [this page](../windows-setup/regular-setup/explaining-benablemodcheck.md#oh-i-want-that-i-want-my-server-to-kick-players-that-doesnt-use-the-mods-that-i-choose) to get your `loadorder.txt` from MO2 or VMM and then use that.

1. Put your `loadorder.txt` in the `/opt/docker/skyrimserver/Data` directory.
2. Edit your `STServer.ini` using `nano`, e.g. `nano /opt/docker/skyrimserver/config/STServer.ini`
3. Find `bEnableModCheck` and set it to `true`.
4. Close and save the file by pressing `CTRL-X` and then `Y` and then `Enter`.

#### Onwards to the next step!
