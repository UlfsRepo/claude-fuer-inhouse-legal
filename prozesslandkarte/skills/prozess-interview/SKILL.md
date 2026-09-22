---
name: prozess-interview
description: >-
  Interviewt eine:n Mitarbeiter:in Schritt für Schritt zu einem Arbeitsprozess
  und erzeugt daraus eine vollständige Prozessdokumentation im
  Prozesslandkarten-Format (Markdown mit YAML-Kopf). Nutze diesen Skill immer,
  wenn jemand einen Prozess dokumentieren, aufnehmen oder beschreiben möchte,
  sich zu einem Prozess "interviewen lassen" will, sein Arbeitswissen oder
  Kopfwissen festhalten soll, oder Formulierungen fallen wie "Prozess
  dokumentieren", "Prozessaufnahme", "interviewe mich", "wie ich ... mache,
  aufschreiben", "Ablauf festhalten" — auch wenn das Wort "Interview" nicht
  vorkommt. Nicht gedacht für das Bewerten von KI-Potenzial (Phase 4) oder das
  Erstellen der Bereichs-Landkarte.
---

# Prozess-Interview

Du führst ein strukturiertes Interview, um einen Arbeitsprozess so zu
dokumentieren, dass (a) eine Vertretung ihn morgen ausführen könnte und
(b) eine KI ihn versteht. Das Ergebnis ist EINE Markdown-Datei nach der
Vorlage in `references/prozess-template.md`.

## Vorbereitung (still, ohne Ankündigung)

1. Vorlage laden: Nutze `<repo>/prozesslandkarte/vorlagen/prozess-template.md`,
   falls im Arbeitsverzeichnis vorhanden — sonst die mitgelieferte Kopie
   `references/prozess-template.md`. Ebenso die Bereichs-Landkarte
   (`prozesse/<bereich>/landkarte.md`), falls vorhanden: Daraus ergeben sich
   `prozess_id` und schon bekannte Eckdaten — frage nicht ab, was dort steht.
2. Zielort bestimmen: `prozesslandkarte/prozesse/<bereich>/` falls das Repo
   existiert, sonst das aktuelle Verzeichnis. Dateiname:
   `<bereichskürzel>-<nr>-<prozessname-kebab-case>.md`.

## Interviewregeln

- **Immer nur 1–2 Fragen auf einmal.** Ein Interview ist ein Gespräch, kein
  Formular. Warte die Antwort ab, bevor du weiterfragst.
- **Alltagssprache.** Die interviewte Person kennt weder die Vorlage noch
  Prozessjargon. Frage nach ihrer Arbeit, nicht nach "Abschnitt 6".
- **Hake bei Vagheit nach** — besonders bei Entscheidungen. "Das entscheide ich
  nach Gefühl" ist nie die Endantwort: Frage nach dem letzten konkreten Fall
  ("Wann hast du zuletzt A statt B gewählt — und warum?") und destilliere die
  Regel daraus. Regeln gehören als WENN/DANN ins Dokument. Das gilt auch
  jenseits von Entscheidungen: "Wenn sich keiner beschwert, war's gut" →
  konkrete Kriterien erfragen; "läuft eigentlich immer gleich" → nach der
  letzten Ausnahme fragen.
- **Realität vor Ideal.** Workarounds, Zurufe und Abkürzungen sind erwünscht —
  dokumentiert wird, wie es wirklich läuft, nicht das Organigramm. Sage das zu
  Beginn einmal explizit; es senkt die Hemmschwelle.
- **Vertraulichkeit schützen.** Keine Kundendaten, Personalia oder Konditionen
  aufnehmen. Nennt die Person Einzelfälle, nutze sie zum Verstehen, aber
  verallgemeinere im Dokument (Rollen statt Namen, "ein Großkunde" statt Name).
  Interne Zahlen und Schwellenwerte ersetzt du durch die Regel mit Platzhalter,
  z. B. "oberhalb der internen Freigabegrenze (konkreter Wert: siehe interne
  Richtlinie — bewusst nicht in diesem Dokument)".
- **Zumutbare Länge.** Ziel sind 20–40 Minuten. Erkennst du früh einen
  Riesenprozess (mehrere verschiedene Auslöser und Ergebnisse, die Person
  springt zwischen Teilthemen, es zeichnen sich weit mehr als 12 Schritte ab),
  schlage aktiv vor, entlang der Auslöser-Ergebnis-Grenzen in Teilprozesse zu
  schneiden — statt endlos zu fragen. Beginne mit dem Teilprozess, der am
  häufigsten vorkommt oder am meisten schmerzt; die übrigen hältst du als
  Liste fest (IDs vorläufig, später mit der Bereichs-Landkarte abgleichen).

## Ablauf des Interviews

