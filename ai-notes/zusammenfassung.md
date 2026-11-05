# Zusammenfassung – Amethyst PC Stats

_Letztes Update: 2026-11-02 (Interview 120/120 fertig)_

## Status
Phase 0 → 1: Konzept steht, KiCad-Schaltplan beginnt. Noch nichts bestellt.

## Konzept
- USB-PC-Stats-Display: CPU/GPU-Last + Temp, RAM/Speicher, Uhr/Datum, Ping/Traffic/Speedtest
- 3,5" ST7796S-TFT quer (480×320), 2–4 Kacheln pro Seite, Seiten rotieren automatisch, keine Bedienung, kein Touch, kein RGB
- Eigene 2-Lagen-Platine (JLC-PCBA, schwarz): RP2040, 16 MB Flash, USB-C + USBLC6 + Polyfuse, LDO, PCF8563-RTC + CR2032, BOOT + RESET, Backlight-PWM, Testpunkte
- Firmware: PlatformIO + TFT_eSPI, JSON-Zeilen über USB, Bootlogo, Uhr bei Verbindungsabbruch, Einstellungen im Flash, Update per UF2 oder Knopf in der PC-App
- PC-App: Python, pystray + tkinter, Tray + Einstellungen, Gerät automatisch finden, .exe + Skript; Sensoren über LibreHardwareMonitor (Windows), psutil/amdgpu (Linux)
- Gehäuse: Keil 30°, Front mit Blende + Rückschale, PLA schwarz/lila, Heat-Inserts, M2-Standoffs, Gummifüße

## Budget
Tier 3, max. $125, Schätzung ~$80–125 → `bom-schaetzung.md`. Knapp!

## Zeitplan (Stand 2026-11-05: 1 h alle 3 Tage, Start 05.11.)
Schätzung ~30 h gesamt (Tier 3 braucht ~17–33 h).
| Abschnitt | h | fertig ca. |
|---|---|---|
| Schaltplan (KiCad) | 7 | 23.11. |
| PCB-Layout + JLC bestellen | 6 | 11.12. |
| Gehäuse (Fusion) + Testdruck | 5 | 26.12. |
| Firmware | 6 | 13.01. |
| PC-App | 4 | 25.01. |
| Zusammenbau, Test, README | 2 | 31.01.2027 |
Ein früheres Ende wäre bei 17 h am 23.12. Das ursprüngliche Ziel von 3–4 Wochen bräuchte ~8–10 h pro Woche.

## Nächste Schritte
1. KiCad-10-Projekt `PCB/amethyst-pc-stats` anlegen, Schaltplan in Blöcke teilen (Erbauer zeichnet)
2. RP2040-Datenblatt + „Hardware design with RP2040“ lesen
3. Journal-Eintrag #1 schreiben (Erbauer, mit Bild)
4. Repo auf GitHub in `amethyst-pc-stats` umbenennen (Erbauer)
5. Gigabyte-Board: USB-Standby-Strom messen (BIOS ErP = Disabled)
6. Design-Reviewer finden (Hack Club Slack #fabricate)

## Offene Punkte
- Display-Pinout des konkreten Amazon-Moduls (vor Platzierung des Headers!)
- Reddit/Printables-Post, Video (beim Build-Ship)
