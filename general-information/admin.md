# Admin

{% hint style="danger" %}
Admin features are only available in Skyrim Together Reborn version 1.6.8+
{% endhint %}

{% hint style="warning" %}
Admin privileges are automatically removed&#x20;
{% endhint %}

## Join as admin

The `STServer.ini` file includes a field called `sAdminPassword` in the `[GameServer]` section. You can set a password here that users need to enter in the Connect window to join as an admin. If you don't set a password, no one will be able to join as an admin.\
ex. `sAdminPassword=password` -> admin password = `password`



## Add admin

You need access to the server console for this. Use the `/AddAdmin` command in the console to make a player an admin. If the player with the specified name isn’t found, you'll see a warning in the console.\
ex. `/AddAdmin SkyrimTogether` -> adds the player "SkyrimTogether" as an admin



## Remove admin

{% hint style="info" %}
Admin privileges are automatically revoked when the admin leaves the server
{% endhint %}

You need access to the server console for this. Use the `/RemoveAdmin` command in the console to make a player an admin. If the player with the specified name isn’t found, you'll see a warning in the console.\
ex. `/RemoveAdmin SkyrimTogether` -> removes admin privileges from player "SkyrimTogether"
