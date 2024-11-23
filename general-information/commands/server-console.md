# Server Console

{% hint style="warning" %}
The command "SetDate" is only available in Skyrim Together Reborn version 1.6.x+
{% endhint %}

<table data-full-width="true"><thead><tr><th width="161">Command</th><th width="174">Parameter</th><th width="425">Description</th><th>Example</th></tr></thead><tbody><tr><td>uptime</td><td></td><td>Show how long the server has been running for</td><td></td></tr><tr><td>players</td><td></td><td>List all players on this server</td><td></td></tr><tr><td>mods</td><td></td><td>List all installed mods on this server</td><td></td></tr><tr><td>resources</td><td></td><td>List all loaded resources on the server</td><td></td></tr><tr><td>quit</td><td></td><td>Stop the server</td><td></td></tr><tr><td>admins</td><td></td><td>List all admins</td><td></td></tr><tr><td>SetTime</td><td>0-23 0-59</td><td>Set in-game hour and minute</td><td>/SetTime 9 30</td></tr><tr><td>SetDate</td><td>0-max 0-12 0-999</td><td>Set in-game day, month, and year</td><td>/SetDate 28 2 100</td></tr><tr><td>AddAdmin</td><td>player_name</td><td>Grants admin privileges to specified player</td><td>/AddAdmin SkyrimTogether</td></tr><tr><td>RemoveAdmin</td><td>player_name</td><td>Revokes admin privileges from specified player</td><td>/RemoveAdmin SkyrimTogether</td></tr></tbody></table>

{% hint style="warning" %}
The player\_name parameter given of the "AddAdmin" and "RemoveAdmin" commands will replace an underscore with a space\
ex. "/AddAdmin Skyrim\_Together" -> adds the player "Skyrim Together" as an admin
{% endhint %}

{% hint style="info" %}
The day parameter of the command "SetDate" follows the normal day count in a month:

31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31
{% endhint %}
