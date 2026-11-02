# Kontext-Zusammenfassung (nach /clear zuerst lesen)

_Stand: 2026-11-02, Interview 36/120_

**Amethyst** = USB-PC-Stats-Display (Hack Club Fabricate, Tier vermutlich 4, evtl. 3). Der 3D-Drucker ist gestrichen.

## Festgelegt
- 3,5" TFT 320×480 (ILI9488/SPI), keine Bedienelemente, kein RGB, Seiten wechseln automatisch (Intervall am PC einstellbar)
- Inhalte: CPU/GPU-Last + Temp, RAM + Speicher, Uhr/Datum, Ping + Traffic + gelegentlicher Speedtest. Kein Spotify.
- Raspberry Pi Pico (Modul) auf eigener KiCad-Trägerplatine: USB-C, ESD, RTC (DS3231/PCF8563 + CR2032), Display-Header, Backlight-PWM
- Firmware Arduino C++. PC-Programm Python (Windows/Linux, Mac optional). Helligkeit am PC einstellbar.
- Standby: Uhr. Erbauer testet, ob USB bei PC aus Strom hat (Gigabyte Z170X-UD5 TH, BIOS ErP = Disabled).
- Gehäuse: schräger Keil, Fusion 360, PLA auf Kobra 2 Neo, Schwarz + Lila, Heat-Inserts. UI clean/modern, nur aktuelle Werte.
- Erbauer: Programmieren „bisschen“, KiCad „mal reingeschaut“, 3–4 Wochen.

## Offen
- USB-C → Pico: Datenleitungen an TP2/TP3 oder Pico-Variante mit USB an Randpads?
- Tier, Budget, BOM

## Ablauf
4 Fragen pro Popup, alle ~20 Fragen Notizen + Commit + Hinweis auf `/clear`. Protokoll: `fragen-antworten-v2.md`. Harte Regeln: `kontext.md`.
