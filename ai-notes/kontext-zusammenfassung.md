# Kontext-Zusammenfassung (nach /clear zuerst lesen)

_Stand: 2026-11-02, Interview 120/120 ✅_

**Amethyst** = USB-PC-Stats-Display (Hack Club Fabricate, **Tier 3, max. $125, kein Eigengeld**). Der 3D-Drucker ist gestrichen.

## Festgelegt
- 3,5" TFT 320×480 **ST7796S**/SPI (Amazon.de, Begründung: verlässlicher Verkäufer/Rückgabe), keine Bedienelemente, kein RGB, Seiten wechseln automatisch (Intervall am PC einstellbar)
- Inhalte: CPU/GPU-Last + Temp, RAM + Speicher, Uhr/Datum, Ping + Traffic + gelegentlicher Speedtest. Kein Spotify.
- **RP2040 direkt** auf eigener KiCad-Platine (JLC-PCBA, schwarz): USB-C, ESD, LDO, Quarz, 16 MB Flash, RTC PCF8563 + Quarz + CR2032, 2 Lagen, BOOT + RESET, Backlight-PWM, keine LED. Platine sitzt direkt hinter dem Display (Stiftleiste). Kein Touch.
- Firmware Arduino C++. PC-Programm Python (Windows/Linux, Mac optional). Helligkeit am PC einstellbar.
- Standby: Uhr. Erbauer testet, ob USB bei PC aus Strom hat (Gigabyte Z170X-UD5 TH, BIOS ErP = Disabled).
- Gehäuse: schräger Keil ~30°, so flach wie möglich, Front (mit gedruckter Blende) + Rückschale, USB-C seitlich, PCB auf M2-Standoffs, Büroklammer-Loch für BOOT/RESET, Gummifüße, kein Logo. Fusion 360 (Erbauer: Grundlagen), PLA auf Kobra 2 Neo, Schwarz + Lila, Heat-Inserts. UI clean/modern, nur aktuelle Werte.
- PC-App: Tray + Einstellungsfenster, Gerät automatisch finden, kein Autostart, .exe + Skript. Einstellungen: Intervall, Helligkeit, Seiten an/aus, Farbschema, Ping-Ziele, Speedtest-Intervall, Uhrformat, Sprache DE/EN.
- Sensoren: Windows über LibreHardwareMonitor-Webserver (PawnIO), Linux psutil + amdgpu, Mac nur Last. GPU: AMD.
- Display quer 480×320, 2–4 Kacheln pro Seite. Bootlogo, bei Verbindungsabbruch nach 5 s Uhr + „PC getrennt“. Einstellungen im Geräte-Flash. Update: UF2 + Update-Knopf in der PC-App.
- Firmware: PlatformIO + TFT_eSPI, JSON-Zeilen über USB-CDC (ArduinoJson). PC: pystray + tkinter (System-Standard-Look).
- JLC: 2 bestückt (+3 nackt), Bezahlung über HCB-Karte. Reihenfolge: PCB zuerst, kein Breadboard-Prototyp. Inserts mit normaler Lötspitze.
- Erbauer: Python bis Funktionen, Git per GitHub Desktop, 5–10 h/Woche. Design-Reviewer noch offen → vor dem Einreichen erinnern.
- Claude-Rolle: Schaltplan-Reviews, Code-Hilfe, CAD-Feedback, BOM/Preise.
- Lizenz: Code MIT, Hardware CERN-OHL. RP2040-Referenzdesign als Lesevorlage.
- Journal: Claude gibt am Ende jeder Session Stichpunkte, Erbauer schreibt selbst.
- Erbauer: Programmieren „bisschen“, KiCad „mal reingeschaut“, 3–4 Wochen.

## Offen
- Nächster Schritt: KiCad-10-Projekt + Schaltplan-Blöcke mit Claude, danach Journal-Eintrag, täglich 15-Uhr-Erinnerung
- Display-Pinout des Amazon-Moduls prüfen, bevor der Header platziert wird
- Repo-Umbenennung in amethyst-pc-stats (Erbauer)
- USB: ESD USBLC6 + Polyfuse 500 mA, Testpunkte 5V/3V3/GND, erster Test mit Multimeter + Powerbank
- BOM + Kosten prüfen (≤ $125 inkl. Versand)
- USB-Standby-Strom am Gigabyte-Board messen

## Ablauf
Interview fertig. Am Session-Ende Notizen + Commit + Journal-Stichpunkte. Protokoll: `fragen-antworten-v2.md`. Harte Regeln: `kontext.md`.