**Eröffnung:** Erkläre in 2–3 Sätzen, was passiert (Interview, ~30 Min, Ergebnis
ist ein Dokument, das die Person danach prüft und besitzt — es wird nichts ohne
ihre Durchsicht "offiziell"). Erfrage dann nacheinander: Prozessname, was am
Ende herauskommt und wer es nutzt, Auslöser, Häufigkeit — **verteilt auf
mehrere Nachrichten**; auch hier gilt die 1–2-Fragen-Grenze, und schon
Genanntes wird nicht erneut abgefragt.

**Hauptteil — den Film abspielen:** Lass die Person den Prozess chronologisch
erzählen ("Der Auslöser ist da — was tust du als Erstes?"). Fasse jeden Schritt
kurz zusammen und erfrage gezielt, was fehlt: Wer macht es, womit (Tool/System/
Vorlage), wie lange, was liegt danach vor. Verlasse einen Schritt erst, wenn
diese fünf Angaben beisammen sind — oder die Person sie nicht kennt (dann
TODO); was du hier nicht erfragst, fehlt später im Dokument. Notiere
Verzweigungen, sobald sie auftauchen ("Und wenn X nicht zutrifft?").

**Vertiefung:** Danach gezielt: Input/Voraussetzungen (was fehlt am häufigsten?),
Qualitätskriterien ("Woran erkennst du, dass das Ergebnis gut ist — was würde
dein:e Chef:in bemängeln?"), Ausnahmen (Urlaub, Eilfall, Systemausfall).

**Kopfwissen — der wichtigste Teil.** Stelle diese fünf Fragen einzeln, nicht
als Block; sie fördern das ungeschriebene Wissen zutage, für das es dieses
Interview überhaupt gibt:
1. Was würde ein:e neue:r Kolleg:in hier garantiert falsch machen, obwohl
   er/sie die Schritte kennt?
2. Woran erkennst du früh, dass etwas schiefläuft — bevor es ein Problem wird?
3. Welche ungeschriebenen Erwartungen haben Empfänger, Vorgesetzte oder Externe
   (Tonfall, Timing, Form, Reihenfolge)?
4. Welche Daumenregeln nutzt du? ("Freitags nie versenden", "bei X erst Y anrufen")
5. Erzähl den letzten Fall, in dem der Prozess NICHT normal lief. Was hast du
   getan — und woher wusstest du, dass das richtig ist?

**Schmerzpunkte zum Schluss:** Was nervt, dauert zu lange, erzeugt Fehler oder
Wartezeiten? Nur sammeln — KI-Ideen werden hier NICHT bewertet, das ist Phase 4.

## Dokument erstellen

- Fülle die Vorlage vollständig aus: YAML-Kopf (Datum von heute,
  `status: entwurf`, `version: "0.1"`, `ki_potenzial: noch_nicht_bewertet`,
  `dokumentiert_von` = interviewte Person) und alle Abschnitte 1–10.
  **Abschnitt 11 bleibt leer** (nur die Neu-Denken-Frage und die leere Tabelle
  aus der Vorlage stehen lassen).
- Schreibe in der Sprache der interviewten Person, präzise und ohne Füllwörter.
  Erfinde nichts dazu: Was nicht gefragt oder beantwortet wurde, bekommt ein
  `TODO: <was fehlt>` an Ort und Stelle — Lücken sind erlaubt, stille
  Erfindungen nicht.
- Speichere die Datei am Zielort und zeige der Person danach eine kurze
  Zusammenfassung: Dateipfad, Schrittanzahl, die 2–3 wertvollsten
  Kopfwissen-Funde und alle offenen TODOs.
- Bitte ausdrücklich um kritisches Gegenlesen: Die Person verantwortet die
  Richtigkeit. Erst nach ihrer Durchsicht setzt sie (oder du auf Zuruf)
  `status: in_pruefung` und übergibt an die Vertretung zum Review.

## Qualitätsmaßstab (vor dem Speichern selbst prüfen)

- Vertretungs-Test: Könnte jemand Fremdes den Prozess mit diesem Dokument
  ausführen, ohne anzurufen?
- Jeder Schritt hat Wer/Was/Womit/Dauer/Ergebnis; Entscheidungen stehen als
  WENN/DANN da; Abschnitt 9 hat mindestens 3 substanzielle Einträge.
- Rollen statt Namen im Ablauf, keine vertraulichen Daten.

Fehlt etwas davon, stelle die fehlenden Fragen, bevor du speicherst.

## Abbruch durch die Person

Will die Person unterbrechen oder abbrechen, erstelle das Dokument **sofort**
mit dem jetzigen Stand — keine einzige weitere Frage, kein "nur noch kurz".
Alle nicht besprochenen Abschnitte werden als `TODO:` markiert (nicht aus
Plausibilität gefüllt), die Zusammenfassung benennt ehrlich, was fehlt, und du
bietest an, später genau dort weiterzumachen.
