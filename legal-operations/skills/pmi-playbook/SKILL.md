---
name: pmi-playbook
description: Erstellt ein eigenständiges Post-Merger-Integration-Playbook aus Legal-Perspektive — Integrations-Governance, Phasenplan (Day 1, 100 Tage, Jahr 1), rechtlicher Integrations-Workstream im Detail (Gesellschaftsrecht, Arbeitsrecht mit Share-/Asset-Deal-Trennung, Litigation-Übergang, Vollmachten-Rollout, Registerpflichten), DD-Findings-Überführung, TSA-Tracking, Modul „Kulturelle Passung und Zusammenarbeit" und Abschlusskriterien. IMMER verwenden, wenn der Nutzer eine Post-Merger-Integration planen, ein PMI-Playbook aufbauen oder eine laufende Integration strukturieren will. Baut auf der PMI-Checkliste des Skills ma-playbook auf und vertieft sie zum vollständigen Playbook.
---

# PMI-Playbook

Verwandelt die Zeit nach dem Closing von einer Improvisationsphase in einen geführten Prozess. Die PMI-Checkliste (Skill `ma-playbook`, Teil B) sagt, *was* zu tun ist — dieses Playbook ergänzt, *wer steuert, wie berichtet wird, wann Schluss ist* und wie die menschliche Seite der Integration gelingt. Erfahrungswert dahinter: Integrationen scheitern selten an Checklisten, sondern an unklarer Steuerung und kultureller Reibung.

## Parametrisierung (zuerst klären)

- **Integrationstiefe:** Vollintegration / teilautonome Tochter / reine Finanzbeteiligung — bestimmt, welche Bausteine überhaupt greifen
- **Deal-Kontext:** Share/Asset, Größe des Ziels, Jurisdiktionen, gibt es TSAs?
- **Rolle von Legal:** Führt Legal die Integration oder einen Workstream? (Das Playbook funktioniert für beide Fälle, die Governance unterscheidet sich.)

## Baustein 1: Integrations-Governance

Eine halbe Seite, vor Day 1 festgezurrt:

| Rolle | Besetzung | Aufgabe |
|---|---|---|
| Integration Lead | eine Person, benannt vor Closing | steuert Gesamtplan, eskaliert, berichtet |
| Workstream-Owner | je Workstream einer (Legal, HR, Finance, IT, Operations …) | eigene Maßnahmenliste, meldet Status |
| Sponsor | Mitglied der Geschäftsleitung | entscheidet Eskalationen binnen definierter Frist |

- **Berichtsrhythmus:** wöchentlich einseitig (Ampel je Workstream, Top-Risiken, Entscheidungsbedarf) — erste 100 Tage; danach 14-tägig
- **Entscheidungswege:** Was entscheidet der Workstream, was der Lead, was der Sponsor — mit Wertgrenzen (`[BETRAG]`-Platzhalter; falls eine Delegation-of-Authority-Regelung existiert: dort andocken, siehe Skill `delegation-of-authority`, nichts doppelt regeln)
- **Eskalationsregel:** Blockiert > 1 Woche = automatisch auf Lead-Ebene; blockiert > 2 Wochen = Sponsor

## Baustein 2: Phasenplan

Übernimm die drei Phasen aus `ma-playbook` Teil B (Day 1 / 100 Tage / Jahr 1) und erweitere jede Maßnahme um vier Spalten: **Verantwortlich (Person) · Frist · Status · Abhängigkeit**. Damit wird aus der Checkliste ein Terminplan. Ergänze je Phase ein **Phasen-Gate**: ein kurzer Review am Phasenende (Was ist offen? Bewusste Entscheidung: nachziehen oder streichen), damit Altlasten nicht unbemerkt ins nächste Quartal rutschen.

## Baustein 3: Legal-Workstream im Detail

Der rechtliche Kern der Integration — hier scheitern Integrationen juristisch, nicht an fehlenden Checklisten-Zeilen, sondern an drei Präzisionsfehlern: Share- und Asset-Deal-Maßnahmen werden vermischt, Fristen laufen im Übergang herrenlos, und Formalia werden als Verwaltungskram unterschätzt. Deshalb gilt in diesem Baustein durchgängig:

