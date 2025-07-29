index link

#

# Scripting

The CrossPlay AMXX is not what you are used to from CS. As mentioned in the Architecture chapter, CrossPlay acts as a new game. You cannot use game specific modules or access pdata.

If you wish to interact with entities, you have to get into the game context.

## Game context

Game context is a concept in CrossPlay. It lets you act as you are now in CS/HL/...

For example, if you with to spawn an entity from HL, you do

```
#include "crossplay"
new gameId = GetGameId("valve");
GameContext(valveId, "MySpawnFunction");
...
public MySpawnFunction() {
  create_entity("monster_zombie");
}
```

## Examples

See the *scripting*
