# Amethyst-Board
## About
Just a board with an external antenna and an ESP32 chip, a USB-C connector and 38 pins.
It supports 3.3V and 5V, and many GND pins.

## Why I built this
I built it because of fun and I need a dev-board which I understood. It helped me to learn more about creating schematics and pcbs.

## Pictures
Under this text is the pictures for the schematics, it is not the best work but it still functions.
<img width="1690" height="865" alt="image" src="https://github.com/user-attachments/assets/579bfaf6-334a-40f4-9954-30b0b87278a9" />

Below this short sentence you can see a picture from the PCB, actually it is a good beginner work.
<img width="774" height="766" alt="Screenshot 2026-11-06 110030" src="https://github.com/user-attachments/assets/873d2b86-e26d-4f36-a4fa-e0944bce60d1" />


## Pinout
### Header J2 (left)

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

### Header J3 (right)

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

## BOM
See [BOM.csv](BOM.csv)
Cost: 

## What did the ai
I used ai for correcting and helping me out so that i didn't make that much mistakes.
As ai i used "Claude Code". With him we brainstormed the Project idea. 
He made the schematic review and error finding, the Pin-to-Pint connection list, the Component and footprint suggestions, the Pinout table formatting.
He helped me also with the writing, spelling and grammar in the different texts.
The Repository organization (folder, .gitignore, license file) was made by him like the BOM.csv structure. 
Important to say is that he helped at the PCB review and how KiCad works.

### What i did myself:
Schematics drawing
Components placement
PCB routing
DRC fixes
Gerber and Step export
README and journal writing

## License
License: CC BY-NC-SA 4.0
Meaning: do not sell it, further develop and private use are allowed
