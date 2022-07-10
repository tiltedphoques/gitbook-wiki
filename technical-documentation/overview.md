# Overview

Skyrim Together is based on a client-server architecture with the server being partially authoritative due to the lack of gameplay code and world representation server side at the moment.

The actual world state is driven by clients that become owners of cells and actors that they load.&#x20;

To understand this, you must first understand the two types of actors we manage, here "client" refers to a Skyrim instance, not to the generic concept of game client:

* `LocalActor` is an actor that is managed by the current client, we do not interfere with the behaviour of these actors. The client will send state changes (i.e. inventory, animation, position...) to the server that will then replicate those changes to other clients.
* `RemoteActor` is an actor that is not managed by the current client, it receives updates from the server and applies those state changes. We do interfere with local changes made to these actors by blocking them in the most part. Some changes such as health changes are not blocked and are sent to the server.

When the client loads an actor it will send a request to the server asking if it can start managing this actor, if the actor is already managed the actor becomes a `RemoteActor` , if not it becomes a `LocalActor`.

Internally we use an entity-component-system and add either a `LocalComponent` or a `RemoteComponent` to mark entities as being locally or remotely controlled.

### Entities

An entity is simply a unique number used to identify a resource and its associated components. The server and client both communicate using the server's entity numbers to identify entities.

### Components

Components are data structures that we can associate with an entity, for example we could associate an `InventoryComponent` to an entity that has an inventory, like actors and chests.
