# Changelog

## 0.1.0

First version, based on CareerMP 0.0.37.

### BeamNG 0.40 port
- Rebuilt `careerMP.lua`, `computer.lua` and `playerDriving.lua` on top of the 0.40 versions of those files
- Removed the old overrides of insurance, inventory, tuning, painting, part shopping, walking and the drag display, the 0.40 versions work as they are
- Updated for the renamed BeamMP events and UI apps
- Removed the top bar and camera patches, the things they patched don't exist anymore in 0.40
- Drag race light sync turned off

### Fixes
- New careers get started under a cleaned up save name, so names with capitals, spaces or symbols don't start a new career on every join anymore
- Other players' cars don't get removed when your career loads
- Traffic turned off in the config stays off
- Only the car you're driving gets reported by speed cameras and red light cameras, not traffic
- Fixed the player list app not loading
- Bigger computer zones in the garages
- Per-part painting works with the 0.40 computer menu and doesn't crash when a vehicle is missing

### Other
- Auto update is off by default and checks this repo instead of the original one
