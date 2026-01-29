---
description: Frequently tested function archetypes when making tweaks or testing changes to Skyrim Together.
---

# Smoke test the features and quests in order of importance

### 1: Booting the game with known addons hooked

A: Address Library 1.6 booting Skyrim Together with Vortex and Mod Organizer 2 should be tested. Known addons that are good to test boot with are Skyrim Script Extender AE, Crashlogger SSE AE VR - PDB support, Engine Fixes 7, and Skyrim Souls RE Updated. A good way to detect if there has been a regression in boot loading is to add Upscaling - Community Shaders. 

{% hint style="warning" %}
Expected: All plugins, including Skyrimtogether.esp, are loaded and usable
{% endhint %}

### 2: Loading a character with all vanilla items

A: If you can reach the main menu successfully, the next step is to open the console and reach gameplay. Press the console key and type "coc qasmoke" to load the test room, and make sure normal movement and menu UI interactions work. Make a savegame. Press F2 and connect to a localhost server and make a party. Now boot a second instance of the game and connect to the same room with the same character. Verify your local server config's party join setting is adhetered to and compare the players' equipped items and movement syncing.

{% hint style="warning" %}
Expected: All worn equipment and character movements are visibly synced
{% endhint %}

### Q: Where can I report bugs and request features?

A: You can submit bugs and feature requests at our code repository [here](https://github.com/tiltedphoques/TiltedEvolution/issues).

{% hint style="warning" %}
Expected: Check for duplicate bugs before reporting, help detail open bugs
{% endhint %}

### 3: Starting a new game and smoke test quest start

A: If you want to, you can use the console to "coc riverwood". It is important that at least one player uses the new game option from the main menu, and plays offline until they complete the Helgen Cave. Once you have both players ready, party up and teleport to the Riverwood player and enter the Riverwood trader house. Have either player start the quest about the golden claw, and observe if both players see Camilla exit the house and point them towards Bleak Falls Barrow. This concludes the first test of quest start propagation.

{% hint style="warning" %}
Expected: Party leader selected dialogue replies play for both players and is printed to the server console. The quest is added to the party members and they see Camilla synced.
{% endhint %}

### 4: Entering Bleak Falls and testing quest items

A: Reach [BleakFallsBarrow01](https://elderscrolls.fandom.com/wiki/Bleak_Falls_Barrow_(Location)) and complete it with 2 players in a party. The important thing to test is freeing the NPC Arvel the swift, taking his golden claw, verifying that both players get it put in their inventory, and that both players can collaborate with the revolving pillars, levers and dragon door puzzles in the dungeon. At the end of BleakFallsBarrow02 both players should receive a Dragon Stone, regardless of who loots the Draugr boss at the Word Wall.

{% hint style="warning" %}
Expected: Both players get to see Arvel freed. Both players get the claw quest item and can use the dragon claw door. Both players can use levers and puzzle pillars in alternating order. Both players get the dragon stone and Fus word.
{% endhint %}

### 5: Testing from Dragonsreach, Way of the Voice

A: This quest has a unique transition that we needed to update 1.8 to handle correctly. Go with the party to WhiterunDragonsreach and turn in the Dragon stone item after talking to the Jarl. Follow the NPC conversations, go upstairs and get the quest to kill a dragon at the watchtower. Once you have travelled to the watchtower and killed the dragon, make a save and head towards whiterun stables. Verify that your quest still requires you to return to the Jarl, and that you don't get an item reward when the Greybeard's voice plays.

{% hint style="warning" %}
Expected: The dragon stone is returned to Farengar, the dragon appears and can positionally sync, and dies at the same time for both players. Regardless of shouting or not, both players have to return to the Jarl to get the quest reward named weapon of Whiterun.
{% endhint %}

### 6: Testing meeting the Greybeards at 7000 steps

A:  Reach HighHrothgarOutside and enter the door. Talk to the NPC inside and demonstrate your shouts. Partake in the FUS RO trial, then go outside and get the Whirlwind Sprint shout and the Horn of Jurgen Windcaller quest start. Both players should progress well.

{% hint style="warning" %}
Expected: The ghost dummies may remain visually, but functionally the players should be able to complete this according to the playguide.
{% endhint %}

### 7: Testing the Blade in the Dark Ustengrav note

A: At the end of the Ustengrav02 dungeon, the players should both see a note in the room meant for the Horn of Jurgen Windcaller. Both players should read the note and see if their quests have the same status after. Which is Meet whoever took the horn in Riverwood.

{% hint style="warning" %}
Expected: The players can rent the attic room from Delphine after using the note. This is important to test because an earlier build had a duplicate quest propagation issue which blocked the players from proceeding the main quest after reading the note in a party.
{% endhint %}

### 8: Testing the dragon's revival near Kynesgrove

A: Some players experience bugs when the dragon is revived near Kynesgrove, sometimes Alduin becomes angry and starts meteors, or doesn't fully transition to waking the dead dragon from the ground. The dragon may revive from elsewhere and appear in weird animation.

{% hint style="warning" %}
Expected: Alduing settles in the sky and revives the dead dragon, the skeleton comes up from the burial spot and transitions to the alive dragon texture. The players can defeat the revived dragon and talk to Delphine after to complete [A blade in the Dark](https://elderscrolls.fandom.com/wiki/A_Blade_in_the_Dark) quest.
{% endhint %}

### 9: Testing the Thalmor Embassy quest completion

A: When you return the Horn to Arngeir, both players should be able to get their final word of the FUS RO DAH shout. After that, find Delphine in Riverwood and discuss infiltrating the Thalmor. Meet Malborn in Solitude and smuggle some items in. Then exit to the Solitude stables and make a save. Have both players take the horse cart to the Thalmor Embassy and try to complete the quest without crashing. Get the note about Esbern near the jail cells and exit the area.

{% hint style="warning" %}
Expected: The players should not crash when arriving to the Embassy, and should get the same quest updates during the infiltration.
{% endhint %}

### 10: Testing Companions scenes and misc quest jobs

A: When you join the Companions in Whiterun, either player should be able to hit Farkas in the courtyard brawl until he is at 3 hits. Then you will be allowed to take his sword to Eorlund the blacksmith, and a shield to Aela. It is important to note if the brawl in Jorrvaskr doesn't complete and Skjor is stuck watching the combatants upstairs. This is a common Companion's Alternate Start bug, and to resolve it you must bash either combatant to unstuck the NPC. Then you can wait for Skjor to go downstairs and meet Aela to have the scene there progress properly before you give her the shield.

Note: Depending on your Skyrim questing logic, the random objective between getting a bed in Jorrvaskr, and getting the Proving Honor quest to clear Dustman's Cairn, may be randomized and should complete when either player completes their individualized objective.

{% hint style="warning" %}
Expected: When the players return from the DustmansCairnExterior01 quest and have the fragments of Wuuthrad, even if they enter the circle of companions outside Jorrvaskr a bit offset in time (say 10 seconds), the scene should play out and the involved players should regain controls after. This was verified up to 1.8.0.4.
{% endhint %}

### Q: What other content can be regression tested?

A: The content outside of this smoke test guide can be detailed in this Testing-guide section, with more detailed steps and articles.
