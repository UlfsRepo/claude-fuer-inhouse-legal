# KI-Strategie für eine Inhouse-Rechtsabteilung

Teil des öffentlichen Repos claude-fuer-inhouse-legal. Alle Pfade in dieser Datei sind relativ zu ki-strategie/.

## Ziel
Entwicklung einer umfassenden, forschungsbasierten KI-Strategie für die Rechtsabteilung eines international tätigen Industrieunternehmens im DACH-Raum nach dem Leitprinzip „AI first“. Ergebnis: ein Strategiepapier, daraus abgeleitete Umsetzungsbausteine für ein unternehmensweit eingesetztes Enterprise-LLM (ChatGPT Enterprise) und eine PowerPoint-Präsentation für die Geschäftsleitung.

## Vertraulichkeit (verbindlich)
Dieses Repository ist öffentlich und enthält keine vertraulichen Unternehmensdaten.
- Keine Firmennamen, Personennamen, Budgets, Vertragsinhalte, Produktnamen, Standorte, Abteilungskürzel, internen Systemnamen oder internen Kennzahlen.
- Unternehmensspezifische Details nur als Platzhalter, z. B. [UNTERNEHMEN], [TEAMGRÖSSE], [BUDGET], [ITSM-TOOL], [STICHTAG].
- Auch Kombinationen vermeiden, die für sich harmlos sind, zusammen aber ein Unternehmen erkennbar machen (z. B. Branche + Region + exakte Teamgröße + konkreter Tool-Stack).
- Wenn ich versehentlich vertrauliche Informationen eingebe, weise mich darauf hin, bevor du sie in eine Datei schreibst. Schlage eine anonymisierte Formulierung vor.
- Vertrauliche Entwürfe gehören ausschließlich nach lokal/ oder in Dateien mit dem Suffix _privat. Office-Dateien und PDFs werden nicht versioniert. Finale, unternehmensbezogene Fassungen (z. B. das Deck für die Geschäftsleitung) entstehen lokal.
- Vor jedem Commit: den Skill ../legal-operations/skills/vertraulichkeits-gate/ auf alle geänderten Dateien anwenden und zusätzlich per grep nach den Begriffen aus lokal/vertraulichkeits-begriffe.txt suchen (case-insensitive). Ergebnis kurz melden. Commit und Push nur nach meiner ausdrücklichen Freigabe.

## Ausgangslage (anonymisiert)
- Kleines Kernteam ([TEAMGRÖSSE] Jurist:innen inkl. Leitung), hohe Auslastung, niemand freistellbar
- Enterprise-LLM unternehmensweit ausgerollt und in der Rechtsabteilung in Nutzung
- Microsoft-365-Umgebung (SharePoint, Teams, Power Automate); Copilot Studio perspektivisch
- Wissen heute verstreut (lokal, SharePoint, Teams, Postfächer); keine Single Source of Truth
- Vorhandene ITSM-Plattform ([ITSM-TOOL]) im Unternehmen, die als Intake-Lösung genutzt werden soll

## Bereits getroffene Entscheidungen
1. Intake zuerst: über die vorhandene ITSM-Plattform, schmale Taxonomie (5–7 Anfragekategorien). Ein eigenes Intake-Konzept existiert und wird nur anonymisiert in 03_bausteine/intake/ übernommen.
2. Wissensbasis in SharePoint, zweistufig:
   - Stufe 1: Vorwärtsaufbau ab [STICHTAG], nur kuratierte Unterlagen, kein Altbestand
   - Stufe 2: spätere gezielte Migration der besten Unterlagen, ausgelöst durch ein konkretes Ereignis (zusätzliche Kapazität oder CLM-Projekt)
3. Flache Struktur mit drei Bibliotheken: Verträge, Templates/Muster, Stellungnahmen/Gutachten. Korrespondenz nur aktengebunden.
4. Schlankes Datenmodell: 6–8 Metadatenfelder pro Bibliothek, Auswahllisten statt Freitext, CLM-migrationsfähig.
5. Pro Kategorie genau ein als verbindlich markiertes Dokument.

