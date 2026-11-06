# Claude-Arbeitslog (NICHT das Fabricate-JOURNAL)

> Das ist **Claudes** Log. Das echte `JOURNAL.md` im Root schreibt der Erbauer selbst (Fabricate-Regel: kein KI-Text, jeder Eintrag max. 5 h + mind. 1 Bild).

## 2026-11-02: Neustart
- Drucker-Projekt gestrichen, Name Amethyst bleibt.
- Neues Interview gestartet (8/120 Fragen): Eingabe + Anzeige, USB-C, 3–4 Wochen.
- Stichpunkte für dein JOURNAL (selbst formulieren!): Warum der Drucker gestrichen wurde, was das neue Projekt können soll.

## 2026-11-02: Interview bis Frage 36
- Konzept steht: PC-Stats-Display mit 3,5"-TFT, Pico auf eigener Platine, Keil-Gehäuse.
- Spotify gestrichen. RTC dazu. Gigabyte-Board: USB-Standby-Strom prüfen (ErP).
- Stichpunkte für dein JOURNAL (selbst formulieren + Bild!): Konzeptentscheidung, Skizze vom Keil-Gehäuse.

## 2026-11-02: Interview bis Frage 60
- Pico-Modul verworfen → RP2040 direkt auf eigener Platine, JLC bestückt. Tier 3.
- PC-App-Konzept + Sensorquellen (LibreHardwareMonitor/PawnIO unter Windows) festgelegt.
- Stichpunkte für dein JOURNAL: Warum RP2040 statt Pico (USB-C-Problem), Recherche zur CPU-Temperatur unter Windows. Bild: Screenshot vom RP2040-Datenblatt oder eine Skizze.

## 2026-11-02: Interview bis Frage 80
- Gehäuse-Details, 2-Lagen-PCB, RTC PCF8563, Firmware-Verhalten (Boot, Timeout, Update) festgelegt.
- Stichpunkte für dein JOURNAL: Gehäuseteilung (Front + Rückschale, warum), 30°-Winkel. Bild: Handskizze vom Keil mit Maßen.

## 2026-11-02: Interview bis Frage 100
- ST7796S statt ILI9488, 2 bestückte Platinen (Kostenregel), Tools festgelegt (PlatformIO, TFT_eSPI, pystray/tkinter, JSON-Protokoll).
- Stichpunkte für dein JOURNAL: Vergleich ILI9488 und ST7796S (warum gewechselt), Amazon-Begründung. Bild: Screenshot vom Display-Datenblatt oder Produktfoto (eigener Screenshot, kein KI-Bild).

## 2026-11-02: Interview fertig (120/120), Repo aufgeräumt
- Drucker-Notizen gelöscht, Ordner CAD/ PCB/ firmware/ pc-app/ angelegt, BOM-Schätzung (~$80–125).
- Tägliche Erinnerung 15 Uhr eingerichtet.

## 2026-11-05: Umstieg auf Dev-Board
- Repo heißt jetzt dev-board, nur noch `main`. KiCad-Dateien des Erbauers nach `PCB/` verschoben, pc-app/ entfernt, versehentliche Plugin-Kopien in ai-notes/ gelöscht.
- LICENSE: CC BY-NC-SA 4.0 (Wunsch: nicht verkaufen, privat nutzen + weiterentwickeln).
- Schaltplan-Review: 7 kritische Fehler, v. a. Stromversorgung und EN/Auto-Reset.
- Stichpunkte für dein JOURNAL: Warum Dev-Board statt Display, erster Schaltplan + Platzierung, was das Review gefunden hat. Bild: Screenshot vom Schaltplan und vom PCB-Layout.

## 2026-11-05: Repo-Struktur nach Fabricate
- `.gitignore` (KiCad-Backups, .kicad_prl), `BOM.csv` im Root (Bauteile aus dem Schaltplan, Preise/Links leer → Erbauer füllt aus), .kicad_prl nicht mehr getrackt.
- Board-Korrektur abgelehnt (Fabricate: Schaltplan/Layout macht der Erbauer).
- Offen beim Erbauer: README-Titel, JOURNAL-Frontmatter-Link auf dev-board ändern, KiCad-Projekt ggf. per „Speichern unter“ in `amethyst` umbenennen.

## 2026-11-06: PCB fertig, JLC-Angebot
- Mehrere Review-Runden: Schaltplan korrekt, C6-GND gefixt, Wärme-Vias 0,2→0,3 mm, Gerber vollständig neu exportiert.
- Repo: STEP, gerbers.zip, production/ (Fabrication Toolkit), BOM.csv mit JLC-Preisen; CAD/, firmware/, PINOUT.md entfernt.
- JLC-Teile zugeordnet; Hinweis: Economic statt Standard, PCBA 2 statt 5, günstiger Versand.
