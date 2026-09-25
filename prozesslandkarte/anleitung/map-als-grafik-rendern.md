# KI-Prozessmap als Grafik rendern

Die Markdown-Map bleibt die **Quelle der Wahrheit** (maschinenlesbar,
versionierbar, KI-verarbeitbar). Für Workshops, Management-Präsentationen und
den Rollout gibt es zusätzlich die **Präsentationsschicht**: eine grafische
Ein-Seiten-Darstellung im Stil der bekannten Prozessmap-Poster — Steckbrief,
Zielbild-Kennzahlen, Schritt-Matrix mit Automatisierungs-Tachos,
Verteilungs-Donut, Reifegrad, Roadmap, SLA, Risiken & Prinzipien.

**Vorlage:** `vorlagen/prozessmap-visual-template.html` — ein fertig
gestaltetes Referenz-Render des Beispiels
`beispiele/unternehmenskommunikation/uk-03-map-krisenkommunikation.md`.
Die KI tauscht nur Inhalte aus; Layout, Farben (hell/dunkel geprüft,
farbfehlsichtigkeits-validiert) und Struktur bleiben unverändert.
Technische Hinweise (Tacho-Prozente, Donut-Segmente, Spalten ergänzen)
stehen als Kommentar am Anfang der Vorlage.

## Weg A — Claude (Claude Code)

Ein Satz genügt:

> Rendere die KI-Prozessmap `<pfad/zur/map.md>` als Grafik nach der Vorlage
> `vorlagen/prozessmap-visual-template.html` — nur Inhalte austauschen,
> Layout und Farben beibehalten — und veröffentliche sie als privates
> Artifact (oder: speichere sie als HTML-Datei neben der Map).

Claude liest beide Dateien, baut die Seite und liefert einen privaten Link
(teilbar über das Share-Menü der Seite) oder eine `.html`-Datei, die sich in
jedem Browser öffnen lässt.

## Weg B — ChatGPT Enterprise

**Der einfache Weg:** Wenn der GPT „Prozessmap-Studio" eingerichtet ist
(`chatgpt/einrichtung-custom-gpt.md`), genügt: GPT öffnen, Map anhängen,
„Poster bitte" — das HTML kommt als Download-Datei. Der Rest dieses
Abschnitts ist der Fallback ohne GPT:

Normaler Chat, **zwei Dateien anhängen**: die Map (`…-map-….md`) und die
Vorlage (`prozessmap-visual-template.html`). Prompt zum Kopieren:

> Erstelle aus der angehängten KI-Prozessmap (Markdown) eine grafische
> Ein-Seiten-Darstellung. Nutze dafür exakt die angehängte HTML-Vorlage:
> Tausche NUR die Inhalte aus (Texte, Prozentwerte, Tabellenzeilen, Anzahl
> der Schritt-Spalten) und lasse CSS, Farb-Variablen und Seitenstruktur
> unverändert — die Hinweise im Kommentar am Anfang der Vorlage beachten
> (Tacho: stroke-dasharray="Prozent 100"; Donut-Anteile ergeben 100;
> Sonderzeichen HTML-escapen). Titel, Untertitel und Meta-Zeile an den
> Prozess anpassen. Gib die komplette HTML-Datei als einen Codeblock aus.

Danach: Codeblock kopieren → als `<prozessname>-map.html` speichern
(Texteditor, Dateityp „Alle Dateien") → Doppelklick öffnet die Grafik im
Browser. Zum Teilen die Datei ablegen (z. B. SharePoint) oder als PDF
exportieren: Browser → Drucken → „Als PDF speichern" — die Vorlage bringt
Druckstile mit (A4 Querformat, saubere Seitenumbrüche, helle Druckfarben),
es ist nichts einzustellen. Hinweis: Bei sehr langen HTML-Ausgaben bricht
ChatGPT gelegentlich mitten im Codeblock ab — dann „bitte fortsetzen"
schreiben und die Teile zusammenfügen; die Ausgabe als Codeblock anfordern,
nicht im Canvas.

## Qualitätscheck vor dem Teilen (2 Minuten)

- [ ] Alle Schritte der Markdown-Map sind als Spalten da; %-Werte stimmen
      mit der Map überein (Tacho, Zahl und Textband je Schritt identisch)
- [ ] Donut-Anteile = Verteilungstabelle der Map; Summe der Mittelwerte ≈ 100
- [ ] Kein Inhalt erfunden oder weggelassen (Stichprobe: Risiken, Roadmap)
- [ ] Umlaute und Sonderzeichen korrekt dargestellt
- [ ] Vertraulichkeitsstufe geprüft: Eine Grafik wird schneller weitergeleitet
      als eine Datei — es gilt dieselbe Stufe wie für die Markdown-Map

## Grundsatz

Erst die Markdown-Map aktualisieren, dann neu rendern — nie umgekehrt.
Wer Inhalte nur in der Grafik ändert, trennt Präsentation und Wahrheit.
