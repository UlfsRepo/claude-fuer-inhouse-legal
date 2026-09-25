# KI-Strategie der Rechtsabteilung – Entwurf v0.2

Stand: 25.09.2026 · Status: **Entwurf mit Vorentscheidungen**, Bestätigung durch das Team im Workshop ausstehend (Entscheidungslog Nr. 6–10) · Evidenzbasis: [Synthese Recherche Runde 1](../01_recherche/synthese-recherche-runde-1.md) · Unternehmensspezifika als Platzhalter

---

## 1. Ausgangslage und Handlungsdruck

**Intern (anonymisiert):**
- Kleines Kernteam ([TEAMGRÖSSE] Jurist:innen inkl. Leitung), hohe Auslastung, niemand freistellbar.
- Enterprise-LLM unternehmensweit ausgerollt und in Nutzung.
- Microsoft-365-Umgebung (SharePoint, Teams, Power Automate), eine ITSM-Plattform ist vorhanden.
- Wissen liegt verstreut, es gibt keine Single Source of Truth.

**Extern (belegt):**
- **Wachstum ist nicht über zusätzliche Köpfe zu lösen.** Das Bundesrecht ist 2010–2024 um 22,6 % mehr Einzelnormen und 31,1 % mehr Textvolumen gewachsen. Rund 47 % der Anwaltschaft erreichen in 15 Jahren das Ruhestandsalter (Bucerius 2026, Prognose). Personalmangel ist international das größte Hindernis für Rechtsabteilungen (48 %, TR 2026).
- **Kleine Rechtsabteilungen nutzen KI, steuern sie aber nicht.** Bis 10 Mitarbeitende nutzen 79,7 % KI, doch 57,8 % haben keine KI-Strategie und 41,4 % keine Nutzungsvorgaben. 90,4 % aller Rechtsabteilungen messen den KI-Erfolg nicht (Bucerius 2026).
- **Der Wertbeitrag ist unsichtbar.** 86 % der GCs sehen ihre Abteilung als wichtigen Wertbeitrag, aber nur 17 % der C-Suite (TR 2026).
- **Eine Strategie wirkt.** Mit benannter KI-Strategie sagen 66 %, KI erfülle die Werterwartung, ohne Strategie 22 % (TR 2026, Selbstauskunft).

**Kernaussage:** Tools sind vorhanden. Es fehlen eine ausdrückliche Richtung, die Grundlagen (Intake, Wissensbasis), Befähigung und Messung. Genau dort setzt diese Strategie an.

## 2. Leitprinzip „AI first“ – was es hier bedeutet

„AI first“ heißt: **Bei jeder wiederkehrenden Aufgabe ist KI die erste Option, und wer auf sie verzichtet, begründet das.** Es heißt nicht, KI vor die Grundlagen zu stellen. Ohne strukturierten Eingang und ohne verbindliche Muster liefert ein LLM keine verlässlichen Ergebnisse (ACC-Stufenlogik, TR „Prozesse vereinfachen, dann automatisieren“).

Drei Grundsätze:
1. **Grundlagen als KI-Infrastruktur:** Intake und Wissensbasis werden von Anfang an so gebaut, dass das LLM sie nutzen kann.
2. **Mensch entscheidet:** KI liefert Entwürfe und Vorsortierung. Verantwortung und Freigabe bleiben bei den Jurist:innen.
3. **Freigegebener Weg statt Schatten-KI:** Genutzt wird das unternehmensweite Enterprise-LLM, nach klaren Regeln.

## 3. Zielbild ([ZIELJAHR], ca. 24 Monate)

Die Rechtsabteilung entwickelt sich **vom Schutzschild zum Navigator** (Leitbild nach Bucerius 2026). Sie konzentriert sich bewusst auf zwei der fünf TR-Archetypen:

| Stufe | Archetyp (TR 2026) | Was das konkret heißt |
|---|---|---|
| Stufe 1 (Monate 0–12) | **Scaled Enablement**: Volumen bewältigen | Alle Anfragen laufen über das Intake mit 5–7 Kategorien. Standardfälle werden mit verbindlichen Mustern und LLM-Unterstützung bearbeitet. Die Wissensbasis ist die einzige Quelle für aktuelle Muster und Stellungnahmen. |
| Stufe 2 (Monate 9–24) | **Empowering Peer**: Fachbereiche befähigen | Fachbereiche lösen definierte Routinefälle selbst, mit Custom GPTs, Playbooks und klaren Leitplanken. Anfragen, die nicht zu Legal müssen, kommen dort gar nicht erst an. |
| Wirkung | **Advisory Plus**: mehr Beratung | Die frei gewordene Kapazität fließt nachweislich in frühzeitige strategische Beratung. Das ist kein eigenes Programm, sondern das Ergebnis von Stufe 1 und 2. |

