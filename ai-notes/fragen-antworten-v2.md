# Interview v2: einfaches Projekt (ab 2026-11-02)

> Protokoll von Claude. Das alte Drucker-Interview steht in `fragen-antworten.md` (archiviert).

## Runde 1–2 (8/120)
1. Verhältnis zum Drucker: Name **Amethyst** bleibt, **Drucker wird gestrichen** (zu teuer, zu kompliziert).
2. Tier: weiß nicht → Claude schlägt vor.
3. Richtung: erst alles (Eingabe, Anzeige, Smart Home/Sensor, Spiel) → dann **Spiel + Sensor gestrichen** → **Eingabe + Anzeige**.
4. Zeit: **3–4 Wochen**.
5. Konzept-Kombi: neu fragen (ohne Spiel/Sensor).
6. Ort: egal.
7. Strom: **USB-C**.
8. Programmieren: **bisschen** (Arduino-Beispiele/Python-Grundlagen).

Runde 3 (Konzept, Eingabe-Elemente, Display, RGB) wurde vom Erbauer abgebrochen → nachfragen, was geändert werden soll.

## Runde 3–9 (36/120)
9. Konzept: **PC-Stats-Display**.
10. Eingabe-Elemente: keine Präferenz → später: **keine Bedienung**.
11. Display: Claude entscheidet → dann gewählt: **3,5" TFT 320×480** (ILI9488, SPI).
12. RGB: **keins**.
13. Infos: **CPU/GPU-Last + Temp, RAM + Speicher, Uhrzeit/Datum, Internet-Speed + Ping**. (Spotify erst gewählt, dann **gestrichen**.)
14. Verbindung: **USB-Kabel** (USB-Seriell, Python-Programm am PC).
15. PC-OS: **Windows + Linux**, Mac wäre schön → PC-Programm plattformübergreifend (Python + psutil).
16. Bedienung: **keine** → Seiten wechseln automatisch.
17. Seitenwechsel-Intervall: **am PC einstellbar**.
18. Display: **3,5" TFT 320×480**.
19. MCU: Claude → **Raspberry Pi Pico (RP2040-Modul)** auf eigener Trägerplatine.
20. Firmware-Sprache: Claude → **Arduino C++** (MicroPython zu langsam für 480×320). PC-Seite: **Python**.
21. Gehäuseform: **schräger Keil**.
22. CAD: **Fusion 360**.
23. Druck: **selbst, Kobra 2 Neo, PLA**.
24. Verbindung: **Schrauben + Einschmelzmuttern**.
25. Farbe: **Schwarz + Lila**.
26. UI-Stil: **clean/modern**.
27. Graphen: **nur aktuelle Werte** (Zahlen + Balken).
28. Standby: **Uhr**.
29. Strom bei PC aus: Erbauer fragt, ob Gigabyte Z170X-UD5 TH USB-Standby-Strom liefert → Claude: wahrscheinlich mit BIOS **ErP = Disabled**, Erbauer soll messen.
30. Helligkeit: **am PC einstellbar** (PWM an Backlight).
31. Netz: **Ping ständig + aktueller Traffic + gelegentlicher Speedtest**.
32. Spotify: **raus**.
33. RTC: **RTC-Chip einplanen** (z. B. DS3231 + CR2032).
34. Platine: Claude entscheidet → Trägerplatine: Pico, USB-C, ESD-Schutz, RTC + Knopfzelle, Display-Anschluss, Backlight-Transistor, Befestigungslöcher.
35. KiCad: **mal reingeschaut**.
36. USB: **USB-C-Buchse auf eigener Platine** → ⚠️ Pico-USB-Datenleitungen liegen auf Testpads TP2/TP3 unten, Anbindung muss geklärt werden.

## Runde 10–15 (60/120)
37. Pico-USB-Problem → **RP2040 direkt auf eigener Platine** (Quarz, Flash, LDO selbst).
38. SMD-Löten: **JLC bestückt (PCBA)**.
39. Display-Anschluss: Claude → **Platine direkt hinter dem Display, Modul per Stiftleiste aufgesteckt**.
40. Touch: **ohne**.
41. Tasten: **BOOT + RESET**.
42. Flash: Claude → **16 MB (W25Q128)**.
43. PCB-Farbe: **schwarz**.
44. Status-LED: **keine**.
45. Tier: egal → Claude: **Tier 3 (max. $125)**.
46. Eigengeld: **nein, nur Grant**.
47. Vorhanden: nur **USB-C-Kabel** → Filament, Inserts, Schrauben kommen in die BOM.
48. Journal: **Claude erinnert + gibt Stichpunkte**, Erbauer schreibt selbst.
49. PC-App: „egal, aber benutzerfreundlich“ → Claude: **Tray-Icon + kleines Einstellungsfenster, Gerät automatisch finden**.
50. Autostart: **nein, manuell**.
51. GPU: **AMD**.
52. CPU-Temp Windows: Claude recherchiert → **LibreHardwareMonitor (mit PawnIO) + Remote Web Server, Python liest `localhost:8085/data.json`**; Linux: psutil + amdgpu-sysfs; Mac: nur Last.
53. Einstellungen: **Seitenwechsel-Zeit, Helligkeit, Seiten an/aus, Farbschema**.
54. Verteilung: **.exe (PyInstaller) für Windows + Python-Skript für Linux/Mac**.
55. Ping-Ziele: **am PC einstellbar**.
56. Speedtest-Intervall: **am PC einstellbar**.
57. UI-Sprache: **umschaltbar (DE/EN)**.
58. Ausrichtung: **quer 480×320**.
59. Layout: **2–4 Kacheln pro Seite**.
60. Uhr-Format: **am PC einstellbar**.

