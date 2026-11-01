# Zusammenfassung – Projektstand Amethyst

_Letztes Update: 2026-11-01 (Session 1)_

## Status
Phase 0: **Planung**. Interview (120 Fragen) erledigt, Fabricate-Regeln recherchiert. Noch kein CAD, PCB oder Teil bestellt.

## Festgelegtes Konzept
- Geschlossener **CoreXY**, Bauraum **250 × 250 × 250 mm**, Ziel ~500 mm/s
- **1 Kopf / 2 Düsen** (H2D-Stil, inaktive Düse wird angehoben), je eigener Extruder, 350 °C, werkzeuglose Düsen
- Düsen-Drucksensor als Bett-Probe (wie Kobra S1 / A1)
- MGN9/12-Schienen, GT2 9 mm, Z: 3 Spindeln + Z-Tilt
- Fertiges Heizbett (120 °C) + PEI-Federstahl, Mean-Well-Netzteil
- Klipper, eigenes Mainboard mit CM4/CB1-Slot, CAN-Toolhead
- Kamera, KlipperScreen 5–7", Mainsail/Moonraker mit eigener GUI, Tailscale, Spoolman
- HEPA + Aktivkohle, E-Fach unten, RGB-Status, lila getönte Tür/Deckel, schwarzes Design mit Farbakzenten
- Multicolor 8–16 Spulen mit Trockner, offenes Protokoll

## ⚠️ Konflikte, die der Erbauer entscheiden muss
1. **Budget:** Fabricate zahlt max. **$500** (≈ 430–460 €), Wunsch 400–800 €. Der Gesamtwunsch (Servos, 48 V, 2 Düsen, Kammerheizung, 8–16-Spulen-System) liegt grob bei **900–1500 €**.
2. **KI-Regeln:** Claude darf weder CAD noch PCB designen und keinen Text für README/JOURNAL schreiben. Der Erbauer muss das selbst machen; Claude ist Mentor, Rechner, Reviewer und Rechercheur.
3. **Kostenoptimierung ist Pflicht:** Echte AC-Servos, alles TMC5160 und ein Fallback-Board sind bei Reviewern schwer zu rechtfertigen.

## Empfohlener Zuschnitt (Vorschlag, noch nicht bestätigt)
**Fabricate-Projekt 1 = Amethyst-Drucker (Tier 1, ≤ $500):**
- Normale NEMA17-Stepper (z. B. LDO/Moons'), 24 V; Board bekommt Step/Dir-Header → Servos später möglich
- TMC2209 für Z/E, TMC2240/5160 für XY
- Eigenes Mainboard **statt** zusätzlichem Fallback-Board (spart Geld); als Plan B ein günstiges Board erst bei Bedarf
- 2. Düse: Mechanik + Anschlüsse vorsehen, zweites Hotend nur, wenn das Budget reicht (laut Erbauer zuerst streichen)
- Kammerheizung: Anschluss + Halterung vorsehen, PTC später
- Druckteile über Printing Legion (kostenlos, ASA möglich?) → löst auch das Kobra-2-Neo-Problem

**Fabricate-Projekt 2 = Multicolor-Einheit mit Trockner (eigenes Projekt, Tier 2/3).**

## Grobe Kostenschätzung Drucker (Schätzwerte, noch nicht recherchiert)
| Gruppe | € (ca.) |
|---|---|
| Alu-Profile zugeschnitten + Verbinder + Schrauben | 70 |
| MGN-Schienen (X + 2×Y + 3×Z-Führung) | 70 |
| 5–6 Stepper + 3 Spindeln + Riemen/Pulleys/Lager | 110 |
| Heizbett 250 + PEI + SSR + Thermosicherung | 70 |
| Hotend(s) + Extruder (1×, 2. optional +70) | 70 |
| Netzteil Mean Well 24 V + IEC-Buchse | 45 |
| Eigenes Mainboard (PCB + PCBA JLC) + CB1/CM4 | 90 |
| Toolhead-Board (CAN), Sensoren, Lüfter, Kabel | 60 |
| Display, Kamera, LEDs | 50 |
| Acryl-Tür/Deckel, Filter, Versand Printing Legion | 50 |
| **Summe** | **~685 € (ohne 2. Düse)** |

→ Noch zu teuer für $500. Einsparideen: Klipper-Host = vorhandener alter Rechner/Pi, Display weglassen (Web-UI reicht), günstigere Schienen, Bauraum 220³.

## Nächste Schritte
1. Erbauer entscheidet über Budget und Zuschnitt (siehe Konflikte)
2. Erbauer legt JOURNAL.md-Eintrag #1 an (Planung/Recherche, mit Bild, z. B. Skizze oder Screenshot)
3. Gemeinsam: Konzeptskizze Rahmen + Kinematik (Erbauer zeichnet in Fusion, Claude liefert Maße/Rechnungen)
4. Teileliste konkretisieren mit echten Links (AliExpress/Trianglelab) → `BOM.csv`
5. KiCad-Lernpfad: kleines Testboard oder direkt Toolhead-Board als Einstieg
6. Ordner anlegen: `CAD/`, `PCB/`, `firmware/`

## Offene Fragen
- Druckt Printing Legion auch ASA/PETG?
- Welches fertige Heizbett (Maße passend zu 250³)?
- Dual-Düsen-Hubmechanik: Servo vs. Solenoid vs. Cam (Claude recherchiert, Erbauer entscheidet)
