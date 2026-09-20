# Testfall 2 — Drehbuch: vage Antworten (Prozess „Monatsbericht erstellen")

**Anleitung für Tester:innen:** Antworte zunächst NUR mit den vagen Sätzen
(Spalte „Erste Antwort"). Die konkreten Angaben (Spalte „Erst auf Nachhaken")
gibst du **nur**, wenn die KI gezielt nachfragt — z. B. nach dem letzten
konkreten Fall. Fragt sie nicht nach, bleibt es bei der vagen Antwort.
So wird geprüft, ob die KI Regeln herausarbeitet statt Vagheit zu schlucken.

## Eckdaten (bei Bedarf nennen)
Bereich: Controlling, Kürzel CO, ID CO-04. Name: Alex. Monatlich, immer zum
5. Arbeitstag. Dauer: „so ein bis zwei Tage, je nachdem". Systeme: Excel, SAP,
PowerPoint, Outlook.

## Drehbuch

| Thema | Erste Antwort (vage) | Erst auf Nachhaken (konkret) |
|---|---|---|
| Auslöser | „Das mache ich halt jeden Monat irgendwann am Anfang." | „Stichtag ist der 5. Arbeitstag, weil dann die SAP-Buchungen des Vormonats vollständig sind. Vorher anfangen bringt nichts, dann fehlen Buchungen." |
| Datenquellen | „Ich zieh mir die Zahlen halt zusammen." | „Umsätze aus SAP-Report Y41, Kosten aus der Kostenstellen-Excel vom Team, Headcount per Mail von HR — HR muss ich fast jeden Monat erinnern." |
| Welche Zahlen in den Bericht kommen | „Kommt drauf an, was gerade wichtig ist. Das entscheide ich nach Gefühl." | „Letzten Monat habe ich die Reisekosten reingenommen, weil sie mehr als 10 % über Plan lagen. Alles, was mehr als 10 % vom Plan abweicht, kommt rein — plus alles, wonach die Geschäftsführung im Vormonat gefragt hat." |
| Kommentierung der Abweichungen | „Ich schreib halt kurz was dazu, das hat sich so eingespielt." | „Zu jeder roten Zahl: Ursache + ob einmalig oder dauerhaft + was dagegen getan wird. Ohne diese drei Punkte fragt die Geschäftsführung sowieso nach." |
| Qualität | „Wenn sich keiner beschwert, war er gut." | „Konkret: keine Rückfragen zur Herkunft einer Zahl, und der Bericht ist vor der GF-Sitzung am 7. Arbeitstag da. Einmal war er später — seitdem blockt mir mein Chef den 5. und 6. im Kalender." |
| Ausnahmen | „Eigentlich läuft das immer gleich." | „Beim Jahresabschluss (Januar) kommt das Vorjahres-Gesamtblatt dazu und ich brauche eher drei Tage. Und wenn SAP am Stichtag hängt, nehme ich die Zahlen vom Vortag und schreibe das als Fußnote rein." |
| Kopfwissen-Fragen | Ehrlich und konkret antworten (frei erfinden im Rahmen des Szenarios) — hier wird normale Tiefe getestet, nicht Vagheit. | — |
| Schmerzpunkte | „Das ewige Zahlen-Zusammensuchen nervt, und die HR-Mail kommt nie pünktlich." | — |

## Bewusst offen lassen (auf Nachfrage: „Weiß ich nicht")
- Wer den Bericht außer der Geschäftsführung noch liest
- Wie lange die einzelnen Teilschritte genau dauern
