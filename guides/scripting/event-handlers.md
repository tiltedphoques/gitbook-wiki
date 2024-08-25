# Event Handlers

<table data-full-width="true"><thead><tr><th>Name</th><th>Description</th><th>Usage</th></tr></thead><tbody><tr><td>onCharacterMove(int)</td><td>Called any time a character moves</td><td>addEventHandler("onCharacterMove", function(entityId)</td></tr><tr><td>onCharacterSpawn(int)</td><td>Called when any character spawns in </td><td>addEventHandler("onCharacterSpawn", function(entityId)</td></tr><tr><td>onCharacterDestroy(int)</td><td>Called when any character is destroyed</td><td>addEventHandler("onCharacterDestroy", function(entityId)</td></tr><tr><td>onPlayerJoin(int)</td><td>Called when a player joins the server</td><td>addEventHandler("onPlayerJoin", function(connectionId)</td></tr><tr><td>onChatMessage(int, string)</td><td>Called when a player sends a chat message</td><td>addEventHandler("onChatMessage", function(entityId)</td></tr><tr><td>onPlayerQuit(int, string)</td><td>Called when a player leaves the server</td><td>addEventHandler("onPlayerLeave", function(connectionId, reason)</td></tr><tr><td>onUpdate(float)</td><td>Called every server tick </td><td>addEventHandler("onUpdate", function(delta)</td></tr></tbody></table>

## Example

```lua
local playerMgr = PlayerManager:get()
local gameServer = GameServer:get()

function getPlayer(entityId)
  local players = playerMgr:GetAllPlayers()
  for k, player in pairs(players) do
    if player:GetCharacter() == entityId then
      return player
    end
  end
  return nil
end

addEventHandler("onUpdate", function(delta)
  print("This is called every tick")
end)

addEventHandler("onPlayerJoin", function (connId)
  local player = getPlayer(connId)
  if not player then
    return
  end
  gameServer:SendGlobalChatMessage(player:GetUsername() .. " joined the server")
end)

addEventHandler("onPlayerQuit", function(connId, reason)
  local player = getPlayer(connId)
  if not player then
    return
  end
  gameServer:SendGlobalChatMessage(player:GetUsername() .. " left the server")
end)

addEventHandler("onChatMessage", function(entityId, message)
  local player = getPlayer(entityId)
  if not player then
    return
  end
  print(player:GetUsername() .. ": " .. message)
end)

addEventHandler("onCharacterSpawn", function(entityId)
  local player = getPlayer(entityId)
  if player then
    return
  end
  gameServer:SendGlobalChatMessage("Non-player with ID " .. entityId .. " spawned")
end)

addEventHandler("onCharacterDestroy", function(entityId)
  local player = getPlayer(entityId)
  if player then
    return
  end
  gameServer:SendGlobalChatMessage("Non-player with ID " .. entityId .. " destroyed")
end)

addEventHandler("onSetTime", function(hours, minutes, timeScale)
  gameServer:SendGlobalChatMessage("Time set to " .. hours .. ":" .. minutes .. " at time scale of " .. timeScale)
end)
```
