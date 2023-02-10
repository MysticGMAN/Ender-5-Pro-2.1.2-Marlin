<p align="center"><img src="buildroot/share/pixmaps/logo/marlin-outrun-nf-500.png" height="250" alt="MarlinFirmware's logo" /></p>

<h1 align="center">Marlin 3D Printer Firmware</h1>

<p align="center">
    <a href="/LICENSE"><img alt="GPL-V3.0 License" src="https://img.shields.io/github/license/marlinfirmware/marlin.svg"></a>
    <a href="https://github.com/MarlinFirmware/Marlin/graphs/contributors"><img alt="Contributors" src="https://img.shields.io/github/contributors/marlinfirmware/marlin.svg"></a>
    <a href="https://github.com/MarlinFirmware/Marlin/releases"><img alt="Last Release Date" src="https://img.shields.io/github/release-date/MarlinFirmware/Marlin"></a>
    <a href="https://github.com/MarlinFirmware/Marlin/actions"><img alt="CI Status" src="https://github.com/MarlinFirmware/Marlin/actions/workflows/test-builds.yml/badge.svg"></a>
    <a href="https://github.com/sponsors/thinkyhead"><img alt="GitHub Sponsors" src="https://img.shields.io/github/sponsors/thinkyhead?color=db61a2"></a>
    <br />
    <a href="https://fosstodon.org/@marlinfirmware"><img alt="Follow MarlinFirmware on Mastodon" src="https://img.shields.io/mastodon/follow/109450200866020466?domain=https%3A%2F%2Ffosstodon.org&logoColor=%2300B&style=social"></a>
</p>

Additional documentation can be found at the [Marlin Home Page](https://marlinfw.org/).


## Marlin 2.1.2

Recent changes Include (in order of apperance)

### Config.h
- `#define NO_MOTION_BEFORE_HOMING` (uncomment) 
<p style="color:green"> - `//#define AUTO_BED_LEVELING_BILINEAR` </p> (comment) 
- `#define AUTO_BED_LEVELING_UBL` (uncomment) 
- `#define LEVELING_NOZZLE_TEMP 80` (was 50)
- `#define MESH_INSET 30` (was 15)      
- `#define GRID_MAX_POINTS_X 9` (was 6) 
- `#define BED_TRAMMING_USE_PROBE` (uncomment) 
- `#define HOMING_FEEDRATE_MM_M { (30*60), (30*60), (6*60) }` (30 was 60)
- `#define EEPROM_INIT_NOW` (uncomment)

### Config_adv.h
- `#define HOMING_BUMP_DIVISOR { 5, 5, 4 }` (5 was 2)
- `#define ASSISTED_TRAMMING` (Uncomment)
- `#define TRAMMING_POINT_XY { {  30, 30 }, { 200, 30 }, { 200, 200 }, { 30, 200 } }` (30 was 20 & 200 was 180)
- `#define ASSISTED_TRAMMING_WIZARD` (uncomment)
- `#define TRAMMING_SCREW_THREAD 40` (uncomment)
