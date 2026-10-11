---
name: management-deck-review
description: Dreistufiges Review einer Management-Präsentation vor der Abgabe an eine Führungskraft — (1) KI-Sprach-Check gegen einen Musterkatalog generierter Texte, (2) Stakeholder-Check gegen ein lokal gepflegtes Profil der Adressatin bzw. des Adressaten, (3) Kürzungsvorschlag nach Zeitbudget und Gesprächsziel. IMMER verwenden, wenn der Nutzer ein Deck, einen Bericht oder eine Vorlage „auf KI-Sprache prüfen", „aus Sicht von <Person> lesen", „kürzen" oder „vor dem Termin gegenchecken" will.
---

# Management-Deck-Review

Prüft eine Präsentation oder einen Bericht so, wie die Adressatin ihn lesen wird — bevor er abgegeben wird. Kern-Idee: Die meisten Management-Decks scheitern nicht am Inhalt, sondern an drei vermeidbaren Dingen: Sie klingen generiert, sie beantworten die Fragen der Adressatin nicht, und sie sind zu lang für den Termin.

Der Skill ersetzt kein Urteil. Er macht Muster sichtbar, die der Autor nach der zehnten Überarbeitung nicht mehr sieht.

## Voraussetzungen

### 1. Das Dokument

PPTX, DOCX, PDF oder Markdown. Bei PPTX **Notes mitlesen** — dort stehen oft die Aussagen, die der Autor nur mündlich machen will; sie gehören in die Bewertung, aber nicht in Kürzungsvorschläge.

### 2. Rahmen des Termins (immer abfragen, wenn nicht genannt)

Drei Fragen, keine mehr:

1. **Zeitbudget und Modus:** Wie lang ist der Termin, wird präsentiert oder vorab gelesen?
2. **Gesprächsziel:** Was soll am Ende stehen — Information, gemeinsames Bild, Entscheidung, Freigabe?
3. **Schärfe des Sprach-Checks:** streng (jede Stelle) oder nur auffällige Fälle?

Ohne diese drei Antworten ist ein Kürzungsvorschlag Raten.

### 3. Lokales Stakeholder-Profil (für Stufe 2)

Der Stakeholder-Check arbeitet mit einer **lokalen Datei des Nutzers** (nicht im Repo, nicht in der Cloud eines Dritten), z. B. `stakeholder-<name>.md`. Existiert sie nicht, lege sie im Interview an. Struktur:

```markdown
# Stakeholder-Profil: <Name, Rolle>

## Quelle
<Woher stammt das Profil: eigenes Leitbild der Person, Beobachtung, Hörensagen? Stand?>

## Überzeugung
<Was die Person für den Kern ihrer Rolle hält — in ihren Worten, wenn vorhanden>

## Kompass (Achsen, an denen sie bewertet)
| Achse | Leitsatz | Was sie daran prüft |
|---|---|---|
| <z. B. Entscheidungsreife> | | |
| <z. B. Risikotransparenz> | | |
| <z. B. Geschäftsnähe> | | |

## Spannungsfelder (die sie selbst benennt oder erkennbar lebt)
- <Pol A ↔ Pol B>

## Ihre eigenen Prüffragen
- <Fragen, die sie sich selbst stellt — eignen sich als Prüffragen ans Dokument>

## Beobachtetes Verhalten (mit Datum)
- <Kommunikationsstil, bevorzugte Formate, Reizthemen, Entscheidungsverhalten>

## Ausdrückliche Wünsche
- <z. B. Vorlauf vor Terminen, Du/Sie, Sprache, Format>
```

**Regel:** Beobachtung schlägt Selbstbild. Wenn ein Leitbild sagt „ich will das Wesentliche auf einer Seite" und die Beobachtung sagt „liest zuerst die Detailtabellen", gilt die Beobachtung — und die Abweichung wird im Output benannt.

**Regel:** Nichts erfinden. Wo das Profil zu einer Frage nichts hergibt, steht im Output „nur aus dem Leitbild abgeleitet" oder „hier rate ich".

Vertrauliche Details (Namen, Zitate, interne Beobachtungen) gehören nur in diese lokale Datei — nie in Prompts an fremde Systeme ohne Prüfung (Skill `vertraulichkeits-gate`).

