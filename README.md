Projekt Name: Amethyst-Board

Just a board with an external antenna an an ESP32 chip, an usb-c connector and 38 pins.
It supports 3.3V and 5V, and many GND pins.

I built it because of fun and I need a dev-board which I understood. It helped me to learn more about creating schematics and pcbs.


Pin-Out

J2	Pin	        Hinweis	  	J3	  Pin	        Hinweis
1	  3V3			                  1	  GND	
2	  EN	        Reset		      2	  IO23	
3	  IO36 (VP)	  nur Eingang		3	  IO22	
4	  IO39 (VN)	  nur Eingang		4	  TX0 (IO1)	  USB-Seriell
5   IO34	      nur Eingang		5	  RX0 (IO3)	  USB-Seriell
6	  IO35	      nur Eingang		6	  IO21	      I²C SDA
7	  IO32			                7	  GND	
8	  IO33			                8	  IO19	
9	  IO25	      DAC1		      9	  IO18	
10	IO26	      DAC2		      10	IO5	        Strapping
11	IO27			                11	IO17	
12	IO14			                12	IO16	
13	IO12	      Strapping     13	IO4	
14	GND			                  14	IO0	        BOOT-Taste
15	IO13			                15	IO2	        Strapping
16	GND			                  16	IO15	      Strapping
17	3V3			                  17	GND	
18	5V			                  18	3V3	
19	5V			                  19	5V	

<img width="1690" height="865" alt="image" src="https://github.com/user-attachments/assets/579bfaf6-334a-40f4-9954-30b0b87278a9" />
