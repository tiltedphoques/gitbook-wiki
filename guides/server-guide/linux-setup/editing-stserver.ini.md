# Editing STServer.ini

### First look at `STServer.ini`

The default `STServer.ini` config file will look like this:

```
[general]
sLogLevel=info
bConsole=true


[LiveServices]
bAnnounceServer=true


[Gameplay]
fGoldLossFactor=0
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
uPort=10578
```

To read about what each specific line does, I will refer to [this page](../server-configuration.md) that explains every parameter available in depth.

I will, in the next page, explain what the `bEnableModCheck` is about, and how to configure that properly.

### Example of how a config file can look

I'll give you an example of how a config file can be setup. I will again refer to [this page](../server-configuration.md) if you need more explanation of the parameters. I think it's pretty straight forward.

```
[general]
sLogLevel=info # Logs everything
bConsole=true # Enables interactive console is enabled or not


[LiveServices]
bAnnounceServer=true # Makes it show on the global server list


[Gameplay]
fGoldLossFactor=0 # Disables players losing gold on deaths
bEnablePvp=true # Enables PVP
bEnableGreetings=false # Disables NPCs greeting
uDifficulty=5 # Setting the difficulty level at Legendary


[ModPolicy]
bAllowMO2=true # Allows using ModOrganizer2
bAllowSKSE=true # Allows SKSE
bEnableModCheck=false # Disables verifying connecting users loadorder.txt (more on that later)


[GameServer]
sPassword=mySuperServerPassword # Setting the password to mySuperServerPassword
sAdminPassword=thisdoesntmatter # Setting the admin password to thisdoesntmatter
sServerName=My Very Best Server # Setting the server name to be "My Very Best Server"
bPremiumMode=true # Setting the tickrate to 60
uPort=10578 # Setting the port to 10578 (important!)
```

### Onwards to learn about the `bEnableModCheck`!
