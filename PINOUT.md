# Amethyst Board – Pinout

Generated from `PCB/DEV-Board-Based-on-ESP32.kicad_sch`.

## Header J2 (left)

| Pin | Signal | Notes |
|:---:|:---|:---|
| 1 | **3V3** | 3.3 V power |
| 2 | **EN** | Reset (active low) |
| 3 | IO36 (VP) | Input only |
| 4 | IO39 (VN) | Input only |
| 5 | IO34 | Input only |
| 6 | IO35 | Input only |
| 7 | IO32 | |
| 8 | IO33 | |
| 9 | IO25 | DAC1 |
| 10 | IO26 | DAC2 |
| 11 | IO27 | |
| 12 | IO14 | |
| 13 | IO12 | ⚠️ Strapping – must be LOW at boot |
| 14 | **GND** | |
| 15 | IO13 | |
| 16 | **GND** | |
| 17 | **3V3** | 3.3 V power |
| 18 | **5V** | USB 5 V (after fuse) |
| 19 | **5V** | USB 5 V (after fuse) |

## Header J3 (right)

| Pin | Signal | Notes |
|:---:|:---|:---|
| 1 | **GND** | |
| 2 | IO23 | |
| 3 | IO22 | I²C SCL (default) |
| 4 | TX0 (IO1) | USB serial |
| 5 | RX0 (IO3) | USB serial |
| 6 | IO21 | I²C SDA (default) |
| 7 | **GND** | |
| 8 | IO19 | |
| 9 | IO18 | |
| 10 | IO5 | ⚠️ Strapping |
| 11 | IO17 | |
| 12 | IO16 | |
| 13 | IO4 | |
| 14 | IO0 | ⚠️ Strapping – BOOT button |
| 15 | IO2 | ⚠️ Strapping |
| 16 | IO15 | ⚠️ Strapping |
| 17 | **GND** | |
| 18 | **3V3** | 3.3 V power |
| 19 | **5V** | USB 5 V (after fuse) |

## Notes

- **Input only (IO34–IO39):** no output, no internal pull-up/pull-down.
- **Strapping pins (IO0, IO2, IO5, IO12, IO15):** sampled at boot. Avoid driving them during reset. IO12 HIGH at boot selects 1.8 V flash and the board will not start.
- **TX0 / RX0:** used by the CH340C for uploading and the serial monitor.
- **5V:** taken from USB through a 500 mA polyfuse.
- **3V3:** AMS1117-3.3 regulator, keep total load well below 800 mA.
