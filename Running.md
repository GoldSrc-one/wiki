[Go back to index](README.md)

#

# Running

There is a launcher that helps you with running the server.

If you installed CrossPlay in `c:\hlds` it will be in `c:\hlds\crossplay\Launcher.exe` and there will be a shortcut on your desktop.

## Games vs Ports

The launcher lets you select what games will be included in the crossplay and what ports will be open.

If you add a game, you will be able to use maps and entities from that game.
If you add a port, you will be able to connect from that game.

You can choose from many combinations, just be aware of this:

### Order matters

The game order matters. It is the order in which the games are initialized. Counter-Strike is special and it must go last, otherwise game messages will not be registered properly.

The port order also matter. It starts with port 27015 and goes up. If you don't like 27015, you can do `+port 12345` and it will go up from there.

### CS/CZ confusion

The cstrike/czero combo is special. Just add either `cstrike` or `czero` as a game and you will be able to use assets from both.

But to join from CS, you need `cstrike` port. To join from CZ, you need `czero` port. To join from both, you need both ports.

If you want to run vanilla CS server and join it from both CS and CS, check out [Running CS/CZ (or HL/AG) crossplay only](Running_CSCZ.md).

## FastDL

The launcher will start the crossfastdl server that allow for faster asset downloading via HTTP.

## Command line

You can tweak the resulting command line or just copy paste it to your own .bat launcher.

# First run

You will need to have some patience when running the server first time.

First time running on deathmatch maps and on CS maps -- the server will convert the player models so they are displayed properly in the other games. This can take a few minutes.

Also be aware that CS bots will start their learning routine if there is not a `.nav` file ready for that map. That drops the server fps down to about 4 and takes from a few minutes to an hour per map.

HL bots also needs to learn the map, so be patient or let them play with the CS bots for a while so they learn from them.

# Running on Linux

If you wish to run the server on linux, you need to use wine. Either copy the whole from windows or use steamcmd with *the parameter I don't know right now the name for* to download windows version of HLDS on linux.

You will have to install all these things mentioned above manually. I have also modified the ReHLDS `hlds.exe` that it runs nicely as a console application, so make sure you grab it [from here](https://github.com/GoldSrc-one/rehlds/releases).

#

[Next topic: Architecture](Architecture.md)
