# Interview: 120 Fragen (2026-11-01)

> Protokoll der Antworten vom Erbauer. Notiert von Claude. „→“ = Konsequenz/Notiz.

## Person & Rahmen
- Erfahrung: **Bastler** (hat Drucker umgebaut/repariert). Alter **13–15**. Land **Deutschland**.
- Programm: **Hack Club Fabricate** → Tier 1 (max. $500).
- Budget-Wunsch: 400–800 € → ⚠️ über Fabricate-Maximum.
- Zeitrahmen: 2–3 Monate. Rhythmus: täglich.
- Eigener Drucker: **Anycubic Kobra 2 Neo** (nur PLA zuverlässig, Probleme mit First Layer).
- Werkzeug: Lötkolben, Multimeter, Inbus/Schraubendreher, Crimpzange.
- 230-V-Hilfe: **Elektriker/Erwachsener vorhanden**.
- Standort: **eigenes Zimmer** → Filter, Rauchmelder, Sicherheit wichtig.

## Konzept
- Name: **Amethyst**.
- Kinematik: **CoreXY** („was das beste ist“; Vorbild Bambu H2D, Anycubic Kobra S1 Combo).
- Bauraum: **25 × 25 × 25 cm**. Außenmaß egal.
- **Geschlossen**. Deckel + Tür aus Glas/Acryl leicht **lila getönt**, Seiten dicht/blickdicht.
- Design: **komplett eigenes**.
- Düsen: **1 Kopf, 2 Düsen (H2D-Stil)**, je eigener Extruder. Hub-Mechanik: Claude schlägt vor.
  - (Verworfen: Laser 20–40 W, 8-Düsen-Toolchanger, Messer, Stiftplotter.)
- Extras: **Kamera**.
- Multicolor: **8–16 Spulen**, eigenes ACE-artiges System **plus** Adapter für Fremdsysteme; Features: Trocknen (65–70 °C), Auto-Nachladen, Fremdspulen, offenes Protokoll. Position egal.

## Material & Temperatur
- Materialien: PLA, PETG, ABS/ASA, TPU, PA/CF/GF.
- Hotend **350 °C**, Bett **120 °C**, Kammer **aktiv beheizt** (PTC + Lüfter).
- Druckteile: erst PETG (bzw. Printing Legion), später selbst in ASA neu drucken.
- Düsen 0,2–0,8, normal + gehärtet; **werkzeuglos wechselbar**. Filament 1,75 mm.

## Mechanik
- **MGN9/MGN12**-Schienen, **GT2 9 mm**, Ziel **~500 mm/s**.
- Z: **3 Spindeln + Auto-Tilt**.
- Rahmen: **Mix** (Alu-Profile innen, Paneele außen); Profile **zugeschnitten** bestellen; Paneele **gedruckt**.
- Kabelführung zum Kopf: wie Kobra S1 (Umbilical von hinten oben).
- Reinigung: Bürste + Poop-Chute + Reinigungsturm-Option + Abfallbehälter.
- Wartung: Kopf < 5 min zerlegbar, E-Fach aufklappbar, Wartungs-Makros.

## Elektronik
- Firmware **Klipper**, Host **CM4/CB1 auf eigenem Board**.
- **Eigenes Mainboard (KiCad 10)**, PCBA bei JLC/PCBWay, **Fallback-Board** als Backup.
  - PCB-Erfahrung: keine. ⚠️ Fabricate: Schaltplan, Platzierung, Routing **von Hand durch den Erbauer**.
- Treiber: „alles TMC5160“. XY: **echte AC/DC-Servos**, **24 V + 48 V** für XY.
- Toolhead: **CAN-Bus**.
- Bett-Probe: **Drucksensor in der Düse** (wie Kobra S1 / Bambu A1).
- Sensoren: Filament, Beschleunigung, Kammertemperatur, Verstopfung.
- Sicherheit: Thermal Runaway, Thermosicherung Bett, Rauchmelder.
- Heizbett + Druckplatte: **fertig kaufen**. Netzteil **Mean Well**, IEC-Buchse mit Schalter + Sicherung.
- Kühlung: Radial am Kopf + Aux-Lüfter; HEPA + Aktivkohle + optionale Abluft nach draußen; Lautstärke normal; **getrenntes E-Fach unten**.
- RGB: Kammerlicht, Außenkanten, Druckkopf, Statusfarben. Look: Technik + clean, Schwarz + Akzente (lila, grau, grün, blau, Farbverläufe).

## Software
- Touchscreen 5–7" (KlipperScreen), Moonraker/Mainsail **mit eigener GUI**, Web-App für Handy + PC.
- OrcaSlicer. Tailscale. Push: fertig, Fehler/Spaghetti, Filament leer.
- Kamera: Livestream, Timelapse, KI-Fehlererkennung, Erste-Schicht-Check.
- Auto-Kalibrierung: Mesh, Input Shaping, Flow/PA, Düsen-Offset XY. Startzeit egal.
- Spulen-ID: eigene NFC (OpenSpool-artig) + Bambu-RFID + manuell. **Spoolman** ja.
- Lizenz: Open Source.

## Zusammenarbeit
- CAD: Erbauer nutzt **Fusion 360**. Wunsch: Claude macht CAD, Erbauer schaut .3mf an. ⚠️ Fabricate-Regel verbietet das.
- Journal: Wunsch „komplett Claude“. ⚠️ Fabricate-Regel verbietet KI-Text im Journal/README.
- Fotos: Erbauer macht Fotos, falls Pflicht (→ ist Pflicht, jeder Eintrag).
- Erklärungen: **wenig**. Fragen bei: **Design + Geld**. Sicherheit: Claude maximal.
- Chat: Deutsch. Doku: Englisch.
- Git: direkt auf main. Autopilot täglich: **erst später**.
- Erbauer macht selbst: drucken, bauen/verkabeln, bestellen.
- Prioritäten: Qualität, Speed, Zuverlässigkeit, Show-Faktor. Erfolg = Benchy < 20 min + 8-Farben-Druck + ASA-Selbstreplikation.
- Wenn Budget eng: zuerst **zweite Düse** streichen. Phasen: „alles parallel“.
- Shops: Amazon.de / was Fabricate erlaubt.
