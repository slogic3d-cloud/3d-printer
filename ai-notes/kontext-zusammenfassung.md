# Kontext-Zusammenfassung (nach /clear zuerst lesen)

_Stand: 2026-11-02, Interview 60/120_

**Amethyst** = USB-PC-Stats-Display (Hack Club Fabricate, **Tier 3, max. $125, kein Eigengeld**). Der 3D-Drucker ist gestrichen.

## Festgelegt
- 3,5" TFT 320×480 (ILI9488/SPI), keine Bedienelemente, kein RGB, Seiten wechseln automatisch (Intervall am PC einstellbar)
- Inhalte: CPU/GPU-Last + Temp, RAM + Speicher, Uhr/Datum, Ping + Traffic + gelegentlicher Speedtest. Kein Spotify.
- **RP2040 direkt** auf eigener KiCad-Platine (JLC-PCBA, schwarz): USB-C, ESD, LDO, Quarz, 16 MB Flash, RTC + CR2032, BOOT + RESET, Backlight-PWM, keine LED. Platine sitzt direkt hinter dem Display (Stiftleiste). Kein Touch.
- Firmware Arduino C++. PC-Programm Python (Windows/Linux, Mac optional). Helligkeit am PC einstellbar.
- Standby: Uhr. Erbauer testet, ob USB bei PC aus Strom hat (Gigabyte Z170X-UD5 TH, BIOS ErP = Disabled).
- Gehäuse: schräger Keil, Fusion 360, PLA auf Kobra 2 Neo, Schwarz + Lila, Heat-Inserts. UI clean/modern, nur aktuelle Werte.
- PC-App: Tray + Einstellungsfenster, Gerät automatisch finden, kein Autostart, .exe + Skript. Einstellungen: Intervall, Helligkeit, Seiten an/aus, Farbschema, Ping-Ziele, Speedtest-Intervall, Uhrformat, Sprache DE/EN.
- Sensoren: Windows über LibreHardwareMonitor-Webserver (PawnIO), Linux psutil + amdgpu, Mac nur Last. GPU: AMD.
- Display quer 480×320, 2–4 Kacheln pro Seite.
- Journal: Claude gibt am Ende jeder Session Stichpunkte, Erbauer schreibt selbst.
- Erbauer: Programmieren „bisschen“, KiCad „mal reingeschaut“, 3–4 Wochen.

## Offen
- BOM + Kosten prüfen (≤ $125 inkl. Versand)
- USB-Standby-Strom am Gigabyte-Board messen

## Ablauf
4 Fragen pro Popup, alle ~20 Fragen Notizen + Commit + Hinweis auf `/clear`. Protokoll: `fragen-antworten-v2.md`. Harte Regeln: `kontext.md`.
