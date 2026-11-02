# CareerMP-V2

A fork of [CareerMP](https://github.com/StanleyDudek/CareerMP) by StanleyDudek, ported to BeamNG.drive 0.40 with some fixes on top.

It works the same way as the original: everyone plays their own career on the same map, and the career is saved on each player's own PC. If you want the server to keep the saves so players can't edit their money, have a look at [CareerMP-Server-Authoritive](https://github.com/MisterP-dev/CareerMP-Server-Authoritive) instead.

All credit for the base mod goes to StanleyDudek (Dudekahedron). This wouldn't exist without CareerMP.

## What's different from CareerMP

- Works on BeamNG.drive 0.40.1. The original glitches on join there because a lot of the career code changed in 0.40.
- Fixed a new career getting started on every join when your BeamMP name has capitals, spaces or symbols in it.
- Other players' cars don't disappear anymore when your career loads.
- Traffic that's turned off in the config actually stays off.
- Traffic driving through speed cameras or red light cameras doesn't get announced as a player anymore.
- Fixed the player list app.
- Bigger computer zones in the garages.
- Fixes for per-part painting.
- Auto update is off by default and checks this repo instead of the original one.
- Drag race light sync is turned off for now, the drag strip code changed too much in 0.40.

## Requirements

Tested with:

- BeamNG.drive 0.40.1
- BeamMP Server 3.9.3

West Coast, USA only, same as the original.

## Installing

1. Remove any old CareerMP from your server first (`Resources/Client/CareerMP.zip` and `Resources/Server/CareerMP/careerMP.lua`). You can keep the config folder.
2. Download this repo (Code > Download ZIP) and copy `Resources/Client/CareerMP.zip` and `Resources/Server/CareerMP/` into the same places in your BeamMP server folder.
3. In `ServerConfig.toml` set `MaxCars = 100` or more and `Map = "/levels/west_coast_usa/info.json"`.
4. Start the server once. It creates `Resources/Server/CareerMP/config/config.json`.
5. Change whatever you want in the config (see [docs/configuration.md](docs/configuration.md)) and restart the server.

`Resources/Client/CareerMP/` in this repo is the unpacked content of `CareerMP.zip`, so the code can be read on GitHub. The server only needs the zip.

**Restart the server every time you update the files.** The server only loads the mod when it starts, so until then players keep getting the old version.

## Saves

Saves are on each player's PC, in `%LOCALAPPDATA%\BeamNG\BeamNG.drive\current\settings\cloud\saves\`.

The save is named after your BeamMP name, in lowercase with only letters and numbers (`Mister_P` becomes `misterp`). If you already have a save with exactly your BeamMP name from an older version, that one gets used.

You can keep playing the same save offline or on another server running CareerMP. To use a single player save online, rename its folder to match your BeamMP name before joining.

A server can change the save name with `serverSaveSuffix` (adds something to the name, so every server gets its own save) or `serverSaveName` (everyone uses that name). See [docs/configuration.md](docs/configuration.md).

## Traffic

Traffic is off by default. When it's on, every player spawns their own traffic and parked cars, and everyone else sees them as normal multiplayer cars. They don't get nametags as long as the simple traffic models are used, which is the default. Keep in mind it adds up: 3 players with 10 traffic cars each means 30 extra cars on the server, so set `MaxCars` high enough.

## Commands

In the server console (`CMP` works as a shorter prefix):

| Command | |
|---|---|
| `CareerMP Help` | Lists the commands |
| `CareerMP GetConfig [section] [key]` | Shows the config, a section or a single value |
| `CareerMP SetConfig <section> <key> <value>` | Changes a setting and saves it, e.g. `CareerMP SetConfig client roadTrafficAmount 5` |
| `CareerMP Update` | Checks this repo for a newer version and downloads it |

## Known issues

- Saves are local, so players can edit their own money. That's how the original works too. Use [CareerMP-Server-Authoritive](https://github.com/MisterP-dev/CareerMP-Server-Authoritive) if that's a problem for you.
- Drag race lights aren't synced.
- Not tested much with more than 3 players yet.

If something breaks, open an issue and add your `Server.log` and the player's `beamng.log` (found in `%LOCALAPPDATA%\BeamNG\BeamNG.drive\current\`).

## Credits

- [StanleyDudek](https://github.com/StanleyDudek) for CareerMP: [original repo](https://github.com/StanleyDudek/CareerMP), [Dudek's Sandbox discord](https://discord.gg/caU5adg)
- Bouboule, and Lion and Luuk from BeamPaint, who are thanked in the original for the http request examples
- BeamNG and the BeamMP team
