# Features

## Implemented features

### NPCs

NPCs and monsters are fully synced, including dragons. Some random encounters, like prisoners being escorted or hunters roaming around, may not always appear in everyone's world. All important NPCs and monsters are synced in terms of animations, position, combat and death state.

### Quests

Quests are fully synced. Make sure to check out the playguide in the sidebar to have a good experience.

### Dialogue

Dialogue of NPCs is synced by the party leader. If an NPC talks on the party leader's client, that same NPC will say the same thing on other people's games. Their subtitles are also synced. Whenever the party leader makes a dialogue choice, the choice will be displayed in the chat and as a small pop up in the bottom left corner.

### Inventories and equipment

Both player and NPC inventories and equipment are fully synced. Chest contents are also synced. Players can look at the same chest at the same time, and loot/store items similarly. Enchanted and poisoned items are synced. Pickpocketing is synced as well, including pickpocketing fellow players. Dropping items on the ground is synced. Picking up items is not always synced.

### Death

When the player dies, it does not reload a save anymore. Instead, if the player dies outside, it will spawn nearby, similarly to GTA Online. If the player dies in a dungeon or another type of interior, they will respawn at the entrance of that dungeon/interior. On death, the player automatically pays all their crime bounties, and will therefore lose aggro from guards and such if they had any. There is an optional server option where the player loses a percentage of their gold. This can be configured in the server's `settings.ini` file.

### Difficulty

The difficulty is determined by the server. This can be configured in the server's `settings.ini` file. The default is "expert" difficulty. We recommend that you use a high difficulty, since the game was not balanced for multiple players. If the game is still too easy, you can install difficulty mods. As always, make sure everyone installs the same mods for the best experience.

### Pausing

We disabled pausing for certain menus, like inventory, magic selection, favorites selection, the console, and looting. Some menus still do pause, like the map, quest journal/settings/save menu, skill tree menu, barter menu, etc.

### PvP

PvP is default disabled, but can be enabled through the server's `settings.ini` file. This is a co-op mod first and foremost, hence why it is disabled by default. We did not build the mod with PvP in mind, and PvP'ing will therefore not be perfect.

### Projectiles

Projectiles like arrows and firebolts are fully synced.

### Magic

Magic spells and effects are fully synced. You cannot use AI driven spells like "fear" on other players. Effects like "slow time" are also synced.

### **Locks and lock picking**

Locks are synchronized, meaning that you can break out of jail with your friends! Same goes for doors, chests and more. If an NPC or player opens a door with a key, it will be open for everyone.

### Horses

Horse mounting is synced. The animation of the horse might be stuck for other players when a player mounts it. This can usually be fixed by having the rider jump with the horse a few times.

### XP sync

The XP sync system attempts to emulate the natural level progression of the game. Whenever someone in your party gains experience in a **combat skill**, the rest of the party will get the same amount of experience in their respective **combat skills**. This goes for combat skills only, so not for smithing for example. As an example: if party member 1 hits a wolf with a one-handed sword and gets 5 xp in he one-handed skill tree, and party member 2 last used a destruction spell as combat skill, party member 2 will get 5 xp in destruction.&#x20;

### Puzzles

Most puzzles are synced, for example the dragon claw door.

### Stealth

Stealth is synced. The AI detection for other players is disabled. This means that you cannot be detected by your fellow players.

### Vampire lord/werewolf

Beastforms (vampire lord and werewolf forms) are fully synced, both in transformation, animations, combat, and transforming back to a normal human being.

### Time

The server runs the world time. On connect, the local time will sync up to the server time. You cannot progress the time by waiting or sleeping.

### Homes

Vanilla homes are not synced, but this is intentional. This way, players can customize their own homes however they like, and they can store items in their chests without having to be afraid of the chest contents getting overwritten by other players (since only these chests do not sync). This only goes for vanilla homes, not for DLC homes or modded homes. These homes are Breezehome, Hjerim, Honeyside, Proudside Manor and Vlindrel Hall.

### Followers

We recommend that you do not use followers unless it is for a quest. The AI of the follower is determined by who hosts that follower, and so the follower may just randomly decide to walk away. Besides, a party with multiple dragonborns is already strong enough. Followers are not necessary.

### Actor values

Actor values like health, stamina and magicka are all synced.

### Mod policy

The server has an optional setting that enforces a mod policy. This means that everyone on the server must have the same mods installed in the same load order. Having the same mod lists on every client ensures the most stable experience. This can be enabled through the server's `settings.ini` file.

## Unimplemented features

### Player map markers/waypoints

This feature is pretty much finished, but there was no time to test it before 1.0. This feature will come in an update in the near future.

### Weather

Weather is planned to be synced later.

### Scripting API

We would like to create a scripting API that modders can use to customize their servers, create Skyrim Together specific mods, or develop scripts to make existing mods more compatible.