> **Rechtsgrundlagen-Hinweis:** Alle Paragraphen-Angaben beziehen sich auf deutsches Recht (Stand des Playbooks; vor Verwendung aktuell prüfen). Für Gesellschaften anderer Jurisdiktionen dienen die Zeilen als Fragenkatalog an Local Counsel — nie als Antwort.

### 3a. Gesellschaftsrecht & Governance

| Maßnahme | Präzisierung | Zeit-Anker |
|---|---|---|
| Organbestellung/-abberufung | Neue Geschäftsführer bestellen, Vertretungsregelung festlegen; Anmeldung zum Handelsregister (§ 39 GmbHG) | Day 1 / unverzüglich |
| Gesellschafterliste | Nach Share Deal: neue Liste zum Handelsregister (§ 40 GmbHG; bei notarieller Abtretung reicht der Notar ein — Eingang kontrollieren, nicht vermuten) | unverzüglich nach Closing |
| Transparenzregister | Änderung der wirtschaftlich Berechtigten mitteilen (§ 20 GwG) — beim Share Deal fast immer ausgelöst, wird notorisch vergessen | unverzüglich |
| Geschäftsordnung & Zustimmungskatalog | Für die Geschäftsführung der neuen Tochter erlassen; Wertgrenzen und Vorbehaltsgeschäfte aus der DoA ableiten (Skill `delegation-of-authority`) — ein Regelwerk, zwei Dokumente, keine Widersprüche | 100 Tage |
| Konzernintegration | Ggf. Beherrschungs-/Gewinnabführungsvertrag (§§ 291 ff. AktG; steuerliche Organschaft mit Steuerfunktion abstimmen); Cash-Pooling-Beitritt nur nach Kapitalerhaltungs-Prüfung (§ 30 GmbHG, Vollwertigkeit des Rückgewähranspruchs) | 100 Tage – Jahr 1 |
| Firmierung & Pflichtangaben | Umfirmierung, dann sofort: Geschäftsbriefe, Rechnungen, Impressum, E-Mail-Signaturen (§ 35a GmbHG, § 37a HGB) | mit Umfirmierung |

### 3b. Arbeitsrecht — strikt nach Deal-Typ trennen

**Share Deal:** Kein Betriebsübergang — Arbeitgeber bleibt dieselbe juristische Person, Arbeitsverhältnisse laufen unverändert. § 613a BGB ist hier **nicht** einschlägig (häufigster Beratungsfehler in PMI-Plänen). Aber: Unterrichtung des Wirtschaftsausschusses über die Übernahme bei Kontrollerwerb (§ 106 Abs. 3 Nr. 9a BetrVG).

**Asset Deal (Betriebsübergang):** § 613a BGB vollständig abarbeiten:
- **Unterrichtung** aller betroffenen Arbeitnehmer in Textform **vor** Übergang (§ 613a Abs. 5 BGB) — inhaltlich vollständig und richtig: Eine fehlerhafte Unterrichtung setzt die Widerspruchsfrist nicht in Gang, das Widerspruchsrisiko läuft dann unbegrenzt weiter
- **Widerspruchsrecht** ein Monat ab ordnungsgemäßer Unterrichtung (§ 613a Abs. 6 BGB) — Rücklaufliste führen
- **Kündigungsverbot** wegen des Übergangs (§ 613a Abs. 4 BGB)
- **Kollektivrecht:** Tarifverträge/Betriebsvereinbarungen wirken transformiert weiter, Verschlechterungssperre ein Jahr (§ 613a Abs. 1 S. 2 BGB)

