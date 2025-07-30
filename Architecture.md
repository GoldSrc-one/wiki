[Go back to index](README.md)

#

# Architecture

CrossPlay is technically a GoldSrc game.
- it sits in a subfolder
- it is launched with the `-game crossplay` parameter/argument
- it has a `liblist.gam` file and a `.dll` in `dlls\`
- it has its own configs, `motd.txt` and so on

But it is a "meta" game. It uses the dlls from the other games to make the magic happen.
The games are specified with the `-xgameX` parameter.

In addition the the dlls, it uses `gamedata`. It is a directory with contains information about the game dlls, very similar to the one you would find in `amxmodx\data`.

One last critical component is the `crossplay.smc` file which contains configuration for each game. Please see [Configuration](Configuration.md) for more details.

After launching the CrossPlay server a `models` folder will be created. It will contain converted player models. So far there are three version of each model.
- 2WB version (HL, OP4, DMC, TFC)
- CS version (CS, CZ)
- DOD version (DOD)

The `models` folder also contains models which have confliting names. For example `p_knife.mdl` from CS vs `p_knife.mdl` from DMC.
