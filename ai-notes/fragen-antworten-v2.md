# Interview v2: einfaches Projekt (ab 2026-11-02)

> Protokoll von Claude. Das alte Drucker-Interview steht in `fragen-antworten.md` (archiviert).

## Runde 1–2 (8/120)
1. Verhältnis zum Drucker: Name **Amethyst** bleibt, **Drucker wird gestrichen** (zu teuer, zu kompliziert).
2. Tier: weiß nicht → Claude schlägt vor.
3. Richtung: erst alles (Eingabe, Anzeige, Smart Home/Sensor, Spiel) → dann **Spiel + Sensor gestrichen** → **Eingabe + Anzeige**.
4. Zeit: **3–4 Wochen**.
5. Konzept-Kombi: neu fragen (ohne Spiel/Sensor).
6. Ort: egal.
7. Strom: **USB-C**.
8. Programmieren: **bisschen** (Arduino-Beispiele/Python-Grundlagen).

Runde 3 (Konzept, Eingabe-Elemente, Display, RGB) wurde vom Erbauer abgebrochen → nachfragen, was geändert werden soll.

## Runde 3–9 (36/120)
9. Konzept: **PC-Stats-Display**.
10. Eingabe-Elemente: keine Präferenz → später: **keine Bedienung**.
11. Display: Claude entscheidet → dann gewählt: **3,5" TFT 320×480** (ILI9488, SPI).
12. RGB: **keins**.
13. Infos: **CPU/GPU-Last + Temp, RAM + Speicher, Uhrzeit/Datum, Internet-Speed + Ping**. (Spotify erst gewählt, dann **gestrichen**.)
14. Verbindung: **USB-Kabel** (USB-Seriell, Python-Programm am PC).
15. PC-OS: **Windows + Linux**, Mac wäre schön → PC-Programm plattformübergreifend (Python + psutil).
16. Bedienung: **keine** → Seiten wechseln automatisch.
17. Seitenwechsel-Intervall: **am PC einstellbar**.
18. Display: **3,5" TFT 320×480**.
19. MCU: Claude → **Raspberry Pi Pico (RP2040-Modul)** auf eigener Trägerplatine.
20. Firmware-Sprache: Claude → **Arduino C++** (MicroPython zu langsam für 480×320). PC-Seite: **Python**.
21. Gehäuseform: **schräger Keil**.
22. CAD: **Fusion 360**.
23. Druck: **selbst, Kobra 2 Neo, PLA**.
24. Verbindung: **Schrauben + Einschmelzmuttern**.
25. Farbe: **Schwarz + Lila**.
26. UI-Stil: **clean/modern**.
27. Graphen: **nur aktuelle Werte** (Zahlen + Balken).
28. Standby: **Uhr**.
29. Strom bei PC aus: Erbauer fragt, ob Gigabyte Z170X-UD5 TH USB-Standby-Strom liefert → Claude: wahrscheinlich mit BIOS **ErP = Disabled**, Erbauer soll messen.
30. Helligkeit: **am PC einstellbar** (PWM an Backlight).
31. Netz: **Ping ständig + aktueller Traffic + gelegentlicher Speedtest**.
32. Spotify: **raus**.
33. RTC: **RTC-Chip einplanen** (z. B. DS3231 + CR2032).
34. Platine: Claude entscheidet → Trägerplatine: Pico, USB-C, ESD-Schutz, RTC + Knopfzelle, Display-Anschluss, Backlight-Transistor, Befestigungslöcher.
35. KiCad: **mal reingeschaut**.
36. USB: **USB-C-Buchse auf eigener Platine** → ⚠️ Pico-USB-Datenleitungen liegen auf Testpads TP2/TP3 unten, Anbindung muss geklärt werden.
