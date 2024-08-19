# GameServer

GameServer is a singleton instance. To fetch use, use the following lua:

```lua
local gameServer = GameServer:get()
```

**Interact with the GameServer** After obtaining the game server instance, you can call methods from the `GameServer` class using the colon operator (:) . For example:

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

***

<table data-full-width="true"><thead><tr><th>Name</th><th>Description</th><th>Usage</th></tr></thead><tbody><tr><td>get()</td><td>Get the GameServer instance</td><td>GameServer:get()</td></tr><tr><td>Kill()</td><td>Shut down server</td><td>GameServer:get():Kill()</td></tr><tr><td>Kick(ConnectionId)</td><td>Kick the player with the given Connection Id</td><td>GameServer:get():Kick(player:GetConnectionId())</td></tr><tr><td>GetTick()</td><td>Get the server's current tick value</td><td>GameServer:get():GetTick()</td></tr><tr><td>SendChatMessage(ConnectionId, string)</td><td>Send a message to the given Connection Id</td><td>GameServer:get():SendMessage(player:getConnectionId(), "This is a message")</td></tr><tr><td>SendGlobalChatMessage(string)</td><td>Send a message to all connected players</td><td>GameServer:get():SendGlobalChatMessage("This is a global message")</td></tr><tr><td>SetTime(int hours, int minutes, float timeScale)</td><td>Set the world's time to the specified hour and minutes at the given time scale (default time scale is whatever the current world time scale</td><td>GameServer:get():SetTime(11, 15, 20)<br>-- Set time to 11:15 AM at a time scale of 20</td></tr></tbody></table>

{% hint style="info" %}
NOTE: `SendChatMessage` and `SendGlobalChatMessage` are automatically sanitized to remove any HTML tags
{% endhint %}

## Example

```lua
local gameServer = GameServer:get()

addEventHandler("onPlayerQuit", function(entityId)
  gameServer:SendGlobalChatMessage("Someone left, server sad, server close :(")
  gameServer:Kill()
end)

addEventHandler("onSetTime", function(hours, minutes, timeScale)
  gameServer:SendGlobalChatMessage("Time set to " .. hours .. ":" .. minutes .. " at time scale of " .. timeScale)
end)

addEventHandler("onChatMessage", function(entityId, message)
  local player = getPlayer(entityId)
  if not player then
    return
  end
  
  if(string.find(message, "a") then
    gameServer:SendMessage(player:GetConnectionId(), "Your message contains an a, you're kicked")
    gameServer:Kick(player:GetConnectionId())
  end
end)
```
