# Use Case 4: Filing Assistant – zentrale Ablage-Mailbox mit KI-Klassifikation

## Ziel

Teammitglieder leiten Dokumente an ein zentrales Postfach weiter (zentrales Legal-Postfach, z. B. legal@[unternehmen].de). Eine KI klassifiziert jedes Dokument (Dokumenttyp,
Matter/Mandat, Parteien, Datum, Laufzeit, Kündigungsfrist), vergibt einen
einheitlichen Dateinamen und ordnet es einer definierten SharePoint-Struktur zu.
So entsteht schrittweise eine einheitliche Ablage und perspektivisch eine
Knowledge Database.

## Status quo (Pain Point)

1. Verträge und Korrespondenz liegen verteilt in E-Mail-Postfächern, SharePoint,
   Teams und lokalen oder Netzlaufwerken.
2. Keine einheitliche Ablagestruktur, Suchen kostet Zeit.
3. Wissen ist personengebunden und schwer zugänglich.

## Mehrwert

1. Einheitliche, durchsuchbare Ablage statt verstreuter Einzelablagen
2. Grundlage für Knowledge Management, Copilot-Suche und spätere CLM-Einführung
3. Fristen- und Laufzeitdaten als Nebenprodukt der Metadaten-Extraktion

## Umsetzung als Pilot (ohne Automatisierung)

Da kein Copilot Studio verfügbar ist, läuft der Pilot **halbmanuell**:

1. **Taxonomie und Namenskonvention definieren** →
   [ablage-taxonomie.md](ablage-taxonomie.md) im Team abstimmen.
2. **Klassifikations-GPT bauen** → Custom GPT in ChatGPT Enterprise mit
   [system-prompt.md](system-prompt.md); Taxonomie als Wissensdatei hochladen.
3. **Pilotbetrieb:** Dokumente aus dem Sammelpostfach einzeln (als **Kopie**!) in
   den GPT geben → GPT liefert Metadaten + Dateinamen + Ziel-Pfad → manuell in
   SharePoint ablegen.
4. **Trefferquote auswerten** → [test-protokoll.md](test-protokoll.md).
5. **Automatisierungs-Anforderungen dokumentieren** (Shared Mailbox + Power
   Automate als Ausbaustufe) → Abschnitt unten fortschreiben.

## ⚠️ Good-2-Know (aus dem Use-Case-Steckbrief)

**IT & Data Privacy einbinden:** Berechtigungskonzept, DSGVO,
Aufbewahrungsfristen. **Im Piloten mit Kopien arbeiten – keine Originale
verschieben.**

## Rolle von Outlook Copilot

- Posteingang der Shared Mailbox sichten/zusammenfassen.
- Im Pilot: Anhänge identifizieren und für die Klassifikation vorbereiten.

## Ausbaustufe: Automatisierung (Anforderungen sammeln)

- Trigger: neue Mail in das zentrale Legal-Postfach → Anhang extrahieren
- Klassifikation per API (strukturierte Ausgabe, JSON-Schema wie im Prompt)
- Ablage in SharePoint gemäß Taxonomie + Metadaten als SharePoint-Spalten
- Fristen (Kündigungsfrist, Laufzeitende) → automatische Erinnerung
- Fehlerfall: „Unklar"-Ordner + Benachrichtigung ans Team
