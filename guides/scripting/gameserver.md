# GameServer

GameServer is a singleton instance. To fetch use, use the following lua:

```lua
local gameServer = GameServer:get()
```

**Interact with the GameServer** After obtaining the game server instance, you can call methods from the `GameServer` class using the dot (.) notation. For example:

```lua
gameServer:Kill(playerId)
gameServer:Kick(playerId)
local serverTick = gameServer:GetTick()
```

**Send a chat message** To send a chat message from the server to a specific player, use the `SendChatMessage` method:

```lua
local connectionId = 1 -- Replace this with the target player's connection ID
local message = "Hello from the server!"
gameServer:SendChatMessage(connectionId, message)
```

Note that the message will be automatically sanitized to remove any HTML tags.