**Pfadlogik:** Kapazität schaffen ist das Mittel, mehr Beratung das Ziel (TR: „Scale“ → „Elevate“). Einen Neuentwurf der gesamten Arbeitsweise um KI herum („Reimagine“) streben wir bis [ZIELJAHR] bewusst nicht an. Nur 1 % der befragten Unternehmensfunktionen sind heute so weit (TR 2026).

**Bewusst zurückgestellt:** Die gemeinsame Steuerung externer Kanzleien mit geteilten Qualitätsstandards (Archetyp „Seamless Integrator“) und die CLM-Einführung. Internationale Arbeit mit Übersetzung und mehrsprachigen Entwürfen läuft als Anwendungsfall im LLM mit, ohne eigenes Programm.

## 4. Handlungsfelder

### H1 Intake (Entscheidung Nr. 1)
- **Was:** Anfragen laufen über die ITSM-Plattform mit schmaler Taxonomie. Pflichtangaben verhindern Rückfragen, Priorisierung und Zuweisung laufen nach festen Regeln.
- **KI-Bezug:** Aus dem Intake entstehen die Daten für Use-Case-Auswahl und KPIs. Später kommen LLM-Vorsortierung und Antwortvorschläge für Standardfälle hinzu.
- **Evidenz:** Intake und Triage sind der nächste Reifeschritt (ACC, mittlere Stufe). Der erste Use Case sollte beim höchsten Volumen mit dem geringsten Urteilsanteil liegen (TR).
- **Baustein:** [03_bausteine/intake](../03_bausteine/intake/) auf Basis des Skills `matter-intake`.

### H2 Wissensbasis (Entscheidungen Nr. 2–5)
- **Was:** SharePoint mit drei Bibliotheken und schlankem Datenmodell. Pro Kategorie gibt es genau ein verbindliches Dokument. Aufgebaut wird ab [STICHTAG], ohne Altbestand.
- **KI-Bezug:** Die kuratierten Muster sind die Wissensdateien für die Custom GPTs. Ohne diese Kuratierung liefert das LLM beliebige Ergebnisse.
- **Evidenz:** Dokumentenerstellung hat die größte Lücke zwischen Nutzen und tatsächlicher Nutzung (83,8 % halten KI dafür für hilfreich, 51,5 % nutzen sie; Bucerius). Wissensmanagement gehört zu den Quick Wins. Die mittlere ACC-Stufe verlangt ein zentrales Repository, Kuratierung und eine teilweise zuständige Person.
- **Baustein:** [03_bausteine/wissensbasis](../03_bausteine/wissensbasis/) auf Basis des Skills `wissensbibliothek`.

### H3 KI-Anwendungsfälle im Enterprise-LLM
- **Was:** Ein priorisiertes Portfolio von Use Cases mit kopierfertigen Prompts und Custom GPTs.
- **Priorisierung nach der Adoption-Impact-Matrix von Bucerius:**
  1. *Quick Wins*, sofort nutzbar: Recherche, Übersetzung, Zusammenfassung, Entwürfe aus Mustern.
  2. *Investitionspriorität:* Vertragsprüfung gegen Playbook, Triage-Unterstützung.
  3. *Stufe 2:* Self-Service-GPTs für Fachbereiche.
- **Evidenz:** Hohe Nutzung ist Standard. Wert entsteht durch gezielte Use Cases, nicht durch Zugang (Wolters Kluwer, TR).
- **Baustein:** [04_chatgpt](../04_chatgpt/), mit Wiederverwendung der Vorlagen aus [ki-use-cases](../../ki-use-cases/).

### H4 Governance
- **Was:**
  - Eine kurze KI-Nutzungsrichtlinie für die Rechtsabteilung: Datenklassen, was ins LLM darf, Prüfpflicht, Kennzeichnung, Verantwortung.
  - Anschluss an die KI-Governance des Unternehmens einschließlich EU AI Act.
  - Die Rechtsabteilung bringt sich dort aktiv ein.
- **Evidenz:**
  - 41,4 % der kleinen Rechtsabteilungen haben keine Nutzungsvorgaben (Bucerius).
  - 34–36 % nutzen nicht freigegebene Tools. Freigabe wirkt besser als Verbot (TR, Wolters Kluwer).
  - TR sieht den GC in der Führungsrolle bei der KI-Governance im Unternehmen.
- **Prüfen, nicht annehmen:** Reicht die bestehende Unternehmens-Governance für vertrauliche juristische Arbeit aus (TR)?

