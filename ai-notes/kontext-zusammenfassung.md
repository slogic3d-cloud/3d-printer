# Kontext-Zusammenfassung (nach /clear zuerst lesen)

_Stand: 2026-11-05 (abends)_

**Amethyst** = jetzt ein **ESP32-Dev-Board** (Hack Club Fabricate, Tier 3 = „Dev-Board“, max. $125). Das PC-Stats-Display und der Drucker sind gestrichen.
Repo umbenannt: **slogic3d-cloud/dev-board**, gearbeitet wird **nur auf `main`** (Wunsch des Erbauers).
Lizenz: **CC BY-NC-SA 4.0** (`LICENSE`), privat nutzen + weiterentwickeln ja, verkaufen nein. Ob Fabricate eine Open-Source-Lizenz verlangt, noch prüfen.

## Stand KiCad (`PCB/DEV-Board-Based-on-ESP32.*`, KiCad 10, vom Erbauer)
- ESP32-WROOM-32U, CH340C, AMS1117-3.3, USB-C (HRO TYPE-C-31-M-12), 2× NPN Auto-Reset, BOOT + RESET, 2× 1x19-Stiftleiste, Platine ~39,5 × 52 mm, Bauteile platziert, **nicht geroutet**
- Review vom 2026-11-05, **kritische Fehler**: ESP32-VDD an GND, CH340C-VCC an GND, C1 in Reihe vor AMS1117-VI, AMS1117-VO geht nirgends hin, EN per R3 nach GND, Auto-Reset-Emitter an GND statt Kreuzschaltung, SENSOR_VN mit RXD0 kurzgeschlossen
- Sollte geändert werden: IO15 an GND, Kondensatorwerte ohne Einheit und fehlende Entkopplung, -32U braucht externe Antenne (Alternative -32E), Flash-Pins 17–22 markieren, Stiftleisten-Abstand 35,5 mm (nicht im Raster, nicht breadboard-tauglich), ESD/Polyfuse fehlen
- Tipp gegeben: Power-Symbole + Net-Labels statt langer Drähte, ERC laufen lassen

## Update Review 2 (neue Dateien in PCB/)
- Schaltplan jetzt korrekt (Strom, EN, Auto-Reset-Kreuzschaltung, USB, GPIOs). Offen: Werte `10kl`→`10k`, `5,1k`→`5.1k`, U2-Wert → ESP32-WROOM-32UE.
- PCB: kein Edge.Cuts-Umriss, alle Bahnen 0,2 mm (Power breiter!), keine GND-Zone, 0 Vias, Header-Abstand 27,5 mm (nicht im Raster), DRC noch nötig.
- Repo: CAD/ gelöscht, PINOUT.md + BOM.csv (neuer Stand) angelegt. README enthält Claude-Pinout-Tabelle → Erbauer soll durch eigenen Text/Link ersetzen bzw. in AI Disclosure nennen. JOURNAL: 7-h-Eintrag > 5 h, kein Bild, github-Feld fehlt.

## Erbauer
13–15, Deutschland, Programmieren: bisschen (Python bis Funktionen), KiCad: Anfänger, GitHub Desktop, 1 h alle 3 Tage, Erklärungen „mittel“.

## Ablauf
Tägliche Erinnerung 14:36 (Trigger trig_012NpC3ZcXYdy1ZP4xGwCUP3). Harte Regeln: `kontext.md`. Am Session-Ende Notizen + Commit auf `main` + Journal-Stichpunkte.
