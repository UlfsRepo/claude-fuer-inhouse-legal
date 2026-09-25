# Schritt-für-Schritt-Leitfaden für Einsteiger:innen

**Für wen:** Alle, die ihre Arbeitsprozesse dokumentieren sollen und wenig
Erfahrung mit KI-Werkzeugen haben. Keine Vorkenntnisse nötig.
**Was du brauchst:** Zugang zu ChatGPT (Enterprise) *oder* Claude, ca. 45
Minuten Zeit pro Prozess, und deinen normalen Arbeitsalltag im Kopf.

---

## Worum geht es — in 4 Sätzen

Wir schreiben auf, wie unsere Arbeit wirklich läuft — Prozess für Prozess, in
einfachen Textdateien. Damit wird Wissen, das bisher nur in Köpfen steckt,
sichtbar und vertretbar. Und es ist die Grundlage dafür, dass KI uns künftig
Routinearbeit abnimmt. **Wichtig:** Es geht darum, dir Arbeit abzunehmen —
nicht darum, dich zu ersetzen. Dein Erfahrungswissen macht dich dabei
wertvoller, nicht überflüssiger.

## Der Gesamtablauf — wo stehst du gerade?

| Phase | Was passiert | Wer | Dein Aufwand |
|---|---|---|---|
| 1 — Inventur | Im Team-Workshop alle Prozesse des Bereichs auflisten | ganzes Team | 90 Min, einmalig |
| 2 — Dokumentation | Jede:r dokumentiert die eigenen Prozesse per KI-Interview | du | ~45 Min pro Prozess |
| 3 — Gegenlesen | Ein:e Kolleg:in prüft: "Könnte ich das morgen übernehmen?" | du + Vertretung | ~20 Min pro Prozess |
| 4 — KI-Workshop | Gemeinsam entscheiden, wo KI hilft — Ergebnis: KI-Prozessmap | Team + Leitung | 2–3 h, einmalig |
| 5 — Ausprobieren | 1–2 Piloten starten, Dokumente aktuell halten | Team | laufend |

Dieser Leitfaden führt dich durch **deinen Teil: Phase 2 und 3.**

---

## Phase 2: Deinen Prozess dokumentieren (Schritt für Schritt)

### Schritt 1 — Prozess auswählen (5 Min)

Öffne die Landkarte deines Bereichs (Datei `landkarte.md`, dein:e
Teamleiter:in sagt dir, wo sie liegt). Such dir einen Prozess aus, bei dem
**dein Name als verantwortlich** steht. Merke dir drei Dinge:
**Prozess-ID** (z. B. `UK-01`), **Prozessname** und dein **Bereichskürzel**.

> Kein Landkarten-Eintrag? Kein Problem — nimm den Prozess, den du am
> häufigsten machst, und kläre die ID später mit deiner Teamleitung.

### Schritt 2 — Das KI-Interview starten (2 Min)

**Mit ChatGPT Enterprise (Unternehmens-Umgebung):**
1. Öffne ChatGPT im Browser und melde dich an.
2. Klicke links in der Seitenleiste auf **GPTs**.
3. Suche den GPT **„Prozess-Interviewer"** (dein:e Admin hat ihn geteilt —
   findest du ihn nicht, frag nach dem Link).
4. Klicke ihn an und schreibe als erste Nachricht:
   > Interviewe mich zu meinem Prozess „<Name>". Mein Bereich ist <Bereich>,
   > Kürzel <XX>, die Prozess-ID ist <XX-NN>. Ich heiße <Vorname>.

**Mit Claude (falls Claude Code eingerichtet ist):**
1. Öffne Claude Code im Ordner der Prozesslandkarte.
2. Schreibe: `Interviewe mich zu meinem Prozess „<Name>"` — der Rest läuft
   automatisch, inklusive Speichern der Datei.

### Schritt 3 — Das Interview führen (20–40 Min)

Die KI stellt dir nacheinander Fragen. Dafür gibt es nur drei Regeln:

1. **Erzähl die Wirklichkeit, nicht das Lehrbuch.** Workarounds, Zurufe auf
   dem Flur, "das mache ich eigentlich anders als vorgeschrieben" — genau das
   ist wertvoll. Niemand wird dafür kritisiert.
2. **Antworte locker, in deinen Worten.** Du musst nichts formulieren — das
   macht die KI. Tippfehler sind egal. Wenn du etwas nicht weißt, sag es.
3. **Keine vertraulichen Details.** Keine Kundennamen, Preise, Gehälter oder
   Personalthemen. Sag stattdessen "ein Großkunde" oder "eine Kollegin".
   (Die KI ist angewiesen, dich zu erinnern, falls dir doch etwas rausrutscht.)

