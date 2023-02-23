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

# Special Notice (Arrêt)
#### If you are from the Marlin Community
##### Please use at your own risk

I am not an expert at firmware building. Although i may have experience in programming. I can assure you that i make mistakes. Sometimes more than i care to admit

## Marlin 2.1.2

Recent changes Include (in order of apperance)
This does not include a list of all changes. This is just incase i make a boo boo. 
Instead of looking back through weeks of version history, this serves as an easy way to see where my boo boo may have taken place.

### Config.h
```C
1670 #define NO_MOTION_BEFORE_HOMING //(uncomment) 
1879 //#define AUTO_BED_LEVELING_BILINEAR //(comment) 
1880 #define AUTO_BED_LEVELING_UBL //(uncomment) 
1888 //#define RESTORE_LEVELING_AFTER_G28 `//(comment)`
1896 #define LEVELING_NOZZLE_TEMP 80 //(was 50)
1991 #define MESH_INSET 30 //(was 15)      
1992 #define GRID_MAX_POINTS_X 9 //(was 6) 
2039 //#define BED_TRAMMING_USE_PROBE //(uncomment) 
2104 #define HOMING_FEEDRATE_MM_M { (30*60), (30*60), (6*60) } //(30 was 60)
2188 #define EEPROM_INIT_NOW //(uncomment)
3220 #define NUM_M106_FANS 1 //(1 was 2)
```

### Config_adv.h
```C
- #define HOMING_BUMP_DIVISOR { 5, 5, 4 } (5 was 2)
- #define ASSISTED_TRAMMING (Uncomment)
- #define ASSISTED_TRAMMING_WIZARD (uncomment)
- #define TRAMMING_SCREW_THREAD 40 (uncomment)
```
