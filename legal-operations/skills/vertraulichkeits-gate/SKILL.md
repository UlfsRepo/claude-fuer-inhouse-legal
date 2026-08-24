---
name: vertraulichkeits-gate
description: Verpflichtendes Quality-Gate vor jeder Weitergabe eines Artefakts — prüft auf vertrauliche Inhalte (Namen, Zahlen, interne Bezeichnungen, Mandatsbezüge) und trennt sauber zwischen generischer Methodik und unternehmensspezifischen Daten. IMMER verwenden, bevor ein erstelltes Dokument geteilt, versendet, veröffentlicht oder in ein öffentliches Repository committet wird.
---

# Vertraulichkeits-Gate

Letzte Prüfung, bevor ein Artefakt die eigene Maschine verlässt. Grundsatz: **Methodik darf reisen, Daten bleiben zu Hause.** Das Gate stellt sicher, dass diese Grenze bei jedem einzelnen Dokument gezogen wurde.

## Prüfkatalog

Prüfe das Artefakt Zeile für Zeile auf:

1. **Personennamen** — Mitarbeitende, externe Berater, Ansprechpartner (auch in Beispielen und Metadaten)
2. **Unternehmens- und Organisationsbezüge** — Arbeitgeber, Konzerngesellschaften, Abteilungskürzel, interne Programm- oder Projektnamen, Systemnamen
3. **Zahlen mit Rückschlusswert** — Schwellenwerte, Budgets, Streitwerte, Gehälter, Zielgrößen, KPIs
4. **Mandats- und Vorgangsbezüge** — echte Fälle, Gegner, Vertragspartner, Aktenzeichen, Matter-IDs mit realem Inhalt
5. **Wörtliche Übernahmen** aus internen Dokumenten — Zielformulierungen, Beschlusstexte, Vertragsklauseln aus echten Verträgen
6. **Metadaten** — Dateipfade, Autorenfelder, Kommentare, Änderungshistorien in Office-Dokumenten

## Entscheidungsregel je Fund

- **Generalisieren:** Der Inhalt ist methodisch wertvoll → ersetze durch Platzhalter (`[THRESHOLD]`, `[COMPANY]`, „ein international tätiges Industrieunternehmen") oder durch fiktive Beispiele.
- **Entfernen:** Der Inhalt trägt methodisch nichts → streichen.
- **Zurückhalten:** Das Artefakt ist ohne die vertraulichen Teile wertlos → es ist ein internes Dokument und wird nicht geteilt. Kennzeichne es entsprechend.

## Ausgabeformat

```
# Vertraulichkeits-Gate — <Artefakt> — <Datum>
**Ergebnis:** ✅ freigabefähig / ⚠️ freigabefähig nach Änderungen / ⛔ intern halten
| # | Fundstelle | Kategorie | Empfehlung |
|---|---|---|---|
```

Bei ⚠️: Nimm die Änderungen vor und lass den Nutzer das Ergebnis bestätigen. Bei ⛔: Benenne, was das Dokument intern macht — und ob eine generische Fassung lohnt.

## Grenzen

Das Gate prüft Texte, keine Absichten: Ob ein Inhalt einem Geheimhaltungsvertrag, einer internen Richtlinie oder gesetzlichen Pflichten unterliegt, entscheidet der Mensch. Im Zweifel gilt ⛔. Das Gate ersetzt keine Freigabeprozesse des Arbeitgebers.