## Workflow

### Stufe 0: Vollständigkeits-Check (vor allem anderen)

Suche nach Platzhaltern: `[...]`, `TBD`, `XXX`, `??`, `[Termin]`, `[Name]`, `[bestätigen]`. Liste sie mit Folien- oder Seitennummer. Wenn der Termin näher als der zugesagte Vorlauf ist, steht das **an erster Stelle des Outputs**, vor jeder Sprachkritik.

Prüfe außerdem Querverweise („siehe Folie N") — sie brechen bei jeder Kürzung.

### Stufe 1: KI-Sprach-Check

Die Signatur generierter Texte liegt selten in einzelnen Wörtern, sondern in **Mustern, die sich über das Dokument wiederholen**. Prüfe in dieser Reihenfolge:

**Muster A — Zahlwort-Headlines.** „Drei Erkenntnisse", „Vier Schritte zum Ziel", „Zwei Risiken bleiben". Einzeln harmlos; ab drei im Dokument ein Listicle-Muster. Regel: höchstens zwei behalten (die, bei denen die Zahl selbst die Botschaft ist), die anderen auf die Aussage umstellen.

**Muster B — Chiasmus und Antithese.** „X statt Y", „nicht nur …, sondern …", „nicht A, sondern B", „schnell, aber unsicher". Zähle die Fälle. Eine beobachtete, präzise Antithese darf bleiben; der Rest wird zur schlichten Aussage.

**Muster C — Headline-Interpunktion.** Doppelpunkt-Einleitungen („Ausgangslage: …"), Semikolon-Headlines, Dreier-Reihungen in der Überschrift. Mehr als zwei im Dokument sind ein Muster.

**Muster D — Topoi aus KI-Vision-Texten.** „Freiraum für Wertschöpfung", „Grundlage gelegt", „Hebel", „Wirkung entfalten", „ganzheitlich", „bewusst" als Füller, rhetorische Fragen als Bullet („Sind wir bereit?"), abstrakte Beruhigungsformeln („Qualität bleibt dabei der Maßstab").

**Muster E — Vokabular der Adressatin.** Wenn das Dokument Leitbegriffe der Adressatin wörtlich übernimmt (aus ihrem Profil, ihren Mails, ihrem Kompass), prüfe: Wirkt es als Anschluss oder als Anbiederung? Faustregel: Ihren Wortlaut zitieren ist gut; ihre Vokabel als eigene Formulierung übernehmen ist riskant.

**Muster F — Wiederholte Kernphrase.** Dieselbe Wendung dreimal im Dokument (z. B. „nah am Kunden") wirkt generiert, auch wenn sie beim ersten Mal stark war. Einmal behalten.

Daneben: echte Sprachfehler (Grammatik, abgebrochene Sätze, Folien, die nicht allein stehen können, obwohl sie es sollen).

**Output je Fund:** Folie/Seite → Zitat → Problem (ein Halbsatz) → Alternativformulierung. Bei „nur auffällige Stellen" nur Muster A–C und die fünf stärksten Einzelfälle.

### Stufe 2: Stakeholder-Check

Lies das Stakeholder-Profil. Dann:

1. **Erster Eindruck (30 Sekunden).** Was nimmt die Adressatin beim Überfliegen mit? Ist sofort klar, was Priorität hat und was von ihr erwartet wird?
2. **Kompass-Prüfung.** Je Achse ihres Profils: stark / ausreichend / schwach / fehlt — mit Zitat der relevanten Stelle. Eine Achse, die im Profil steht und im Dokument gar nicht vorkommt, ist der wichtigste Befund.
3. **Spannungsfeld-Prüfung.** Welche ihrer Spannungen berührt das Dokument? Kippt es zu einem Pol (z. B. nur Tempo, keine Sorgfalt; nur Breite, keine Priorisierung)?
4. **Innere Widersprüche.** Behauptet das Dokument auf einer Seite etwas, das eine andere Seite widerlegt (z. B. „Wir befähigen die Fachbereiche" neben einer Maßnahmentabelle, in der fast überall die eigene Abteilung als verantwortlich steht)? Diese Widersprüche findet die Adressatin zuerst.
5. **Simulierte Rückfragen.** 3–6 Fragen, die sie stellen würde — in ihrer Stimme, als simuliert gekennzeichnet, abgeleitet aus Kompass und Spannungsfeldern. Jede Frage, die das Dokument schon beantwortet, ist keine.
6. **Positionierungsrisiken für den Autor.** Wo könnte das Dokument ungewollt wirken: zu viel Ego, zu wenig klare Linie, Kritik am Unternehmen, für die dem Autor (noch) das Standing fehlt, Übergriff in das Terrain der Adressatin (besonders bei Themen, in denen der Autor mehr Expertise hat als sie, die Richtung aber bei ihr liegt)?
7. **Änderungsvorschläge.** Je Schwachstelle: Zitat → Problem → Vorschlag → erwarteter Effekt (idealerweise: „beantwortet Rückfrage N, bevor sie gestellt wird").
8. **Gesamturteil.** 1–10, ein Satz, plus Grundlage: „Leitbild" oder „Leitbild + Beobachtung" mit Stand.

### Stufe 3: Kürzungsvorschlag

Rechne zuerst: **Präsentiert** → etwa zwei Minuten je Inhaltsfolie, ein Drittel der Zeit für Gespräch. **Vorab gelesen** → Deck muss allein stehen, Kürzung konservativ, Summary-Folie wird wichtiger.

Dann ordne jede Folie einer von vier Klassen zu:

| Klasse | Kriterium |
|---|---|
| **Kern** | Trägt direkt zum Gesprächsziel bei oder ist von der Adressatin ausdrücklich erbeten (z. B. ein Statusbericht, um den sie gebeten hat) |
| **Zusammenlegen** | Zwei Folien laufen entlang derselben Struktur (z. B. Zielsätze → Zielzustand und Zielsätze → Lücke) — eine Tabelle mit drei Spalten ersetzt beide |
| **Anhang** | Belegt eine Kern-Folie im Detail; wird nur bei Nachfrage gebraucht |
| **Nur mündlich** | Hohes Fehlwirkungsrisiko (Kulturkritik, Hypothesen, Namen) oder kein Beitrag zum Ziel — als Gesprächsangebot besser als auf Folie |

Gib zwei Varianten: **empfohlen** (passt ins Zeitbudget) und **aggressiv** (maximale Gesprächszeit). Beide mit Zuordnungstabelle alt → neu.

Zum Schluss die **Folgearbeiten**: Querverweise neu nummerieren, Anhang umbenennen, Angaben, die sich bis zum Termin ändern können (offene Entscheidungen, Gremientermine), markieren.

## Output-Format

```
# Review: <Dateiname>
Stand · Termin · Format · Gesprächsziel

## 0. Vollständigkeit
<Platzhalterliste; Vorlauf-Hinweis, falls relevant>

## 1. KI-Sprach-Check
### Muster A–F (je mit Tabelle Folie | Jetzt | Vorschlag)
### Sprachfehler

## 2. Stakeholder-Check: <Name>
Zweck · Erster Eindruck
### Kompass (Tabelle Achse | Bewertung | Begründung)
### Spannungsfelder
### Simulierte Rückfragen
### Positionierungsrisiken
### Änderungsvorschläge
### Gesamturteil (x/10) · Grundlage

## 3. Kürzungsvorschlag
### Empfohlen (Tabelle Neu | Alt | Anmerkung)
### Anhang · Nur mündlich
### Aggressive Variante
### Folgearbeiten
```

## Grenzen

- Der Stakeholder-Check ist ein Denkwerkzeug, keine Vorhersage. Er findet Blindstellen; er sagt nicht, wie die Person tatsächlich reagiert.
- Der Sprach-Check erkennt Muster, keine Autorschaft. Ein Mensch kann alle sechs Muster selbst produzieren; ein KI-Text kann keines zeigen. Bewertet wird die Wirkung auf die Leserin, nicht die Herkunft.
- Keine Kürzung ohne die drei Rahmenfragen. Wer das Zeitbudget nicht kennt, kürzt das Falsche.
- Nichts aus dem Stakeholder-Profil darf so formuliert werden, dass es als tatsächliche Aussage der Person weitergegeben werden könnte.
