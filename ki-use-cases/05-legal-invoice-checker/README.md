# Use Case 5: Legal Invoice Checker – Kanzleirechnungen gegen Billing Guidelines prüfen

## Ziel

Ein GPT prüft Kanzleirechnungen gegen zuvor definierte Billing Guidelines –
u. a. Stundensätze, Caps, Budgets, administrative Tätigkeiten, Einsatz von KI.

**Output:** Abweichungsbericht je Rechnungsposition mit beziffertem
Kürzungsvorschlag und Entwurf einer E-Mail an die Kanzlei.

Weitere denkbare Kriterien: Reisezeit nur anteilig, keine Doppelbesetzung, keine
Einarbeitung neuer Mitarbeiter, ausreichende Detailtiefe, korrekte Anwendung
vereinbarter Fee Arrangements.

## Status quo (Pain Point)

1. Rechnungsprüfung erfolgt manuell, ist zeitaufwendig und je Prüfer:in
   unterschiedlich.
2. Keine LC-übergreifende Auswertung (Legal Spend, KPIs, Kanzleisteuerung).

## Mehrwert

1. Kostenkontrolle und konsistente Kürzungspraxis
2. Belastbare Verhandlungsbasis gegenüber Kanzleien
3. Datengrundlage für Kanzleisteuerung und Legal-KPIs
4. Vermeidung von Lizenzkosten für ein externes Legal-Spend-Tool

## Prozessschritte und Umsetzung

1. **Billing Guidelines definieren** →
   [billing-guidelines-vorlage.md](billing-guidelines-vorlage.md) füllen.
2. **Prompt bauen** → [system-prompt.md](system-prompt.md) als Startpunkt.
3. **Test mit 2–3 anonymisierten Echt-Rechnungen** →
   [test-protokoll.md](test-protokoll.md).
4. **Abweichungsbericht und Kürzungs-E-Mail verfeinern** (Formatwünsche direkt im
   Prompt nachziehen).
5. **Auswertung und Entscheidung über Regelbetrieb.**

## ⚠️ Good-2-Know (aus dem Use-Case-Steckbrief)

Billing Guidelines müssen den Kanzleien **vorab kommuniziert** werden – gekürzt
werden kann nur, was vereinbart ist.

## Ausbaustufen

- Strukturierte Rechnungsdaten (z. B. **LEDES-Format**) statt PDF – GitHub
  Copilot kann beim Bau eines LEDES-Parsers helfen.
- Automatischer Rechnungseingang über Power Automate.
- Spend-Auswertung über alle Rechnungen (Legal-KPIs, Kanzleivergleich) – Code
  Interpreter im GPT oder eigenes Auswertungsskript.