## Runde 16–20 (80/120)
61. Neigung: **~30°**.
62. USB-C-Ausgang: **Seite**.
63. Display-Einfassung: **gedruckte Blende**.
64. Füße: **Klebe-Gummifüße**.
65. Logo/Name: **nichts**.
66. BOOT/RESET-Zugang: **kleines Loch (Büroklammer)**.
67. Teilung: Claude erklärt → 69.
68. Höhe: **so flach wie möglich**.
69. Teilung: **Front + Rückschale**.
70. Fusion-Level: **Grundlagen**.
71. PCB-Befestigung: **eigene Schrauben/M2-Standoffs**.
72. Lizenz: **Open Source, Code MIT, Hardware CERN-OHL**.
73. Lagen: Claude → **2 Lagen** (Fallback 4).
74. RTC: Claude → **PCF8563 + 32,768-kHz-Quarz** (PC synchronisiert eh).
75. KiCad lernen: **alles zusammen** (Hack Club Guides, YouTube, Learning by doing + Claude). Hinweis: Videoschauen zählt nicht als Journal-Zeit.
76. Referenz: **RP2040 „Hardware design with RP2040“ als Vorlage lesen**, Schaltplan selbst zeichnen.
77. Boot: **Amethyst-Bootlogo**.
78. Verbindungsabbruch: **nach 5 s auf Uhr + Hinweis „PC getrennt“**.
79. Farbschema/Sprache: **im Flash des Geräts speichern**.
80. Firmware-Update: **UF2 per Drag & Drop + Update-Knopf im PC-Programm**.

## Runde 21–25 (100/120)
81. Reihenfolge: **PCB zuerst** (Lieferzeit JLC), parallel Gehäuse + Software.
82. Breadboard-Prototyp: **nein**.
83. Zeit: **5–10 h/Woche** (→ 15–40 h gesamt, passt zu Tier 3).
84. Design-Review (Pflicht): **weiß noch nicht** → Claude erinnert vor Einreichen.
85. Display-IC: **ST7796S** (statt ILI9488).
86. Display-Shop: Amazon.de → Claude weist auf Fabricate-Regel hin → 90.
87. JLC-Anzahl: erst 5 bestückt → Claude weist auf Kostenregel hin → 89.
88. Insert-Werkzeug: weiß nicht → Claude: **normale Lötspitze reicht**.
89. JLC: **2 bestückt** (+ 3 unbestückte Platinen).
90. Display: **Amazon.de mit Begründung**.
91. Bezahlung: **Fabricate-Karte/HCB**.
92. Claude-Rolle: **Schaltplan-Reviews, Code-Hilfe, CAD-Feedback, BOM + Preise**.
93. Amazon-Begründung: **verlässlicher Verkäufer/Rückgabe** (AliExpress-Displayvarianten oft falsch beschrieben).
94. Display-Lib: **TFT_eSPI**.
95. IDE: **PlatformIO in VS Code**.
96. Protokoll: Claude → **JSON-Zeilen über USB-CDC (ArduinoJson)**.
97. Python: **Variablen, if, Schleifen, Funktionen** (keine Klassen, noch keine pip-Erfahrung).
98. Git: **GitHub Desktop/Web**.
99. GUI: Claude → **pystray + tkinter**.
100. GUI-Stil: **System-Standard**.

## Runde 26–30 (120/120) ✅ Interview fertig
101. USB-Schutz: **ESD-Diode USBLC6 + Polyfuse 500 mA**.
102. Erster Test: **Multimeter + Powerbank** (nicht direkt am PC).
103. Testpunkte: **5 V, 3,3 V, GND**.
104. Passung: **KiCad-STEP in Fusion + Testdruck der Front mit echtem Display**.
105. Repo: **umbenennen (auf GitHub, macht der Erbauer) + neu strukturieren, Drucker-Kram löschen**.
106. Video: **später**.
107. Teilen: „Fabricate“ → Claude: zusätzlich Reddit/Printables-Post nötig (Build-Ship).
108. AI-Disclosure: **Claude gibt Stichpunkte**, Erbauer formuliert.
109. Repo-Name: **amethyst-pc-stats**.
110. Alte Drucker-Notizen: **komplett löschen**.
111. `.claude-flow/` + `.swarm/`: **drin lassen**.
112. Ordner: **CAD/ PCB/ firmware/ pc-app/ angelegt** (.gitkeep).
113. Nächster Schritt: **KiCad mit Claude starten → Journal-Eintrag am Ende der Session → morgen weiter**.
114. BOM-Schätzung: **jetzt** (→ `bom-schaetzung.md`).
115. Check-ins: **Claude erinnert**.
116. Erklärungen: **mittel** (bei Elektronik/Code das Warum).
117. Erinnerung: **täglich**.
118. Uhrzeit: **15:00** (deutsche Zeit).
119. KiCad: **10 installiert**.
120. KiCad-Start: **Projekt anlegen + Schaltplan in Blöcke teilen**.
