[Go back to index](README.md)

#

# Running CS/CZ or HL/AG crossplay only

If you wish to run vanilla CS server and just let CZ players join (or similar setup with HL server and AG players), you can do that just with the custom ReHLDS.

If you have the installer downloaded, there is nothing easier then just checking "Counter Strike" and "ReHLDS" in the installer and letting it run.

If you don't have the installer, you can get the ReHLDS binaries [from here](https://github.com/GoldSrc-one/rehlds/releases).
If you are running windows, just get `swds.dll` and `swds.pdb` and put them in your HLDS folder. If you are running linux, get the `engine_i486.so`.

To allow clients from other games, you need to use the `-sgameX XXX` parameter.
For example

## CS/CZ crossplay

```
hlds -game cstrike -sgame1 cstrike -sgame2 czero ...
```

This will open port 27015 for cstrike player and 27016 for czero players

## HL/AG crossplay

```
hlds -game valve -sgame1 valve -sgame2 ag ...
```

This will open 27015 for HL1 players and 27016 for AG players.
