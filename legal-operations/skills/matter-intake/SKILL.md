---
name: matter-intake
description: Führt eine Matter-Steuerung für Rechtsabteilungen ein — vereinheitlichte Matterliste (Status, Priorität, Verantwortlichkeit, Fristen), Intake-Mechanik über Outlook-Kategorien, Wochenroutine für den Team-Jour-Fixe und Fristen-/Auslastungsbericht. IMMER verwenden, wenn der Nutzer Mandats-/Matterlisten, Intake-Prozesse, Fristenübersichten oder Auslastungstransparenz aufbauen will.
---

# Matter-Intake-System

Macht die Arbeit einer Rechtsabteilung steuerbar: Was liegt an, wer hat es, wie dringend ist es, wann ist es fällig. Ziel ist risikobasierter, bewusster Kapazitätseinsatz statt Zuruf-Betrieb — umsetzbar mit M365-Bordmitteln (Excel/Lists + Outlook), ohne Tool-Beschaffung.

## Bausteine

### 1. Matterliste (das eine Register)
Lege eine Liste mit genau diesen Spalten an — mehr Spalten nur bei nachgewiesenem Bedarf:

| Spalte | Inhalt |
|---|---|
| Matter-ID | `JJJJ-NNN`, fortlaufend |
| Kurztitel | max. 8 Worte, verständlich ohne Kontext |
| Fachbereich / Anfragender | wer braucht das Ergebnis |
| Typ | Vertrag, Anfrage, Streit, Projekt, Gremium … |
| Status | Neu / In Arbeit / Wartet auf Dritte / Erledigt |
| Priorität | A (rechtlich/wirtschaftlich kritisch), B (wichtig, terminiert), C (Routine) |
| Verantwortlich | genau eine Person |
| Frist | hartes Datum oder leer — nie „asap" |
| Nächster Schritt | ein Satz, beginnt mit Verb |

**Befüllungsregel:** Steuerungsrelevante Matters zuerst — nicht rückwirkend alles erfassen, sondern ab Stichtag alles Neue plus die laufenden A- und B-Matters.

### 2. Intake-Mechanik (Outlook-Kategorien als Signal)
- Eine Outlook-Kategorie (z. B. `LEGAL-INTAKE`) markiert eingehende Anfragen als aufzunehmen.
- Feste Tageszeit (z. B. 16:30): markierte Mails in die Matterliste übertragen, Kategorie auf `ERFASST` wechseln.
- Eingangsbestätigung an den Anfragenden mit Matter-ID und realistischem Zeitfenster — das beendet Nachfass-Mails.
- Was keine Matter wird (Kurzauskunft unter 15 Minuten), wird nicht erfasst — die Liste ist ein Steuerungs-, kein Zeiterfassungsinstrument.

### 3. Wochenroutine (Jour-Fixe-Agenda, 15 Minuten)
1. Neue Matters seit letzter Woche (nur A und B einzeln, C als Zahl)
2. Fristen der nächsten 14 Tage
3. Blockierte Matters („Wartet auf Dritte" > 2 Wochen)
4. Kapazität: Wer ist überlastet, was wird umverteilt oder herabpriorisiert
5. Erledigte abhaken (Motivation, dann Archiv)

### 4. Fristen- & Auslastungsbericht (Ausbaustufe)
Wöchentlich automatisch oder manuell erzeugt, eine Seite: Fristen der nächsten 14 Tage sortiert nach Datum, offene Matters je Verantwortlichem (Anzahl nach Priorität), Blockiertes, Trend zur Vorwoche. Empfänger: Team + Leitung.

## Workflow bei Einführung

1. **Schema anpassen:** Spalten und Prioritätsdefinitionen mit dem Nutzer auf den Kontext zuschneiden (Interview: Teamgröße, Matter-Typen, bestehende Listen).
2. **Pilot definieren:** 4–6 Wochen, ein Teilbereich oder das ganze Team; Erfolgskriterien vorab festlegen (z. B. „keine verpasste Frist, Jour Fixe unter 20 Minuten").
3. **Pilot-Review dokumentieren:** Nach dem Pilot ein 1-Pager: Was hat funktioniert, was nicht, Empfehlung (ausrollen / anpassen / verwerfen) mit Begründung.

## Übergabe
Liefere: Matterlisten-Vorlage (als Tabelle), Intake-Regelwerk (halbe Seite), Jour-Fixe-Agenda, Berichtsformat, Pilot-Review-Template. Echte Matterdaten bleiben lokal beim Nutzer — in Beispiele gehören nur fiktive Einträge (siehe Testakte).
