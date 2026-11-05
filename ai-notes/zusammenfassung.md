# Zusammenfassung – Amethyst Dev Board

_Letztes Update: 2026-11-05_

## Status
Projekt wurde zum **ESP32-Dev-Board** umgestellt. Der erste Schaltplan und die Platzierung vom Erbauer liegen in `PCB/`. Das Review hat kritische Fehler gefunden (siehe `kontext-zusammenfassung.md`). Nichts bestellt.

## Nächste Schritte
1. Schaltplan korrigieren: Stromversorgung (3V3/5V), EN-Pull-up + Kondensator, Auto-Reset-Kreuzschaltung, SENSOR_VN/RXD0, Kondensatoren mit Einheiten
2. Power-Symbole + Net-Labels einsetzen, ERC ohne Fehler
3. Entscheiden: WROOM-32U (+ Antenne) oder WROOM-32E, Breite für Breadboard
4. Danach routen (von Hand), DRC, Claude-Review
5. Journal-Einträge schreiben (Erbauer, mit Bild)
6. Klären, ob Fabricate eine Open-Source-Lizenz verlangt (#fabricate)

## Archiv
- Interview zum PC-Stats-Display: `fragen-antworten-v2.md`, BOM-Schätzung dazu: `bom-schaetzung.md` (veraltet)
