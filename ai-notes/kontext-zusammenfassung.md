# Kontext-Zusammenfassung (nach /clear zuerst lesen)

_Stand: 2026-11-06_

**Amethyst Board** = ESP32-Dev-Board (Fabricate Tier 3, max. $125). Repo **slogic3d-cloud/dev-board**, nur `main`. Lizenz CC BY-NC-SA 4.0.

## Fertig
- KiCad 10: Schaltplan + PCB vom Erbauer (ESP32-WROOM-32UE, CH340C, AMS1117, USB-C + USBLC6 + Polyfuse, Auto-Reset, BOOT/RESET, 2x 1x19). 48,5 × 53 mm, 2 Lagen, alle Netze geroutet, DRC 0 Fehler, Via min 0,3 mm.
- `PCB/`: .kicad_*, .step, gerbers.zip, production/ (JLC bom.csv, positions.csv, netlist.ipc)
- `BOM.csv` mit JLC-Preisen (Stand Standard PCBA ×5, Express): €99,70 ≈ $115
- README: About, Why, Pictures, Pinout, BOM + Cost, AI Disclosure, License. JOURNAL: 2 Einträge (7,5 h), Bilder, github/description.

## Offen
- JLC-Warenkorb umstellen: **Economic PCBA, Menge 2, Global Standard Versand** → BOM + README-Cost neu
- Firmware (Fabricate-Pflicht) fehlt, firmware/ wurde auf Wunsch gelöscht
- Gegencheck in #fabricate, Grant-Ablauf klären, NICHT selbst bezahlen
- README/JOURNAL: Listen ohne `-`, Tippfehler (optional)
- Später Build-Ship: bauen, Video, Foto, Post

## Regeln
Kein Text in README/JOURNAL schreiben (nur Feedback/Korrekturen), kein CAD/PCB designen. Plugin-Ordner .claude-flow/.swarm bleiben drin (Stop-Hook meldet sie ständig). Tägliche Erinnerung 14:36 (trig_012NpC3ZcXYdy1ZP4xGwCUP3).
