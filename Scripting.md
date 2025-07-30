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
  create_entity("monster_zombie");
  ...
}
```

## Examples

See the [scripting repository](https://github.com/GoldSrc-one/scripting)
