[Go back to index](README.md)

#

# Scripting

The CrossPlay AMXX is not what you are used to from CS. As mentioned in the Architecture chapter, CrossPlay acts as a new game. You cannot use game specific modules or access pdata.

If you wish to interact with entities, you have to get into the game context.

## Game context

Game context is a concept in CrossPlay. It lets you act as you are now in CS/HL/...

For example, if you with to spawn an entity from HL, you do

```pawn
#include "crossplay"

new g_valveId = -1;

public plugin_init() {
  ...
  g_valveId = GetGameIndex("valve");
  register_clcmd("zombie", "ZombieMaker");
}

public ZombieMaker(playerId) {
  GameContext(g_valveId, "ValveZombieMaker");
}

public ValveZombieMaker() {
  var zombie = create_entity("monster_zombie");
  ...
}
```

## Entity ownership

Another concept is entity ownership. Each entity has an assigned "owner" -- the game in which the entity belongs.

For example when you connect from cstrike and your player entity id is 1, this should be true:
```pawn
GetEntityOwner(1) == GetGameIndex("cstrike")
```
Of course this code doesn't make much sense, you would put it inside an if statement for example. You would also store the game index beforehand for better performance.

Another example, if you created that entity using that code above, this would be true:
```pawn
GetEntityOwner(zombie) == g_valveId
```

Nesting these functions allows you to simply do `GameContext(GetEntityOwner(entity), "MyCallback");` to enter the game context of the given entity.

## Examples

See the [scripting repository](https://github.com/GoldSrc-one/scripting)
