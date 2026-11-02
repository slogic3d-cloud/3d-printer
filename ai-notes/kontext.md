# Kontext für Claude (bei jeder Session zuerst lesen)

## Projekt
**Amethyst**: jetzt ein **einfaches Gerät** (USB-PC-Stats-Display) aus Elektronik + 3D-Gehäuse + Code. Der Drucker ist seit 2026-11-02 gestrichen. Stand: `kontext-zusammenfassung.md`.
Erbauer: Teen (13–15) aus Deutschland, gefördert über **Hack Club Fabricate** (Tier noch offen).
Repo: github.com/slogic3d-cloud/3d-printer, Branch `main`, direkt pushen erlaubt.

## Dateien
- `ai-notes/kontext.md`: diese Datei (Regeln für mich)
- `ai-notes/zusammenfassung.md`: aktueller Projektstand, Entscheidungen, offene Punkte → **nach jeder Session aktualisieren**
- `ai-notes/fragen-antworten.md`: Protokoll des 120-Fragen-Interviews
- `ai-notes/fabricate-regeln.md`: Programmregeln
- `ai-notes/session-log.md`: kurzes Log, was ich pro Session gemacht habe (≠ Journal!)
- `JOURNAL.md`: **gehört dem Erbauer**, ich schreibe dort keinen Inhalt
- `README.md`: **gehört dem Erbauer**, ich schreibe dort keinen Inhalt

## ⚠️ Harte Regeln (Fabricate, sonst Ablehnung/Bann für den Erbauer)
1. **Keinen Text in README.md oder JOURNAL.md schreiben.** Ich darf Struktur-Tipps und Feedback geben und auf Rechtschreibung hinweisen, aber der Text kommt vom Erbauer.
2. **Kein CAD/PCB direkt designen.** Kein generiertes STEP/3MF/KiCad-Layout als Projektdatei. Erlaubt: Konzepte, Maße, Rechnungen, Teileauswahl, Datenblätter, Reviews von *seinen* Dateien, Erklärungen, Fehlersuche.
3. **PCB:** Schaltplan, Platzierung und Routing macht der Erbauer selbst von Hand (kein Autorouter). Ich erkläre, prüfe und finde Fehler.
4. **Firmware/Klipper-Config:** Ich darf helfen, aber nicht alles allein schreiben. Der Erbauer schreibt mit, ich erkläre und reviewe.
5. **Keine KI-Bilder/Grafiken.**
6. Der Erbauer muss eine **AI Disclosure** ins README schreiben (selbst formuliert).
7. Jeder Journal-Eintrag ist max. 5 h lang und hat mindestens 1 Bild. Ich erinnere ihn daran.

## Arbeitsweise
- Chat auf **Deutsch**, kurz, wenig Erklärung. Repo-Doku ist Englisch (schreibt der Erbauer).
- **Bei Design- und Geldentscheidungen fragen** (AskUserQuestion). Sicherheit entscheide ich maximal streng.
- Sicherheit: Er ist 13–15 und der Drucker steht im Zimmer. 230-V-Arbeiten nur mit dem Elektriker/Erwachsenen. Thermal Runaway, Thermosicherung, Rauchmelder und Filter sind Pflicht.
- Kostenoptimiert bleiben (Fabricate-Pflicht): AliExpress/Trianglelab vor Amazon, Druckteile über Printing Legion.
- Erbauer-Drucker: Kobra 2 Neo (PLA, First-Layer-Probleme).
- Am Ende jeder Session: `zusammenfassung.md` + `session-log.md` aktualisieren, committen, pushen.
- Commit-Nachrichten: Englisch, kurz.
