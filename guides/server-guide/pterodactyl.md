---
description: How to run Skyrim Together via Pterodactyl
---

# Pterodactyl

Visit the following Page for more information and for the download.&#x20;

{% @github-files/github-code-block %}

{% embed url="https://pterodactyl.io/project/introduction.html" %}

{% hint style="warning" %}
The guide uses the tag "latest" for the server which potentially isn't what you want.

Check the file "egg-tilted-evolution.json" for the word "docker\_images". \
Here "latest" is mentioned twice which needs to be changed to the desired version e.g. "1.5.0". Available versions can be found here [https://hub.docker.com/r/ad3m3r5/tiltedevolution-pterodactyl/tags](https://hub.docker.com/r/ad3m3r5/tiltedevolution-pterodactyl/tags)
{% endhint %}

{% hint style="info" %}
The following steps are the same as mentioned on the Github page.&#x20;
{% endhint %}

## Steps:

* Download the `egg-tilted-evolution.json` egg definition
* Adding the Nest & Egg
  * admin > Nests > **Create New**
    * Name: "Skyrim"
    * **Save**
  * admin > Nests > **Import Egg**
    * Egg File: `egg-tilted-evolution.json`
    * Associated Nest: "Skyrim"
    * **Import**
* Creating a Server
  * admin > "Servers" > **Create New**
    * Server Name: "Skyrim Together Reborn"
    * Server Owner: _desired user_
    * Memory: _desired memory allocation_
    * Disk: _desired disk space_
    * Nest: "Skyrim"
    * Egg: "Tilted Evolution"
    * **Create Server**
* Configuring the Server
  * Using the CLI:
    * Can be done while the server is running using the built in CLI commands.
    * This config will be saved to the `STServer.ini` file upon shutdown.
  * Using the `STServer.ini`:
    * Can ONLY be done while the server is shutdown
    * If done while running, the config will be overwritten with the running config
* Updating the Server
  * Pterodactyl should automatically pull the latest image when (re)starting the server

