# Fabricate-Regeln (recherchiert 2026-11-01)

> Notizen von Claude (KI-Assistent). Quelle: https://fabricate.hackclub.com/docs
> Regeln können sich ändern → vor dem Einreichen nochmal prüfen.

## Grant / Tiers
| Tier | Scraps | Stunden | Beispiel | Max. Grant |
|---|---|---|---|---|
| **1** | 1000 | ~67+ | **custom 3D printer**, CNC | **$500** |
| 2 | 500 | ~34–66 | Roboterarm, Drohne mit eigenem FC, Linux-SBC | $250 |
| 3 | 250 | ~17–33 | Dev-Board, Smart-Home-Hub | $125 |
| 4 | 100 | ~8–16 | Macropad, USB-Hub | $50 |

- 10 Scraps = $5. Übrige Scraps → Chips → Belohnungen auf dem „Path“ (Werkzeug usw.).
- Tier hängt von Komplexität **und** Politur/Doku ab.
- Projekt muss **kostenoptimiert** sein (Non-Profit). Keine Extra-Teile „für später“.
- Amazon nur wenn nötig → AliExpress (z. B. Trianglelab für Druckerteile) bevorzugt.
- 3D-Druckteile: **Printing Legion** druckt kostenlos (Filament zahlt Hack Club, nur Versand aus Grant).
- PCB: JLCPCB. **Kein ENIG**, kein Edge-Plating nur für Optik.
- Vor eigenen Käufen mit späterer Erstattung: erst in #fabricate fragen.

## Pflicht beim Einreichen (Design-Ship)
- Original (eigene Note, kein Klon).
- Komplette CAD-Assembly **inkl. Elektronik** als **.STEP** + Quelldatei (.f3d/.f3z oder öffentlicher Onshape-Link).
- Firmware vorhanden (darf minimal/ungetestet sein, muss ernst gemeint sein).
- Design von jemand anderem gegengecheckt.
- `BOM.csv` im Root **mit Links** (inkl. Versand, Druckteile anteilig, eigene Teile mit Preis + Notiz).
- PCB-Quellen (.kicad_pro, .kicad_sch, .kicad_pcb, gerbers.zip).
- Ordner: `CAD/`, `PCB/`, `firmware/`.
- README: Beschreibung, Warum, Bilder, Screenshot 3D-Modell, Screenshot PCB, Verkabelungsplan, BOM-Tabelle am Ende.
- Dateien > 25 MB → Git LFS.

## Journal (JOURNAL.md im Root)
- Frontmatter: title, github, description, created_at, total_time.
- Einträge `## Datum: Titel`, **jeder Eintrag max. 5 h**, **jeder Eintrag braucht mindestens 1 Bild**.
- Auch Fehlschläge/Sackgassen + Gedanken dokumentieren.
- Zählt: CAD/KiCad-Zeit, Recherche (Datenblätter), Kunst. Zählt nicht: YouTube schauen.
- Muss von Anfang an geführt werden (fast fertige Projekte werden nicht angenommen).

## ⚠️ KI-Regeln (sehr wichtig für unsere Zusammenarbeit)
**Verboten (→ Ablehnung / möglicher Bann):**
- KI-PCB-Design-Software/Plugins, KI-CAD-Software/Plugins
- KI-Text in README.md und JOURNAL.md
- KI-generierte Bilder/Grafiken
- Komplett KI-generierte Firmware
- „Using AI to directly design your project“ = Betrug

**Erlaubt:** KI für Ideen, Troubleshooting, Beratung, Hilfe beim Firmware-Schreiben, Debugging — **muss im README offengelegt werden** („AI Disclosure“).

**Zusätzlich PCB:** Kein Autorouter. Routing, Schaltplan und Footprint-Platzierung **von Hand**.

## Build-Ship (nach dem Bauen)
- Repo aktualisieren + Foto im README
- 1-min-Video (YouTube, darf unlisted sein)
- Online teilen (Reddit bevorzugt, oder Printables)
- Ohne physischen Bau keine Path-Belohnungen.
