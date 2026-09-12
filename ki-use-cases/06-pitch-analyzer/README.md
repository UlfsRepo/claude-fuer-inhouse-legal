# Use Case 6: Pitch Analyzer – Kanzleiangebote auf RFPs strukturiert auswerten

## Ziel

Ein GPT wertet Kanzleiangebote auf RFPs der Rechtsabteilung aus:
Vollständigkeitsprüfung, Preisnormalisierung (Blended Rate, Retainer,
Festpreis-Warenkorb), Abweichungen vom geforderten Service-Modell, Red Flags
aus Annahmen/Ausschlüssen und ein belegter Scoring-Vorschlag je
Bewertungskriterium.

**Output:** Executive Summary, Vergleichstabelle über alle Kanzleien,
Detailbericht je Kanzlei, Rückfragenliste, Entwurf einer
Finalisten-Empfehlung.

Vorbild ist das Marktprodukt lapco.legal („Scope it. Price it. Control it."):
Vergleichbarkeit entsteht durch strukturierte Eingabe, nicht durch
nachträgliche Analyse. Kernstück ist deshalb ein **Response-Template**
(Excel), das die Kanzleien ausfüllen – nicht der Prompt.

## Status quo (Pain Point)

1. Pitches kommen als unstrukturierte PDFs; Preis- und Leistungsvergleich ist
   Handarbeit und je Prüfer:in unterschiedlich.
2. Annahmen und Ausschlüsse (wo das Risiko steckt) gehen im Layout unter.
3. Keine dokumentierte, kriterienbasierte Entscheidungsgrundlage gegenüber
   unterlegenen Kanzleien.

## Mehrwert

1. Vergleichbare Angebote ab Eingang (Template erzwingt Struktur)
2. Objektivierte, dokumentierte Auswahlentscheidung (Scoring-Matrix)
3. Preisdaten wiederverwendbar für Kanzleisteuerung und spätere Verhandlungen
4. Blaupause für alle künftigen RFPs – und Vorstufe einer eigenen
   Pitch-Plattform, später mit Agent-Tools (z. B. Copilot Studio)
   automatisierbar

## Bausteine

1. **Response-Template (Excel)** – von den Kanzleien auszufüllen; typische
   Tabs: Instructions, Firm & Team, Scope Coverage (Module mit
   Coverage-Dropdowns), Service Model (Accept / Deviation je Anforderung),
   Pricing (Stundensatzraster, Festpreise für Sample Work Products,
   Retainer), Declarations (Conflicts, Haftpflicht, Referenzen,
   Annahmen/Ausschlüsse). Struktur darf von Bietern nicht verändert werden.
2. **Scoring-Matrix (Excel, intern)** – Kriterien + Gewichtungen (VOR
   Angebotseingang fixieren), Preisvergleich mit Blended-Rate-Berechnung
   über einen angenommenen Stundenmix, Scoring 1–5 mit Auto-Ranking.
3. **RFP-Ergänzungspassagen** – Einreichungsformat (nur ausgefülltes
   Template, .xlsx), Bewertungskriterien, definierte Sample Work Products
   für Festpreise, Vertraulichkeit.

## Prozessschritte und Umsetzung

1. **RFP finalisieren** → Einreichungsformat vorschreiben, Template anhängen.
2. **Kriterien & Gewichtungen festlegen** → in der Scoring-Matrix VOR
   Angebotseingang festzurren und dokumentieren.
3. **Prompt bauen** → [system-prompt.md](system-prompt.md); Wissensbasis:
   finales RFP + Kriterienliste.
4. **Angebote eingehen lassen** → nur ausgefüllte Templates akzeptieren;
   Nachforderung bei Formatabweichung.
5. **Auswertung** → Templates in den GPT hochladen; Ergebnisse in die
   Scoring-Matrix übertragen; Gremium entscheidet.
6. **Test** → [test-protokoll.md](test-protokoll.md) mit 2–3 Dummy-Angeboten
   VOR dem Echtlauf.

## ⚠️ Good-2-Know

1. **Gleichbehandlung:** Kriterien und Gewichtungen vor Angebotseingang
   fixieren; Änderungen danach dokumentieren. Der GPT schlägt vor, das
   Gremium entscheidet – so bleibt der Prozess gegenüber unterlegenen
   Kanzleien verteidigbar.
2. **Vertraulichkeit:** Angebote sind vertraulich; keine Inhalte einer
   Kanzlei in Rückfragen an andere Kanzleien tragen. Nur unternehmensseitig
   freigegebene KI-Umgebungen nutzen; keine unnötigen personenbezogenen
   Daten hochladen.
3. Excel-Uploads: ChatGPT liest .xlsx zuverlässig über Code Interpreter –
   bei Problemen Tabs als CSV exportieren.

## Ausbaustufen

- **Agent-Automatisierung** (z. B. Copilot Studio): Agent auf
  Dokumentbibliothek, automatischer Intake + Vollständigkeitsprüfung bei
  Eingang.
- **Eigene Pitch-Plattform** (lapco-Modell) mit Kanzlei-Logins – erst nach
  erfolgreichem Pilot sinnvoll.
- Panel-Performance-Datenbank: Scores + spätere Budgettreue je Kanzlei
  fortschreiben (Verknüpfung mit Use Case 5, Legal Invoice Checker).