**Beide Deal-Typen:**
- Geplante Restrukturierung = Betriebsänderung: Interessenausgleich/Sozialplan **vor** Umsetzung (§§ 111, 112 BetrVG)
- Harmonisierung der Arbeitsbedingungen: neue Muster gelten für Neueintritte sofort; Bestandsverträge nur per Änderungsvereinbarung — betriebliche Altersversorgung immer gesondert prüfen (eigene Anwartschaftslogik)
- Bindung von Schlüsselpersonen: Verzahnung mit dem Schlüsselpersonen-Radar (Baustein 6c)

### 3c. Laufende Rechtsstreitigkeiten & Verfahren

| Schritt | Präzisierung |
|---|---|
| Litigation-Register anlegen | Aus der DD-Bestandsliste: Verfahren, Gericht/Instanz, Streitwert-Kategorie, Verfahrensbevollmächtigte, **nächste Frist** — kein Verfahren ohne benannte verantwortliche Person, auch nicht für eine Woche |
| Share Deal | Partei bleibt die Zielgesellschaft, Verfahren laufen unverändert — aber: Instruktionsrechte und Prozessvollmachten neu ordnen, Kanzleimandate bestätigen oder neu vergeben (vorher Interessenkonflikt-Check: Vertritt die Kanzlei Gegner des Erwerber-Konzerns?) |
| Asset Deal | Keine automatische Prozessübernahme: Aktiv- und Passivprozesse einzeln dem Kaufvertrag zuordnen; bei Veräußerung der streitbefangenen Sache führt der Veräußerer den Prozess fort (§ 265 ZPO) — Parteiwechsel nur mit Zustimmung der Gegenseite |
| SPA-eigene Fristen | Garantie-/Freistellungsansprüche aus dem Kaufvertrag selbst: Notice Periods und Verjährungsfristen in den Fristenkalender, Beweissicherung ab Tag 1 (nicht erst, wenn ein Anspruch sichtbar wird) |
| Versicherungen | D&O: Run-off/Nachmeldefrist für Alt-Organe klären, bevor die Altpolice endet; Betriebshaftpflicht lückenlos; offene Schadenfälle dem neuen Versicherer melden |

### 3d. Vollmachten & DoA-Rollout

1. **Inventar:** Alle bestehenden Vollmachten erfassen (Prokuren, Handlungsvollmachten § 54 HGB, Einzelvollmachten, Bankvollmachten) — die Dunkelziffer ist regelmäßig hoch
2. **Widerruf:** Nicht mehr gewollte Vollmachten aktiv widerrufen; Erlöschen von Prokuren zum Handelsregister anmelden (§ 53 HGB) — eine nicht gelöschte Prokura wirkt im Rechtsverkehr fort
3. **Neukonzept:** Vollmachten nach der DoA-Matrix neu erteilen (Rollen statt Personen, Wertgrenzen, Vier-Augen-Prinzip) — Skill `delegation-of-authority`
4. **Banken:** Zeichnungsberechtigungen stichtagsgenau umstellen (Day 1), alte Berechtigungen schriftlich bestätigt löschen lassen

### 3e. Formalia je Jurisdiktion (internationale Ziele)

- Je Land **einen** Local Counsel benennen mit festem Fragenkatalog: Meldepflichten bei Gesellschafterwechsel, UBO-/Transparenzregister, Formerfordernisse der Organbestellung (Notariat, Apostille, Legalisation), lokale arbeitsrechtliche Beteiligungsrechte
- **Post-Closing-Auflagen** aus Fusionskontroll- oder Investitionskontroll-Freigaben in ein eigenes Auflagen-Register (Behörde, Auflage, Nachweis, Frist) — Verstöße hier sind bußgeldbewehrt und fallen Jahre später auf
- Faustregel: Was in Deutschland Registersache ist, ist anderswo oft Notariats- oder Behördensache mit Wochen Vorlauf — Fristen rückwärts von Day 1 planen

## Baustein 4: DD-Findings-Register

Jeder Red Flag aus der Due Diligence wird binnen zwei Wochen nach Closing in genau eine Zeile überführt:

| Finding (aus DD) | Risiko, wenn unbehandelt | Maßnahme | Owner | Frist | Status |
|---|---|---|---|---|---|

