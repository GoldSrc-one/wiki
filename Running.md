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

#

[Next topic: Architecture](Architecture.md)
