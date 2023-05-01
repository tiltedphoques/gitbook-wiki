# Components

The Server achitecture uses components, since it is based on an ECS (Entity Component System) architecture.

In simple terms, imagine a video game world with many characters, items, and environmental objects. Each of these objects can have different attributes and behaviors, such as appearance, movement, health, and interactions with other objects. In a traditional programming approach, managing all these objects and their interactions can become complex and difficult.

Now, lets focus on components: Components are the attributes or properties of an entity. For example, a character entity may have components like position, health, and inventory. Components are designed to be small and reusable, which means they can be easily combined and shared between different entities.

Currently only the movementcomponent is exposed:

To get the `MovementComponent` instance for an entity, use the following Lua code:

```lua
local entity = ... -- Replace this with the target entity
local movementComponent = GetMovementComponent(entity)
```

**Interact with the MovementComponent** After obtaining the movement component, you can access its properties using the dot (.) notation. For example:

```lua
local position = movementComponent.Position
local rotation = movementComponent.Rotation
local direction = movementComponent.Direction
local sent = movementComponent.Sent
```

