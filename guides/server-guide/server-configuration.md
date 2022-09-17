---
description: Everything you need to know about the configuration file
---

# Server configuration parameters

To configure the server, simply go to the folder where Skyrim Together is installed, then go into the `config` folder and open `STServer.ini`. Here, you can configure all the server settings. Alternatively, you can use the command line in the server console when you have opened the server. Use /help to display all the possible commands.

{% hint style="info" %}
If you want to restore config defaults, simply close the server, delete `STServer.ini`, and start the server again.
{% endhint %}

### sLogLevel

#### Description

This is used to configure the logger in the server console. This option currently does not work.

#### Options

| Option | Description                                     |
| ------ | ----------------------------------------------- |
| info   | Displays all logged information                 |
| warn   | Displays warnings and critical information only |
| error  | Displays critical information only              |

### bConsole

#### Description

Determines whether the interactive console is enabled or not.

#### Options

Can be set to `true` or `false`.

### bAnnounceServer

#### Description

Determines whether the server shows up on the server list or not. If the server has a password, it will not show up on the server list.

#### Options

Can be set to `true` or `false`.

### fGoldLossFactor

#### Description

Used to determine how much gold a player loses when they die. When set to 0, players will not lose any gold.

#### Options

This is a factor. It can be set to anything between 0 and 1. For example, if you want the player to lose 5% of its gold on death, set it to 0.05.

### bEnableItemDrops

#### Description

Disabling this will make it so that dropping items in the world is not synced. Dropping items has caused crashes in the past, and picking them up is often not synced anyway, so we recommend you keep it at the default, which is "off".

#### Options

Can be set to `true` or `false`.

### bEnableXpSync

#### Description

Determines whether the xp sync system is enabled or not.

#### Options

Can be set to `true` or `false`.

### uTimeScale

#### Description

Determines how fast the time in Skyrim progresses.

#### Options

Can be set to a number between `0` and `1000`.

### bEnableDeathSystem

#### Description

Determines whether the Skyrim Together Reborn custom death system is enabled. This should ONLY be turned off if you know what you're doing, and if you have a suitable death mod that replaces the mechanics. Reloading old saves every time you die **will** cause issues.

#### Options

Can be set to `true` or `false`.

### bSyncPlayerHomes

#### Description

Determines whether chests in player homes are synced. Beware that long term storage is not consistent in Skyrim. By default, this option is disabled so that players can use their homes to safely dump items in their chests as a form of long term storage.

#### Options

Can be set to `true` or `false`.

### bEnablePvp

#### Description

Determines whether players can damage each other. Shouts on other players, like fus ro dah, also only work when this option is enabled.

#### Options

Can be set to `true` or `false`.

### bEnableGreetings

#### Description

In the base game, when you walk close to an NPC, they start talking to you with random dialogue. During testing, we found this to be quite annoying when dialogue sync was implemented. Therefore, we decided to disable those greetings. You can enable this again if you'd like through this setting.

#### Options

Can be set to `true` or `false`.

### uDifficulty

#### Description

This sets the server side difficulty, which is enforced on **all** clients.

#### Options

| Option | Description |
| ------ | ----------- |
| 0      | Novice      |
| 1      | Apprentice  |
| 2      | Adept       |
| 3      | Expert      |
| 4      | Master      |
| 5      | Legendary   |

### bAllowMO2

#### Description

Sets whether the client is allowed to use mod organizer 2.

#### Options

Can be set to `true` or `false`.

### bAllowSKSE

#### Description

Sets whether the client is allowed to use SKSE.

#### Options

Can be set to `true` or `false`.

### bEnableModCheck

#### Description

This is the mod policy feature, as descripted in the "**Features**" page. To use this, you must create a Data folder in the same place as where you run `SkyrimTogetherServer.exe`. This Data folder must contain a file called `loadorder.txt`, which contains the load order that you want to enforce for all users.

#### Options

Can be set to `true` or `false`.

{% embed url="https://wiki.tiltedphoques.com/tilted-online/guides/server-guide/windows-setup/regular-setup/explaining-benablemodcheck#what-does-benablemodcheck-do" %}

### sPassword

#### Description

This sets the password that players need to fill in when connecting to the server. Leave this blank if you do not want to set a password on the server. If you do set a password on the server, it will not show up in the serverlist, and people will have to connect manually.

### sAdminPassword

#### Description

Used for potential admin panels in the future. This option is currently unused.

### sServerName

#### Description

The name that shows up on the server list.

### bPremiumMode

#### Description

Determines the tickrate of the server. Most networks should be able to handle running a server with this option enabled.

#### Options

Can be set to `true` for a tickrate of 60 or `false` for a tickrate of 30.

### uMaxPlayerCount

The max number of players that can connect to your server.

### uPort

The port on which the server runs.