## Geparkt (später bearbeiten)
- Workflow-Ebene (Power Automate, später Copilot Studio)
- CLM-Tool-Auswahl (z. B. Ironclad oder vergleichbar)

## Arbeitsphasen
1. Recherche: aktuelle Studien und Frameworks zu KI in Rechtsabteilungen
2. Strategie: Zielbild, Handlungsfelder, Roadmap, Governance, Change-Management
3. Bausteine: Intake, Wissensbasis, Workflows
4. Umsetzung im Enterprise-LLM: Prompts, Custom-GPT-Instruktionen, Wissensdateien
5. Präsentation: Storyline, dann PowerPoint

## Bezüge im Repo (nutzen statt duplizieren)
- ../research/legal-department-2030-research.md: bestehendes Research-Memo (Stand 09/2026) mit Hypothesen und belegten Zahlen; Ausgangspunkt der Recherche, Lücken gezielt ergänzen
- ../legal-operations/skills/matter-intake/: methodische Grundlage für den Intake-Baustein
- ../legal-operations/skills/wissensbibliothek/: methodische Grundlage für die Wissensbasis
- ../legal-operations/skills/vertraulichkeits-gate/: verpflichtend vor jedem Commit
- ../ki-use-cases/ und ../prozesslandkarte/: vorhandene Custom-GPT-Vorlagen und Prozessdoku-Framework; bei Phase 4 darauf aufbauen

## Recherche-Regeln
- Vorrangige Quellen: Thomson Reuters (Future of Professionals, Generative AI in Professional Services, Archetypen-Framework), ACC (Chief Legal Officers Survey, Legal Ops Maturity Model), Wolters Kluwer (Future Ready Lawyer), CLOC (State of the Industry), Gartner Legal & Compliance, Studien führender Beratungshäuser.
- Nur aktuelle Quellen (bevorzugt 2025–2026); Erscheinungsjahr immer angeben.
- Jede Aussage mit Quelle und Link; keine erfundenen Zahlen, Zitate oder Studien. Nicht verifizierbare Quellen als „nicht verifiziert“ kennzeichnen. Wenn nur eine Zusammenfassung hinter einer Paywall zugänglich ist, als „Paywall – nur Sekundärquelle“ kennzeichnen.
- Pro Studie eine Exzerpt-Datei in 01_recherche/ nach der Vorlage _vorlage_exzerpt.md, mit Kernaussagen, relevanten Zahlen, Relevanz für kleine Inhouse-Teams und Grenzen der Studie; jede Quelle zusätzlich in quellenverzeichnis.md eintragen.
- Keine längeren wörtlichen Übernahmen aus Studien (Urheberrecht; das Repo ist öffentlich): eigene Zusammenfassungen, Zitate nur kurz und belegt.
- Besonders relevant: Erkenntnisse zu Adoptionswiderständen und Change-Management, nicht nur zu Tools.

## Arbeitsweise
- Sprache: Deutsch. Fachbegriffe auf Englisch nur, wo üblich.
- Strukturiert und entscheidungsorientiert; ehrliche Einschätzung vor Bestätigung.
- Vor umfangreichen Ausarbeitungen kurz Rückfragen stellen.
- Entscheidungen in 02_strategie/entscheidungslog.md mit Datum und Begründung festhalten.
- Artefakte für das Enterprise-LLM so formulieren, dass sie ohne Änderung per Copy-paste übernommen werden können; Zeichenlimits für GPT-Instruktionen beachten und die Zeichenzahl jeweils angeben.

## Ordnerstruktur
- 01_recherche/ – Studien-Exzerpte, Quellenverzeichnis, Exzerpt-Vorlage
- 02_strategie/ – Strategiepapier, Entscheidungslog
- 03_bausteine/ – Unterordner intake/, wissensbasis/, workflows/ (geparkt)
- 04_chatgpt/ – Unterordner prompts/, gpt-instruktionen/, konfigurationen/ (JSON)
- 05_deck/ – Storyline und Foliengliederung (Markdown); die .pptx entsteht lokal
- lokal/ – vertrauliche Entwürfe und Grep-Begriffe, nicht versioniert