Gegen Ende kommen fünf Fragen zu deinem **Erfahrungswissen** ("Was würde ein
Neuling falsch machen?", "Woran merkst du früh, dass etwas schiefläuft?").
Nimm dir gerade hier Zeit — das ist der wertvollste Teil des ganzen Interviews.

> **Du musst nicht alles in einer Sitzung schaffen.** Sag einfach "Ich muss
> unterbrechen, bitte erstelle das Dokument mit dem jetzigen Stand" — offene
> Punkte werden als TODO markiert und du kannst später weitermachen.

### Schritt 4 — Das Dokument speichern (5 Min)

**Bei ChatGPT:** Am Ende bietet die KI das fertige Dokument als
**Download-Datei** an.
1. Auf den Download-Link klicken — die Datei landet in Deinem Downloads-Ordner.
2. Datei von dort an den vereinbarten Ablageort verschieben (fragt eure
   Teamleitung; z. B. der Team-Ordner `prozesslandkarte/prozesse/<bereich>/`).
   Fertig.

*Falls stattdessen ein grauer Textkasten (Codeblock) erscheint:* oben rechts
am Kasten **„Code kopieren"** → Texteditor öffnen (Windows: Editor/Notepad) →
einfügen → **Speichern unter** → Dateiname wie von der KI vorgeschlagen →
bei „Dateityp" **„Alle Dateien"** wählen, damit die Endung `.md` bleibt.

**Bei Claude Code:** Die Datei ist schon gespeichert — Claude nennt dir den Pfad.

### Schritt 5 — Kritisch gegenlesen (10 Min)

Lies das Dokument einmal in Ruhe durch und prüfe:
- Stimmen die Schritte und Regeln wirklich? (Die KI formuliert glatt — auch
  Falsches klingt bei ihr überzeugend. **Du** verantwortest die Richtigkeit.)
- Hat die KI etwas dazuerfunden? Dann korrigieren oder löschen.
- Stehen `TODO:`-Markierungen drin? Ergänze, was du beantworten kannst —
  einfach den TODO-Text durch die Antwort ersetzen.

Fertig? Ändere im Kopfbereich der Datei die Zeile `status: entwurf` in
`status: in_pruefung`.

---

## Phase 3: Review durch eine:n Kolleg:in

1. Schicke die Datei (oder den Ablage-Link) an deine Vertretung.
2. Die Leitfrage für sie/ihn: **„Könntest du diesen Prozess morgen allein
   ausführen, ohne anzurufen?"**
3. Alles, was fehlt, ergänzt ihr gemeinsam — meist sind es 10 Minuten Gespräch.
4. Danach setzt du `status: freigegeben`. Geschafft! 🎉

---

## Wenn etwas hakt

| Problem | Lösung |
|---|---|
| Ich finde den GPT „Prozess-Interviewer" nicht | Teamleitung oder Admin nach dem Link fragen (`chatgpt/einrichtung-custom-gpt.md` beschreibt die Einrichtung) |
| Die KI stellt zu viele Fragen auf einmal / wird formularhaft | Schreib: "Bitte immer nur 1–2 Fragen auf einmal" — sie passt sich an |
| Die KI hat etwas Falsches geschrieben | Im Chat korrigieren ("Schritt 3 stimmt nicht, richtig ist …") und um neue Ausgabe bitten — oder direkt in der Datei ändern |
| Mein Prozess ist riesig | Die KI schlägt von selbst vor, ihn zu teilen; sonst: "Lass uns nur den Teil X dokumentieren" |
| Ich habe versehentlich Vertrauliches genannt | Im Dokument prüfen und entfernen; im Zweifel Teamleitung fragen |
| Die Datei lässt sich nicht als `.md` speichern | Beim Speichern „Alle Dateien" als Dateityp wählen; zur Not als `.txt` speichern und die Endung im Datei-Explorer umbenennen |

## Häufige Sorgen — ehrlich beantwortet

- **„Dokumentiere ich mich damit weg?"** Nein. Dokumentiert wird der Prozess,
  damit Routine automatisierbar wird. Die Entscheidungen, Beziehungen und dein
  Urteilsvermögen — genau das, was im Kopfwissen-Teil steht — bleiben deine
  Rolle. Wer sein Wissen teilt, wird zur Schlüsselperson der KI-Einführung.
- **„Mein Prozess ist zu chaotisch zum Aufschreiben."** Dann ist er ein
  perfekter Kandidat: „Chaotisch" heißt meist nur, dass die Regeln in deinem
  Kopf stecken. Das Interview holt sie raus.
- **„Ich habe keine Zeit."** 45 Minuten pro Prozess — und jede künftige
  Übergabe, Vertretung und Einarbeitung wird damit kürzer.
