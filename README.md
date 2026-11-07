# This repository is a ready to install Version of Marlin 2.1.2.9, with Tronxy X5SA (and variants) ready for install.

> **⚠️ Currently only for STM32F103 boards** (Chitu3D V5 / V6 / V9, STM32F103ZET6).

Built from the source repository
[Marlin-2.1.2.9-ALL-UI-Standart-Color-LVGL-BLTouch-STM32F103](https://github.com/Darkwulf183/Marlin-2.1.2.9-ALL-UI-Standart-Color-LVGL-BLTouch-STM32F103)
with the default settings of that configuration (no BLTouch, no Linear Advance, no Dual/Mixing extruder, no Power Loss Recovery, no Printcounter).
If you need one of these options, select it in the source repository and build your own firmware.

## Beware of the LVGL Ui. This one is buggy with the Chitu boards. Only those who know exactly how to avoid the errors should use them!

## Predefined update.cbd + assets
```
Color UI    / V5 Boards / <machine> / update.cbd
            / V6 Boards / <machine> / update.cbd
Classic UI  / V5 Boards / <machine> / update.cbd
            / V6 Boards / <machine> / update.cbd
LVGL UI     / V5 Boards / <machine> / update.cbd + assets
            / V6 Boards / <machine> / update.cbd + assets
```
- V5 Boards: `V5_330_*`, `XY3_V5_310_NO_TITAN_NO_TMC_NO_ABL`
- V6 Boards: `V6_330_*`, `V6_400_*`, `V6_500_*`, `V6_500_TITAN_TMC2209` (New Chitu V6 190319), `V6_500_TITAN_TMC2209V9` (New Chitu V9 200420), `XY2_V6_255_ALL`

## Install
1. Copy `update.cbd` of your machine to the SD card (for **LVGL UI** also the `assets` folder).
2. Insert the SD card and power on the printer. After a few beeps Marlin starts.
3. Send `M502` and then `M500` (reset EEPROM to the new defaults), set your Z offset (`M851`) and calibrate the touch screen if needed.

## Notes for 2.1.2.9
- Max. hotend temperature is now **290 °C** (`HEATER_0_MAXTEMP` 305 – thermistor 1 only reads up to 320 °C).
- Z steps: 800 steps/mm for the TMC boards, 400 steps/mm for the non-TMC boards and the V6 190319 / V9 – check with `M503` and correct with `M92` + `M500` if your machine differs.
- All 45 firmwares were built and tested to compile (arm-none-eabi-gcc, PlatformIO env `chitu_f103`). Flash/RAM usage is far below the limit.

<img align="right" width=175 src="marlin-250.png" />

Marlin documentation: [marlinfw.org](https://marlinfw.org/) – Marlin is licensed under the GPL v3.

Contributors: see [CONTRIBUTORS.md](CONTRIBUTORS.md)
