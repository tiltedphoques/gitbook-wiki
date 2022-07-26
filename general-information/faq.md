---
description: Frequently asked questions about Skyrim Together Reborn and Fallout Together.
---

# FAQ

### Q: What is Skyrim Together Reborn?

A: Skyrim Together is a Skyrim mod that aims to bring co-op to the game. Skyrim Together Reborn is essentially a "sequel" to the original Skyrim Together (which some of you may know as "Harbor Edition", "Nightlies", or simply "Old ST").&#x20;

The code was rewritten from the ground up because the old codebase was too difficult to work with. This decision has paid off big time, as Skyrim Together Reborn is significantly better than the original Skyrim Together. The current list of features can be found [here](features.md).

### Q: What platforms and versions are supported?

A: Skyrim Special Edition on Steam, specifically version 1.6, is the **ONLY** version that is supported and will most likely always be supported. This has been mislabeled as "Anniversary Edition" by the modding community. The Anniversary Edition is a combination of the Special Edition and the Anniversary Upgrade. This is not required to play Skyrim Together Reborn. You only need to purchase the Special Editio.

The VR, console, legendary edition (aka Oldrim), and the gamepass version are not supported and will never be.

### Q: Where can I report bugs and request features?

A: You can submit bugs and feature requests at our code repository [here](https://github.com/tiltedphoques/TiltedEvolution/issues).

### Q: What is the recommended amount of players?

A: While there is no hard player count limit in theory, we recommend that you play with 2 to 8 people for the best experience.

### Q: What is the current status of Fallout Together?

A: When developing Skyrim Together Reborn, the developers decided to make the mod work with Fallout 4 too. At the start of 2022, we decided to focus on Skyrim Together Reborn entirely due to time constraints and the small size of the team. We said that we would finish Fallout Together after Skyrim Together Reborn was released.

There is currently only one developer on the team who is interested in finishing Fallout Together (see [Q: will the mod get future updates?](https://wiki.tiltedphoques.com/tilted-online/general-information/faq#q-will-the-mod-get-future-updates)). Even for this developer, this is most likely too big a task. If Fallout Together is to be completed, more developers need to pitch in. We hope that going open source brings in more people to help with that.

### Q: Can I use other mods with this mod?

A: Our official position is that you **should not** install any other mods for the best, most stable experience. You can still do so, and our mod also loads SKSE if you have it installed, but we cannot guarantee that these mods will not cause stability issues, will play nice with our systems, or that their features will sync. This is entirely up to you.&#x20;

Creation Club mods, including the Anniversary Upgrade mod pack, are included in this category.

{% hint style="warning" %}
We did not build Reborn with the Anniversary Upgrade mod pack in mind. For the most stable experience, you should [disable the mods](../guides/client-setup/initial-setup/launching-the-game.md#making-sure-anniversary-upgrade-dlc-is-disabled) that come with the paid Anniversary Upgrade mod pack.
{% endhint %}

### Q: Will X mod work with this mod?

A: We have no idea which mods work well with Skyrim Together Reborn. There are no mods that are explicitly synced. Mods only sync by accident. The only way to find out if a mod syncs is to test it. Graphics mods generally work well. Aside from that, it's difficult to say. If you have SKSE installed, our mod will automatically load it. We have a mod tracker where you can check and submit mod compatibility. You can find it [here](https://github.com/tiltedphoques/Mod-Compatibility). We have blocked a few mods because they are inherently incompatible:

* Engine fixes
* Skyrim Souls RE
* Fraps (not a mod, but also blocked)

### Q: Will the mod get future updates?

A: Skyrim Together Reborn 1.0 is a solid base for a lot of future expansion. The current development team has put in a lot of work. Unfortunately, they cannot keep working at this pace. That is why the mod has become open source. We hope that new developers will join in the future to help this mod reach new heights.&#x20;

There is still a lot of work to be done, such as creating a scripting API, adding features like weather sync, fixing bugs and crashes, smoothing out quests, and finishing Fallout Together.

The current development team will continue to maintain the codebase, guide new developers, and build new features (if they feel like it).

### Q: Is there some place where I can donate money to the project?

A: We currently do not take donations. This may change in the future.

### Q: What operating systems are supported?

A: For the mod itself you will need Windows 8.1 or higher. Linux support will be something that will have to be done by the community on our GitHub. The server runs on both Windows and Linux.

AES-NI support is also required on your CPU. Check [this page](../guides/troubleshooting/my-game-crashes-when-i-open-it-or-connect-to-a-server.md) to see if your CPU is compatible.

### Q: What is Tilted Online?

A: Tilted Online is the name of the codebase of both Skyrim Together Reborn and Fallout Together.
