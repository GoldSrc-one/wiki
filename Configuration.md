[Go back to index](README.md)

#

# Configuration

## crossplay.smc

This file contains the core settings for each game. You don't need to touch it unless you want to have different player models.

### Player models

For example to change what HL player models will be on the CT side, edit the games/valve/teams/CS list. Separate the model names by a semicolon.

To change what OP4 player models will be available in the deathmatch, edit the games/gearbox/teams/UNASSIGNED list.

After changing the file, restart the server (close and start again). The server will regenerate the missing converted models.

### Others

Don't touch the other settings.

## game_{gamedir}.cfg

If you wish to have some specific configuraiton on CS/HL/... maps, just go to game_{gamedir}.cfg

For now, there is a specific config for CS maps in `game_cstrike.cfg` and for the other maps there is `game_deathmatch.cfg`

