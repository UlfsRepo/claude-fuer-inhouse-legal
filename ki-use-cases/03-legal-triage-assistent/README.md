# Use Case 3: Legal-Triage-Assistent

## Ziel

Ein GPT strukturiert eingehende Anfragen an die Rechtsabteilung:

- Sachverhalt in Kurzform
- Rechtsgebiet
- erkennbare Fristen und Dringlichkeit
- fehlende Informationen und Unterlagen (als Rückfragenliste **inkl. E-Mail-Entwurf**)
- Kategorisierungsvorschlag nach Matter-Schema (z. B. Neu / kritisch / Frist / warten)

**Wieso:** Die Triage-Logik ist zugleich die fachliche Vorarbeit für das geplante
Intake über Ticketing-System.

## Status quo (Pain Point)

1. Anfragen sind oft unvollständig; Nachfassen kostet Zeit und verzögert die Bearbeitung.
2. Priorisierung und Zuständigkeit je Anfrage unklar oder werden manuell geklärt.
3. Intake-System existiert noch nicht, Triage-Kriterien sind nicht definiert.

## Mehrwert

1. Schnellere Qualifizierung eingehender Anfragen; weniger Rückfrageschleifen
2. Einheitliche Priorisierung im Team
3. Fachlich validierte Triage-Logik als Blaupause für das Ticketing-Intake

## Prozessschritte und Umsetzung

1. **Kategorien- und Prioritätslogik entwickeln** →
   [triage-logik.md](triage-logik.md) im Team abstimmen und füllen.
2. **Prompt-Entwurf bauen** → [system-prompt.md](system-prompt.md) als Startpunkt,
   im Workshop verfeinern.
3. **Test mit 5–10 anonymisierten Echt-Anfragen** →
   [test-protokoll.md](test-protokoll.md).
4. **Rückfragen-Bausteine je Anfragetyp ableiten** → in `triage-logik.md`
   dokumentieren.
5. **Learnings als Anforderungsliste für das Ticketing-Intake dokumentieren** →
   Abschnitt „Ticketing-Intake-Anforderungen" in diesem README fortschreiben.

## Zusammenspiel mit Outlook Copilot

- Lange Mail-Threads vor der Triage mit Outlook Copilot zusammenfassen und die
  Zusammenfassung + Originaltext in den GPT geben.
- Den vom GPT gelieferten Rückfragen-E-Mail-Entwurf in Outlook einfügen und mit
  Copilot an den Hausstil anpassen.

## Ticketing-Intake-Anforderungen (Learnings sammeln)

> Während der Tests hier fortschreiben – das ist das zweite Arbeitsergebnis dieses
> Use Cases.

- Pflichtfelder im Intake-Formular: …
- Kategorien/Prioritäten (validiert): …
- Automatische Rückfragen-Textbausteine: …
- Routing-Regeln (Zuständigkeit): …
