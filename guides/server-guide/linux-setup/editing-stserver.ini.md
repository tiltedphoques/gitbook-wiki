# Editing STServer.ini

## First look at `STServer.ini`

The default `STServer.ini` config file will look like this:

```
[general]
sLogLevel=info
bConsole=true


[LiveServices]
bAnnounceServer=false


[Gameplay]
bEnableMiscQuestSync=false
fGoldLossFactor=0
bAutoPartyJoin=true
bEnableItemDrops=false
bEnableXpSync=true
bSyncPlayerCalendar=false
uTimeScale=20
bEnableDeathSystem=true
bSyncPlayerHomes=false
bEnablePvp=false
bEnableGreetings=false
uDifficulty=4


[ModPolicy]
bAllowMO2=true
bAllowSKSE=true
bEnableModCheck=false


[GameServer]
sPassword=
sAdminPassword=
sServerName=Dedicated Together Server
bPremiumMode=true
uMaxPlayerCount=8
uPort=10578
```

To learn more about what each line does, visit [this page](../server-configuration.md), which goes over each parameter in detail.

On the following page, the guide will explain what the `bEnableModCheck` is and how to properly configure it.

#### Onwards to learn about the `bEnableModCheck`!