Regel: Kein Finding verschwindet — es wird erledigt, akzeptiert (dokumentiert, von wem) oder eskaliert. Das Register ist der wichtigste Nachweis, dass die DD nicht für die Schublade war.

## Baustein 5: TSA-Tracking

Übergangsvereinbarungen (Transition Service Agreements) sind planmäßig endende Provisorien — ohne Tracking werden sie teure Dauerzustände:

| TSA / Leistung | Erbringer | Endtermin | Ablösung durch | Ablöse-Status | Kosten p. M. |
|---|---|---|---|---|---|

Regel: Jede TSA hat ab Tag 1 einen Ablösungsplan. 90 Tage vor Endtermin: Entscheidung verlängern (bewusst, mit Grund) oder beenden — nie stillschweigend auslaufen lassen oder verlängern.

## Baustein 6: Modul „Kulturelle Passung und Zusammenarbeit"

Der am häufigsten übersprungene Teil — und die häufigste Scheiterursache. Drei konkrete Instrumente statt Kultur-Prosa:

**6a. Kultur-Schnellcheck (Workshop, 90 Minuten, beide Seiten):** Je Dimension einordnen — wo stehen wir, wo steht das Ziel, wie groß ist die Lücke?
- Entscheidungsstil: konsensorientiert ↔ hierarchisch schnell
- Formalisierungsgrad: dokumentiert/prozessgetrieben ↔ zuruforientiert
- Fehlerkultur: Eskalation erwünscht ↔ Probleme bleiben lokal
- Kommunikation: direkt ↔ indirekt; Meeting-Kultur; Sprache(n)
- Tempo-Erwartung: Quartalslogik ↔ Langfristlogik

Ergebnis: die 2–3 größten Lücken mit je einer konkreten Arbeitsregel (siehe 6b). Nicht mehr — Kulturarbeit scheitert an Vollständigkeitsanspruch.

**6b. Zusammenarbeitsregeln (1-Pager):** Für die Übergangszeit explizit machen, was sonst jeder anders annimmt: Wer lädt wen zu welchen Runden ein · in welcher Sprache wird dokumentiert · Antwortzeiterwartungen · wie werden Meinungsverschiedenheiten zwischen alt/neu entschieden · welche Alt-Gewohnheiten bleiben bewusst erhalten (Wertschätzung!).

**6c. Schlüsselpersonen-Radar:** Liste der 5–10 Personen des Ziels, deren Weggang die Integration gefährdet — je Person: Bindungsrisiko (hoch/mittel/niedrig), Maßnahme (Gespräch, Rolle, Retention), Owner. Vierteljährlich aktualisieren. (Personenbezogen → strikt vertraulich, nie in geteilte Ablagen ohne Zugriffsschutz.)

## Baustein 7: Abschlusskriterien

Eine Integration ist fertig, wenn Kriterien erfüllt sind — nicht wenn niemand mehr fragt. Vorab definieren, z. B.: alle DD-Findings geschlossen/akzeptiert · alle TSAs beendet · Vertragsmigration ≥ [X] % · Governance des Ziels im Regelbetrieb (DoA, Vollmachten, Gremien) · Kultur-Arbeitsregeln in Regel-Zusammenarbeit überführt. Dann: Abschlussbericht (1 Seite), Lessons Learned zurück ins M&A- und dieses PMI-Playbook (neue `vNN`) — und formales Ende des Integrationsmodus.

## Übergabe

Liefere: Governance-Halbseite, erweiterten Phasenplan, den Legal-Workstream (Baustein 3, an Deal-Typ und Jurisdiktionen angepasst), die Register-Vorlagen (Findings, TSA, Litigation, Auflagen, Schlüsselpersonen), Kultur-Workshop-Leitfaden mit Zusammenarbeitsregeln-1-Pager, Abschlusskriterien-Liste — ablagefertig nach `governance-format`. Echte Transaktions- und Personendaten bleiben lokal. Vor Weitergabe: Skill `vertraulichkeits-gate`.
