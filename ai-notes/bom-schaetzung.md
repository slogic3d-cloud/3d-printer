# BOM-Schätzung (Claude, 2026-11-02)

> ⚠️ Veraltet: gehört zum gestrichenen PC-Stats-Display.

> Nur Schätzung zur Budgetkontrolle. Die echte `BOM.csv` (mit Links, Versand, Notizen) legt der Erbauer selbst an, wenn der Schaltplan steht.
> Grant: **Tier 3 = max. $125**, kein Eigengeld.

| Posten | Menge | ca. USD | Notiz |
|---|---|---|---|
| JLC-PCB 2 Lagen, schwarz, ~100×60 mm | 5 | 5–8 | |
| JLC-PCBA Economic: Setup + Schablone | 1 | ~10 | Setup $8, Schablone $1.50 |
| JLC-Bauteile (RP2040, W25Q128, 12-MHz-Quarz, LDO, USB-C, USBLC6, Polyfuse, PCF8563 + 32k-Quarz, CR2032-Halter, Taster, MOSFET, Passive) | 2 Sätze | 8–12 | ~$4–6 pro Platine |
| JLC Extended-Part-Gebühr | ~5–7 Typen | 8–20 | $1.50–3 pro Typ, im Live-Angebot prüfen |
| JLC Versand + MwSt (DE) | | 15–25 | |
| 3,5" ST7796S SPI-Display (Amazon.de) | 1 | 15–22 | Begründung: verlässlicher Verkäufer/Rückgabe |
| CR2032 | 1 | 1 | |
| Buchsenleiste für Display (falls nicht bei JLC) | 1 | 1 | |
| Einschmelzmuttern + M2/M3-Schrauben + Standoffs | Set | 10–15 | Möglichst ein kleines Sortiment |
| Gummifüße | 4 | 2–3 | |
| PLA schwarz + lila (anteilig, ~100–150 g) | | 3–5 | Anteilig rechnen, falls Spule gekauft wird |
| **Summe** | | **~80–125** | knapp! |

## Sparhebel, falls es zu teuer wird
1. Bauteile mit „Basic“/„Preferred Extended“ bei JLC wählen (keine Ladegebühr)
2. Display doch von AliExpress (~$6–13)
3. RTC weglassen (Pico-RTC + Standby-Strom)

Quellen: JLCPCB PCBA-Preise (jlcpcb.com/help/article/pcb-assembly-price), eBay/Alibaba-Displaypreise (Stand 2026-11).
