**Ready to install Marlin 2.1.2.9 – update.cbd + assets – Tronxy X5SA / XY-2 / XY-3**

> ⚠️ Currently only for **STM32F103 boards** (Chitu3D V5 / V6 / V9).

Configuration by @Darkwulf183 – built from [Marlin-2.1.2.9-ALL-UI-Standart-Color-LVGL-BLTouch-STM32F103](https://github.com/Darkwulf183/Marlin-2.1.2.9-ALL-UI-Standart-Color-LVGL-BLTouch-STM32F103).

- 45 firmwares: 15 machines × Color UI / Classic UI / LVGL UI (LVGL with `assets` folder)
- Default options (no BLTouch, Linear Advance, Dual/Mixing extruder, Power Loss Recovery, Printcounter) – for these build your own from the source repository
- Download the ZIP below, copy `update.cbd` of your machine (LVGL: plus `assets`) to the SD card and power on
- After flashing: `M502`, `M500`, set Z offset, calibrate touch if needed
- Max. print temperature: 290 °C