### H5 Befähigung und Change
- **Was:** Befähigung findet in der Arbeit statt, nicht daneben. Grundlage sind die sechs Hebel der TR AI Success Pyramid und das ADKAR-Modell:
  - **Rollenkonkret machen:** Pro Rolle ist festgehalten, wo KI unterstützt und wo das Urteil bleibt (Awareness).
  - **Leitung als Vorbild:** Die Leitung nutzt KI sichtbar selbst („leader-led learning“, Bucerius).
  - **Lernen am echten Fall:** 15 Minuten pro Woche im Teammeeting für den „Fall der Woche“ mit KI. Review KI-gestützter Arbeit im Vier-Augen-Prinzip (Knowledge).
  - **Mitgestaltung:** Das Team wählt die Use Cases mit aus und pflegt die Muster (Ownership).
  - **Erwartungen stufenweise:** Erst ca. 3 Monate ermutigen und Zugang schaffen, danach gilt „KI zuerst“ für Standardfälle verbindlich; Abweichungen werden kurz begründet (Expectations; Entscheidungslog Nr. 8).
  - **Persönliche Ziele:** Je Person ein KI-bezogenes Ziel in der Zielvereinbarung (Accountability).
- **Evidenz:**
  - Kompetenz ist der Engpass, nicht Akzeptanz: 91,7 % akzeptieren KI, 41,7 % fühlen sich nicht vorbereitet (Bucerius).
  - Schulung ist eine der Top-Hürden (39 %, Wolters Kluwer).
  - Die Lücke zwischen Strategie und Alltag ist ein Change-Problem (TR).
- **Veränderungslast steuern:** Pro Quartal gibt es höchstens eine größere Umstellung (ACC, höchste Stufe Change Management).

### H6 Wertnachweis und KPIs
- **Was:** Wenige Kennzahlen ab dem ersten Tag, berichtet in der Sprache der Geschäftsleitung. Gezeigt wird nicht nur, was eingespart wurde, sondern wofür die frei gewordene Kapazität eingesetzt wurde.
- **Evidenz:**
  - 90,4 % der Rechtsabteilungen messen KI-Erfolg nicht (Bucerius).
  - Nur 17 % der C-Suite sehen Legal als wichtigen Wertbeitrag.
  - Wer nur Effizienz meldet, riskiert Kürzungen (TR).

## 5. KPI-Set

Kennzahlen mit ● werden an die Geschäftsleitung berichtet (Entscheidungslog Nr. 9), die übrigen dienen der internen Steuerung.

| KPI | Quelle | Ausgangswert |
|---|---|---|
| ● Anfragevolumen je Kategorie und Monat | ITSM | ab Go-live Intake |
| ● Durchlaufzeit je Kategorie (Median) | ITSM | ab Go-live Intake |
| Anteil Standardfälle, die mit verbindlichem Muster und LLM bearbeitet werden | ITSM-Kennzeichnung | Schätzung Team |
| ● Abdeckung der Wissensbasis: Kategorien mit verbindlichem Dokument | SharePoint | 0 zum [STICHTAG] |
| ● Anteil Anfragen, die per Self-Service gelöst werden (ab Stufe 2) | GPT-Nutzung / ITSM | – |
| ● Stakeholder-Zufriedenheit (Kurzbefragung, halbjährlich) | Umfrage | Erstbefragung vor dem Start |
| ● Kapazitätsnachweis: frei gewordene Stunden und ihr Einsatz | Teamschätzung, quartalsweise | – |
| Reifegrad in sechs ACC-Bereichen | Workshop, jährlich | Standortbestimmung |

**Realistische Erwartung:** Etwa 10 % Zeitgewinn pro Kopf durch KI-Unterstützung (Wolters Kluwer, Selbsteinschätzung). Der größere Hebel ist Nachfrage, die dank Self-Service und Mustern gar nicht erst bei Legal ankommt. Den Business Case entsprechend konservativ rechnen.

## 6. Reifegrad: Ist und Ziel (ACC Legal Ops Maturity Model 2.0)

Die Ist-Stufen ermittelt das Team in einem zweistündigen Workshop. Die Zielstufen sind Vorschläge.

| Bereich | Ist | Ziel [ZIELJAHR] |
|---|---|---|
| Strategic Planning | [IST] | Intermediate: schriftliche Strategie, jährlich aktualisiert |
| Internal Resources / Intake | [IST] | Intermediate: Intake- und Triage-Funktion über ITSM |
| Knowledge Management | [IST] | Intermediate: zentrales Repository, Kuratierung, KM als Teilrolle |
| Technology Management | [IST] | Intermediate, dazu ein Advanced-Merkmal: fester Prozess für KI-Piloten |
| Change Management | [IST] | Intermediate: systematisch je Initiative, Veränderungslast gesteuert |
| Metrics & Analytics | [IST] | Intermediate: Basiskennzahlen aus ITSM, Reporting an die Geschäftsleitung |

