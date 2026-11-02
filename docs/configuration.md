# Configuration

The config is created the first time the server starts, in `Resources/Server/CareerMP/config/config.json`. New settings get added to it automatically when you update. You can edit the file while the server is off, or change things live with `CareerMP SetConfig <section> <key> <value>` in the server console.

## server

| Setting | Default | |
|---|---|---|
| `allowTransactions` | `true` | Lets players pay each other from the player list. |
| `shortWindowMax` | `1000` | Payment limit: how much a player can send within `shortWindowSeconds`. |
| `shortWindowSeconds` | `30` | |
| `longWindowMax` | `10000` | Payment limit: how much a player can send within `longWindowSeconds`. |
| `longWindowSeconds` | `300` | |
| `sessionSendingMax` | `100000` | Most a player can send to others in one session. |
| `sessionReceiveMax` | `200000` | Most a player can receive from others in one session. |
| `autoUpdate` | `false` | Checks this repo for a new version when the server starts and downloads it. |
| `autoExit` | `true` | Closes the server after an auto update, for servers with a restart script. |

## client

These get sent to every player.

| Setting | Default | |
|---|---|---|
| `roadTrafficEnabled` | `false` | |
| `roadTrafficAmount` | `0` | Driving traffic cars per player. |
| `extraTrafficEnabled` | `false` | |
| `extraTrafficAmount` | `0` | Extra traffic cars that get spawned but don't all drive at the same time. The game swaps them in so traffic looks more varied. |
| `parkedTrafficEnabled` | `false` | |
| `parkedTrafficAmount` | `0` | Parked cars per player. |
| `trafficSimpleVehicles` | `true` | Uses the simple traffic models, which are much lighter. |
| `trafficSmartSelections` | `true` | BeamNG's own pick of which cars spawn in traffic. |
| `trafficAllowMods` | `false` | Lets mod vehicles show up in traffic. |
| `serverSaveSuffix` | `""` | Added to the end of the save name so players get a separate save for this server. With `myserver`, `misterp` becomes `misterpmyserver`. |
| `serverSaveName` | `""` | Save name every player uses instead of their BeamMP name when `serverSaveNameEnabled` is on. Each player still has their own copy on their PC. |
| `serverSaveNameEnabled` | `false` | |
| `localUnicycleGhost` | `false` | When you walk, other things go through you. |
| `remoteUnicycleGhost` | `true` | Other players that are walking can't be hit. |
| `remoteVehicleGhost` | `false` | Other players' cars have no collision. |
| `worldEditorEnabled` | `false` | Lets players open the world editor. |
| `consoleEnabled` | `false` | Lets players open the Lua console. |
| `simplifyRemoteVehicles` | `false` | |
| `spawnVehicleIgnitionLevel` | `0` | |
| `skipOtherPlayersVehicles` | `false` | |

The traffic and gameplay settings are set in the player's game while they're on the server and put back to their own when they leave.
