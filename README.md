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

# Intended Use

This Build of Marlin (2.1.2) is only ment to be used for the Big Tree Tech (BTT) SKR MINI E3 V3.0. With the Ender 5 Pro (w/ upgraded lead screw [^1]) & a CR-Touch. Everything else is stock. 

## Special Notice (Arrêt)
#### If you are from the Marlin Community
##### Please use at your own risk [^2]


## Marlin 2.1.2

Recent changes Include <sub>in order of apperance</sub>.[^3]

<sup> The numbers before the code are there for ease of location during diagnostics </sup>

### Config.h
```C
1493 #define PROBING_MARGIN 25 //(was 10)
1549 //#define MULTIPLE_PROBING 1 //(comment)
1571 #define Z_PROBE_LOW_POINT -1.25 //(was -2)
1574 #define Z_PROBE_OFFSET_RANGE_MIN -4 //(was -20)
1604 #define PREHEAT_BEFORE_PROBING //(uncomment)
1606 #define PROBING_NOZZLE_TEMP 50 //(was 90) 
1670 #define NO_MOTION_BEFORE_HOMING //(uncomment) 
1879 //#define AUTO_BED_LEVELING_BILINEAR //(comment) 
1880 #define AUTO_BED_LEVELING_UBL //(uncomment) 
1888 //#define RESTORE_LEVELING_AFTER_G28 //(comment)
1894 //#define PREHEAT_BEFORE_LEVELING //(comment)
1896 #define LEVELING_NOZZLE_TEMP 80 //(was 50)
1943 //#define G26_MESH_VALIDATION //(comment)
1991 #define MESH_INSET 10 //(was 30)      
1992 #define GRID_MAX_POINTS_X 9 //(was 6) 
2023 //#define LCD_BED_LEVELING //(comment)
2032 //#define LCD_BED_TRAMMING //(comment)
2039 //#define BED_TRAMMING_USE_PROBE //(comment) 
2104 #define HOMING_FEEDRATE_MM_M { (30*60), (30*60), (6*60) } //(30 was 60)
2188 #define EEPROM_INIT_NOW //(uncomment)
3220 #define NUM_M106_FANS 1 //(1 was 2)
```

### Config_adv.h
```C
883 #define HOMING_BUMP_DIVISOR { 5, 5, 4 } //(5 was 2)
1032 #define ASSISTED_TRAMMING //(Uncomment)
1047 #define ASSISTED_TRAMMING_WIZARD //(uncomment)
1057 #define TRAMMING_SCREW_THREAD 40 //(uncomment)
```
####


[^1]: This lead screw is a 400mm T8 ACME thread single (1) start with a 2mm pitch & lead. It also has a T8 Anti-backlash spring loaded Nut. As well as a royal duck load of cheap WD-40 Whit lithium grease in the z-stepper motor. MLG maneuver right there. 

[^2]: I am not an expert at firmware building. Although i may have experience in programming. I can assure you that i make mistakes. Sometimes more than i care to admit.

[^3]: This does not include a list of all changes. This is just incase i make a boo boo. Instead of looking back through weeks of version history, this serves as an easy way to see where my boo boo may have taken place.