## 7. Roadmap

| Phase | Zeitraum | Schwerpunkte | Meilensteine |
|---|---|---|---|
| 0 – Fundament | Monate 0–3 | Standortbestimmung (ACC-Workshop, KI-Audit: wo wird schon genutzt, wo improvisiert); Nutzungsrichtlinie; Stakeholder-Erstbefragung; Intake-Taxonomie final | Richtlinie in Kraft, Ausgangswerte erhoben, Strategie im Team beschlossen |
| 1 – Scaled Enablement | Monate 3–12 | Intake-Go-live; Wissensbasis ab [STICHTAG]; erste 3–5 Prompts und 1–2 Custom GPTs für Standardfälle; Lernroutine im Team | Alle Anfragen über Intake; verbindliche Dokumente für die Top-Kategorien; erster KPI-Bericht an die Geschäftsleitung |
| 2 – Empowering Peer | Monate 9–24 | Pilot-Fachbereich nach ca. 6 Monaten Intake-Daten wählen (Entscheidungslog Nr. 10); Self-Service-GPTs für 1–2 Fachbereiche; Workflow-Ebene prüfen (derzeit geparkt) | Messbarer Self-Service-Anteil; Kapazitätsnachweis |
| Laufend | – | Quartalsweiser Review: KPIs, Use-Case-Portfolio, Veränderungslast | Jährliche Neubewertung des Reifegrads |

Phase 1 und 2 überlappen bewusst. Bei voller Auslastung haben Intake und Wissensbasis immer Vorrang vor neuen GPTs.

## 8. Rollen (Teilrollen, keine neuen Stellen)

| Rolle | Aufgabe | Umfang |
|---|---|---|
| Sponsor (Leitung) | Priorisierung, Vorbildfunktion, Berichte an die Geschäftsleitung | – |
| KI- und Legal-Ops-Verantwortung | Use-Case-Portfolio, Prompts und GPTs, KPIs | zusammen mit der Kuratierung ca. 10–15 % Teamkapazität, verteilt auf 1–2 Personen (Entscheidungslog Nr. 7) |
| Wissensbasis-Kuratierung | verbindliche Dokumente, Metadatenqualität | (siehe oben) |
| Schnittstellen | IT (Enterprise-LLM, ITSM), Unternehmens-KI-Governance, Datenschutz | nach Bedarf |

## 9. Risiken

| Risiko | Gegenmaßnahme |
|---|---|
| Kapazität reicht nicht für den Aufbau | Veränderungslast steuern, Phase 0 und 1 strikt vor Phase 2; Quick Wins zuerst, damit früh Zeit frei wird |
| Die Strategie erreicht den Arbeitsalltag nicht (TR: bei 44 % der Unternehmensbefragten mit Strategie der Fall) | Rollen konkret beschreiben, Lernroutine, verbindliche Nutzungserwartung nach der Einführungsphase |
| Effizienzgewinne führen zu Kürzungen | Kapazitätsnachweis mit Wirkung berichten, nicht nur Einsparung (TR) |
| Qualitätsfehler durch KI-Ergebnisse | Prüfpflicht in der Richtlinie, Vier-Augen-Review, verbindliche Muster als Grundlage |
| Datenschutz und Vertraulichkeit | Datenklassen in der Richtlinie, Anschluss an Unternehmens-Governance und EU AI Act |
| Die Wissensbasis bleibt leer | Kuratierung als feste Teilrolle; Wissensteilen anerkennen (ACC Knowledge Management, kultureller Faktor) |

## 10. Vorentscheidungen und offene Punkte

Vorentschieden (Bestätigung im Team-Workshop, siehe [Entscheidungslog](entscheidungslog.md) Nr. 6–10):
1. Zielbild zweistufig: *Scaled Enablement*, dann *Empowering Peer*; „Reimagine“ nicht vor [ZIELJAHR].
2. Teilrollen mit zusammen ca. 10–15 % Teamkapazität, keine neue Stelle.
3. „KI zuerst“ wird nach ca. 3 Monaten Einführung für Standardfälle verbindlich.
4. Vier KPI-Gruppen an die Geschäftsleitung, einschließlich Kapazitätsnachweis.
5. Pilot-Fachbereich für Self-Service wird nach ca. 6 Monaten anhand der Intake-Daten gewählt.

Offen für den Workshop:
- Ist-Stufen in den sechs ACC-Bereichen (Abschnitt 6)
- Konkrete Verteilung der Teilrollen im Team
- [ZIELJAHR] und Startzeitpunkt der Roadmap
