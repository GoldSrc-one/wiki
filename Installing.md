[Go back to index](README.md)

# Installing

The CrossPlay project consists of many individual parts. There is a graphical installer to help you with that.

This page is here just to explain what all the individual options mean.

## The target directory

The default target directory is set to `c:\hlds`, but you can choose whichever dir you desire. Just don't get too crazy with spaces or special characters, I haven't really tested those.

The full installation will have around 3 GBs so don't point this to a floppy drive please.

## SteamCMD

SteamCMD is a Valve tool for installing HLDS (the server part for all GoldSrc games).
If you already have one installed, you can just point the installer to it, otherwise it will download one for you (into the `steamcmd` subdirectory).

## Counter-Strike

If you want crossplay with CS, check it.

### ReGameDLL_CS

The server uses a custom game dll. If you uncheck this, round end check will not work, bots will crash and deathmatch won't work.

## Condition Zero

You can uncheck this one to save space if you don't need assets from CZ.

You can connect from CZ even if you don't have CZ installed, you just won't be able to play CZ maps.

### ReGameDLL_CS

Once again, custom game dll, this time only necessary if you are going to crossplay with CZ directly. If you are going to crossplay with CS and use CZ assets, this is not needed.

## Half-Life

If you want crossplay with HL, check it.

### Metamod + jk_botti

If you with to have HL bots in the game, check it. This will install Metamod-R and custom version of jk_botti that understands CS gamestyle at least a little bit.

## Opposing Force

If you want OP4, check it.

### Metamod + jk_botti

Same as above

## Deathmatch Classis

If you want DMC, check it.

## ReHLDS

Not really optional. The project uses custom version of ReHLDS and cannot work without it.

## CrossPlay

Not optional.

### Metamod + AmxModX

Some parts of the project are written as AMXX plugins. That include:
- "Equip" script that gives you random gear on CS maps + /wish menu
- "Pickups" script that handles dropped weapons and weapon/item pickups
- "Bots" script that manages CS and jk_botti bots + /bots menu
- "LetMePlay" script that allow you to respawn in place of a bot
- "Displacer" script that alters the behavior of the OP4 displacer on CS maps
- "fy_pool_nightmare" script that places monsters on the fy_pool_day map

This step installs Metamod-R and AmxModX and all the plugins above.

## FastDL

Since you need to download large amount of assets from the other games when connecting, the project has custom FastDL server that allows fast download via HTTP. It is installed in `crossfastdl` subdirectory.

## Desktop shortcut

Launching the server is also not that straightforward, so I made a launcher for you and put a shortcut on your desktop.

[Next step: launching](Launching.md)
