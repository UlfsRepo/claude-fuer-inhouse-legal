---
name: ma-playbook
description: Erstellt das M&A-Playbook einer Rechtsabteilung — Due-Diligence-Checklisten je Workstream (Corporate, Commercial, Compliance, IT/Datenschutz, IP, KI), Onboarding-/PMI-Checkliste und Kanzlei-Briefing-Template, parametrisiert nach Transaktionstyp. IMMER verwenden, wenn der Nutzer M&A-Prozesse, DD-Checklisten, PMI-Prozesse oder Kanzlei-Briefings standardisieren will.
---

# M&A-Playbook-Baukasten

Verwandelt vorhandene M&A-Erfahrung einer Rechtsabteilung in wiederverwendbare Standards: Checklisten, die bei der nächsten Transaktion sofort einsatzbereit sind, statt jedes Mal bei null zu beginnen. Reine Dokumentations- und Standardisierungsleistung — mit bestehenden Ressourcen umsetzbar.

## Parametrisierung (immer zuerst klären)

Frage vor jeder Checklisten-Erstellung ab:
- **Deal-Typ:** Share Deal / Asset Deal / Joint Venture / Minderheitsbeteiligung
- **Zielgröße:** Kleinsttransaktion, Mittelstand, Konzern-Dimension (bestimmt Prüftiefe)
- **Jurisdiktionen:** nur Inland / EU / Drittstaaten (bestimmt Zusatz-Workstreams wie Investitionskontrolle, Sanktionen)
- **Branche & Besonderheiten:** reguliert? IP-lastig? Software/KI-Anteil? Produktionsstandorte?

Die Checklisten werden auf diese Parameter zugeschnitten — bei Kleinsttransaktionen radikal gekürzt, nicht nur kopiert.

## Baustein 1: DD-Checklisten je Workstream

Je Workstream eine eigene Checkliste mit drei Spalten: **Prüfpunkt | Angeforderte Unterlagen | Red Flags**. Kern-Workstreams:

- **Corporate:** Gesellschafterstruktur, Satzungen/Gesellschaftsverträge, Gremienbeschlüsse, Change-of-Control-Klauseln, Organhaftung
- **Commercial:** Top-Kundenverträge, Lieferverträge, Rahmenverträge, Exklusivitäten, Laufzeiten/Kündigungsrechte, AGB
- **Compliance:** Sanktions-/Exportkontrolle, Korruptionsprävention, laufende Verfahren, Kartellthemen, Hinweisgebersystem
- **IT/Datenschutz:** Verarbeitungsverzeichnis, AVVs, Drittlandtransfers, IT-Sicherheitsvorfälle, Lizenz-Compliance
- **IP:** Schutzrechtsportfolio, Arbeitnehmererfindungen, Lizenzen (ein- und ausgehend), Open-Source-Nutzung, Domains/Marken
- **KI:** eingesetzte KI-Systeme und deren Einstufung, Trainingsdaten-Herkunft, KI-Klauseln in Kundenverträgen, interne KI-Richtlinien

Bei internationalem Bezug ergänze: Investitionskontrolle, Arbeitsrecht der betroffenen Länder, Steuern (Verweis an Fachbereich).

## Baustein 2: Onboarding-/PMI-Checkliste

Phasen nach Signing/Closing mit Verantwortlichkeits-Spalte (Legal / Fachbereich / extern):
1. **Day 1:** Vertretungsbefugnisse, Bankvollmachten, Handelsregister, Informationspflichten
2. **100 Tage:** Vertragsmigration (Templates des Erwerbers einführen), Vollmachtenkonzept, Compliance-Integration (Richtlinien ausrollen), Datenschutz-Harmonisierung
3. **Jahr 1:** Gesellschaftsrechtliche Vereinfachung, Verschmelzungen/Umfirmierungen, Beendigung von Übergangsvereinbarungen

## Baustein 3: Kanzlei-Briefing-Template

Eine Vorlage, die jede Mandatierung externer Kanzleien vereinheitlicht:
- Transaktionssteckbrief (Parteien-Rollen, Deal-Typ, Zeitplan — ohne vertrauliche Details im Erstkontakt)
- Scope: Welche Workstreams extern, welche inhouse (Abgrenzungsliste)
- Liefergegenstände und Formate (Red-Flag-Report vs. Full Report, Sprache, Vorlagen des Auftraggebers)
- Budgetrahmen, Abrechnungsmodell, Reporting-Rhythmus
- Ansprechpartner und Eskalationsweg

## Ausbaustufe: Adaptive Checklisten
Hinterlege die Checklisten so, dass sie per Prompt auf eine konkrete Transaktion zugeschnitten werden können („Share Deal, Software-Unternehmen, DACH, 40 Mitarbeiter" → gekürzte, angepasste Fassung). Die Parametrisierungs-Fragen oben sind dafür das Eingabeformular.

## Übergabe
Liefere jede Checkliste als eigenes Artefakt, ablagefertig nach der Namenskonvention der Wissensbibliothek (siehe Skill `wissensbibliothek`). Echte Transaktionsdaten bleiben lokal. Vor Weitergabe: Skill `vertraulichkeits-gate`.
