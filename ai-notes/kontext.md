# Kontext für Claude (bei jeder Session zuerst lesen)

## Projekt
**Amethyst**: ESP32-Dev-Board (eigene KiCad-Platine, später Gehäuse/Firmware-Beispiele). Davor geplant und gestrichen: 3D-Drucker, dann PC-Stats-Display.
Erbauer: Teen (13–15) aus Deutschland, Hack Club **Fabricate Tier 3 (max. $125)**.
Repo: github.com/slogic3d-cloud/dev-board, **nur Branch `main`**. Lizenz CC BY-NC-SA 4.0.

## Dateien
- `ai-notes/kontext-zusammenfassung.md`: **aktueller Stand, nach /clear zuerst lesen**
- `ai-notes/zusammenfassung.md`: Projektüberblick, nächste Schritte
- `ai-notes/fragen-antworten-v2.md`: 120-Fragen-Interview
- `ai-notes/bom-schaetzung.md`: Kostenschätzung
- `ai-notes/journal.md`: Claudes Arbeitslog (≠ Fabricate-JOURNAL)
- `ai-notes/fabricate-regeln.md`: Programmregeln
- `JOURNAL.md`, `README.md`: **gehören dem Erbauer**, ich schreibe dort keinen Inhalt
- Ordner: `PCB/` (KiCad), `CAD/`, `firmware/`

## ⚠️ Harte Regeln (Fabricate, sonst Ablehnung/Bann für den Erbauer)
1. **Keinen Text in README.md oder JOURNAL.md schreiben.** Struktur-Tipps, Stichpunkte, Feedback ja, Text vom Erbauer.
2. **Kein CAD/PCB direkt designen.** Erlaubt: Konzepte, Maße, Rechnungen, Teileauswahl, Datenblätter, Reviews, Erklärungen, Fehlersuche.
3. **PCB:** Schaltplan, Platzierung, Routing macht der Erbauer von Hand (kein Autorouter).
4. **Firmware/PC-App:** helfen, erklären, kleine Beispiele, reviewen, aber nicht alles allein schreiben.
5. **Keine KI-Bilder.**
6. AI Disclosure ins README (Erbauer formuliert, ich gebe Stichpunkte).
7. Jeder Journal-Eintrag max. 5 h + mind. 1 Bild. Am Session-Ende Stichpunkte geben.

## Arbeitsweise
- Chat Deutsch, Erklärungen **mittel** (bei Elektronik/Code das Warum). Repo-Doku Englisch (schreibt der Erbauer).
- Bei Design- und Geldentscheidungen fragen. Kostenoptimiert bleiben (AliExpress vor Amazon, nur 2 PCBA).
- Tägliche Erinnerung 15 Uhr (geplante Aufgabe in dieser Session).
- Am Ende jeder Session: Notizen aktualisieren, committen, pushen. Commit-Nachrichten Englisch, kurz.
