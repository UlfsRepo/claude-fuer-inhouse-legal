# ChatGPT Enterprise: Custom GPT „Prozess-Interviewer" einrichten

Diese Anleitung richtet sich an Administrator:innen oder Power-User, die den
Interview-Skill einmalig als Custom GPT für das Team bereitstellen. Dauer:
ca. 15 Minuten. Es sind keine Programmierkenntnisse nötig.

## Voraussetzungen

- Zugang zu ChatGPT Enterprise mit der Berechtigung, GPTs zu erstellen
  (Standard in den meisten Enterprise-Workspaces; sonst IT/Workspace-Admin fragen).
- Zwei Dateien aus diesem Repository:
  - `chatgpt/gpt-instructions-prozess-interview.md` (die Anweisungen)
  - `vorlagen/prozess-template.md` (die Vorlage, wird als Wissensdatei hochgeladen)

## Einrichtung Schritt für Schritt

1. ChatGPT öffnen → in der Seitenleiste auf **GPTs** klicken → oben rechts
   **„+ Erstellen"** (Create a GPT).
2. Oben auf den Reiter **„Konfigurieren"** (Configure) wechseln — nicht den
   Chat-Assistenten links benutzen, das Konfigurieren von Hand ist zuverlässiger.
3. **Name:** `Prozess-Interviewer`
4. **Beschreibung:**
   `Interviewt dich zu einem deiner Arbeitsprozesse und erstellt daraus eine vollständige Prozessdokumentation im Prozesslandkarten-Format. Dauer ca. 30 Minuten.`
5. **Instructions:** Den gesamten Text aus
   `chatgpt/gpt-instructions-prozess-interview.md` (ab der Trennlinie `---`)
   kopieren und einfügen.
6. **Knowledge (Wissen):** Auf **„Dateien hochladen"** klicken und
   `vorlagen/prozess-template.md` hochladen.
7. **Funktionen (Capabilities):** Webbrowsing und Bilderzeugung
   **deaktivieren** — das Interview braucht sie nicht. **Code Interpreter
   aktivieren:** Damit gibt der GPT das fertige Dokument als
   **Download-Datei** aus statt als Codeblock — das erspart den Umweg über
   Texteditor und „Speichern unter" und ist der größte
   Vereinfachungs-Hebel für ungeübte Nutzer:innen.
8. **Conversation Starters** (Gesprächsvorschläge) eintragen, z. B.:
   - `Interviewe mich zu einem meiner Arbeitsprozesse.`
   - `Ich möchte einen Prozess dokumentieren, weiß aber nicht, wo ich anfangen soll.`
9. Oben rechts **„Erstellen"/„Teilen"** klicken → Sichtbarkeit **„Nur für
   Personen mit Link"** oder **„Für den Workspace"** wählen (je nach
   Rollout-Plan). Nicht „öffentlich".
10. **Selbst testen** (Pflicht vor dem Rollout): die Testfälle aus
    `tests/testplan.md` durchspielen.

## Zweiter GPT: „Prozessmap-Studio" (Phase 4 + Poster, empfohlen)

Damit niemand Prompts und Anhänge zusammensuchen muss, gibt es die Map- und
Poster-Erstellung als eigenen GPT. Einrichtung wie oben, mit diesen Werten:

1. **Name:** `Prozessmap-Studio` · **Beschreibung:**
   `Hänge eine fertige Prozessdokumentation an und erhalte die KI-Prozessmap und das visuelle Poster als Download.`
2. **Instructions:** aus `chatgpt/gpt-instructions-prozessmap-studio.md`
   (ab der Trennlinie).
3. **Knowledge (3 Dateien):** `vorlagen/ki-prozessmap-template.md`,
   `anleitung/ki-potenzial-analyse.md`, `vorlagen/prozessmap-visual-template.html`.
4. **Funktionen:** **Code Interpreter an** (Datei-Downloads), Rest aus.
5. **Gesprächsvorschlag:** `Erstelle aus der angehängten Prozessdokumentation Map und Poster.`

Nutzung danach: GPT öffnen → eigene `.md`-Datei anhängen → „Map und Poster
bitte" → zwei Download-Dateien. Die Einzel-Prompts in
`chatgpt/prompt-ki-prozessmap.md` und `anleitung/map-als-grafik-rendern.md`
bleiben als Fallback für Nutzer:innen ohne GPT-Zugriff gültig.

**Alternative für Workspaces mit „Projekten":** Statt zweier GPTs können beide
Instruktionssätze auch als ein ChatGPT-**Projekt** mit den Vorlagen als
Projektdateien angelegt werden — Teammitglieder starten dann Chats direkt im
Projekt, ganz ohne Anhänge. Funktional gleichwertig; GPTs sind leichter
teamweit teilbar, Projekte schneller angelegt.

## Wo landen die fertigen Dokumente?

ChatGPT speichert keine Dateien in eurer Ablage. Der GPT gibt das fertige
Dokument als Markdown-Codeblock aus; die Mitarbeiter:in kopiert ihn und
speichert ihn als `.md`-Datei am vereinbarten Ablageort (z. B. SharePoint-
Ordner `prozesslandkarte/prozesse/<bereich>/`). Legt diesen Ablageort VOR dem
Rollout fest und schreibt ihn in die Beschreibung des GPT oder in den
Einsteiger-Leitfaden.

**Tipp:** `.md`-Dateien lassen sich mit jedem Texteditor (auch Notepad)
erstellen: neue Textdatei anlegen, Inhalt einfügen, beim Speichern die Endung
`.md` statt `.txt` verwenden.

## Anpassung an das eigene Unternehmen (Checkliste)

Das Framework ist bewusst generisch. Vor dem Rollout im Unternehmen anpassen:

- [ ] **Ablageort** für fertige Dokumente festlegen und in GPT-Beschreibung
      bzw. Leitfaden eintragen (z. B. SharePoint/Teams-Ordner).
- [ ] **Bereichskürzel** vergeben (z. B. UK, HR, FIN …) und in der jeweiligen
      Bereichs-Landkarte notieren.
- [ ] **Vertraulichkeitsregeln** schärfen: Welche Informationsklassen dürfen
      keinesfalls ins Dokument (Kundendaten, Preise, Personalia, …)? Ergänzt
      unternehmensspezifische No-Gos direkt in den Instructions unter
      „Schütze Vertraulichkeit".
- [ ] **Interne Systemnamen** prüfen: Der GPT übernimmt Systemnamen aus den
      Antworten — klären, ob interne Systemnamen ins Dokument dürfen.
- [ ] **Freigabe durch IT/Datenschutz** einholen, bevor der GPT geteilt wird
      (Enterprise-Workspace: Eingaben werden laut OpenAI nicht zum Training
      verwendet — trotzdem interne Richtlinie prüfen).
- [ ] **Pilotbereich** wählen und die Tests aus `tests/testplan.md` mit 1–2
      echten Kolleg:innen durchführen, bevor alle eingeladen werden.

## Grenzen gegenüber der Claude-Skill-Variante

- Der Custom GPT kann Dateien weder lesen (außer Knowledge/Upload im Chat)
  noch speichern — das Kopieren/Ablegen übernimmt der Mensch.
- Er kennt die Bereichs-Landkarte nicht automatisch; Bereichskürzel und
  Prozessnummer nennt die interviewte Person (steht im Einsteiger-Leitfaden).
- Instructions-Feld ist auf 8.000 Zeichen begrenzt — die mitgelieferten
  Anweisungen passen; bei eigenen Ergänzungen Länge im Blick behalten.
