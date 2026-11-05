Projekt Name: Amethyst-Board

Just a board with an external antenna an an ESP32 chip, an usb-c connector and 38 pins.
It supports 3.3V and 5V, and many GND pins.

I built it because of fun and I need a dev-board which I understood. It helped me to learn more about creating schematics and pcbs.


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


<img width="1690" height="865" alt="image" src="https://github.com/user-attachments/assets/579bfaf6-334a-40f4-9954-30b0b87278a9" />
<img width="332" height="461" alt="Screenshot 2026-11-05 234348" src="https://github.com/user-attachments/assets/519e7b70-938e-40e9-b6d1-a47c77f3e172" />
