# Leitfaden: So dokumentierst du deine Prozesse

**Ziel:** Deine Prozesse so aufschreiben, dass (a) eine Vertretung sie morgen
ausführen könnte und (b) eine KI sie versteht. Nicht mehr, nicht weniger.
Pro Prozess solltest du mit **30–60 Minuten** rechnen.

## Grundhaltung

- **Beschreibe die Realität**, nicht das Ideal. Workarounds, Abkürzungen und
  „das mache ich immer per Zuruf" gehören ins Dokument — genau dort steckt der Wert.
- **Du wirst nicht wegdokumentiert.** Ziel ist, Routinearbeit an KI abzugeben und
  Zeit für die Arbeit zu gewinnen, die Urteilsvermögen und Beziehungen braucht.
  Dein Kopfwissen macht dich dabei wertvoller, nicht ersetzbarer.
- **Unfertig ist okay.** `status: entwurf` und Lücken mit `TODO:` markieren ist
  ausdrücklich erlaubt.

## Weg A — Selbst schreiben

1. Kopiere `vorlagen/prozess-template.md` nach
   `prozesse/<bereich>/<kürzel>-<nr>-<prozessname>.md`.
2. Fülle zuerst den YAML-Kopf und Abschnitt 1–2 (Zweck, Auslöser) aus.
3. Geh den Prozess einmal gedanklich als „stiller Film" durch und schreibe die
   Schritte in Abschnitt 5. Für jeden Schritt: Wer, was genau, womit, wie lange.
4. Danach die schwereren Abschnitte 6–9. Nimm dir Abschnitt 9 (Kopfwissen)
   zuletzt und mit den Leitfragen unten vor.
5. Abschnitt 11 (KI-Potenzial) lässt du leer — der wird gemeinsam ausgefüllt.

## Weg B — KI-Interview (empfohlen)

Meist schneller und gründlicher: Lass dich von Claude interviewen.

**Mit installiertem Skill (der einfachste Weg):** Wenn der Skill
`prozess-interview` eingerichtet ist (liegt unter `skills/prozess-interview/`,
Installation siehe README), reicht in Claude Code ein Satz wie
„Interviewe mich zu meinem Prozess <Name>" oder `/prozess-interview` —
Claude führt dann das komplette Interview, stellt die Kopfwissen-Fragen und
speichert das fertige Dokument am richtigen Ort. Weiter bei Punkt 3 unten
(kritisch gegenlesen!).

**Ohne Skill:**
1. Öffne Claude und gib ihm die Vorlage (`vorlagen/prozess-template.md`).
2. Prompt zum Kopieren:

   > Ich möchte einen meiner Arbeitsprozesse dokumentieren. Interviewe mich dazu
   > Schritt für Schritt: Stelle mir immer nur 1–2 Fragen auf einmal, hake nach,
   > wenn meine Antworten vage sind (besonders bei Entscheidungsregeln und
   > Erfahrungswissen), und fülle am Ende die angehängte Vorlage vollständig aus.
   > Abschnitt 11 bleibt leer. Der Prozess heißt: <Name>.

3. Antworte mündlich-locker — Claude formuliert aus. Rechne mit 20–40 Minuten.
4. **Lies das Ergebnis kritisch gegen:** Stimmen die Regeln? Hat Claude etwas
   dazuerfunden? Du bist verantwortlich für die Richtigkeit, nicht die KI.
5. Speichere die Datei unter `prozesse/<bereich>/…` und setze `status: entwurf`.

**Wichtig:** Keine vertraulichen Einzelfälle (Kundendaten, Personalia, Konditionen)
ins Interview geben. Beschrieben wird der Prozess, nicht der Fall.

## Kopfwissen heben — die Leitfragen für Abschnitt 9

Beantworte mindestens diese fünf Fragen ehrlich:

1. **Der Neuling-Test:** Was würde ein:e neue:r Kolleg:in bei diesem Prozess
   garantiert falsch machen, obwohl er/sie die Schritte kennt?
2. **Frühwarnzeichen:** Woran erkennst du früh, dass etwas schiefläuft — bevor
   es ein Problem wird?
3. **Ungeschriebene Erwartungen:** Was erwarten Empfänger, Chef:in oder Externe,
   ohne dass es je jemand gesagt hat (Tonfall, Timing, Form, Reihenfolge)?
4. **Erfahrungsregeln:** Welche Daumenregeln nutzt du? („Freitags nie versenden",
   „bei X immer erst Y anrufen", „wenn Z im Betreff steht, ist es dringend")
5. **Die Ausnahme-Frage:** Erzähl den letzten Fall, in dem der Prozess NICHT
   normal lief. Was hast du getan und woher wusstest du das?

## Qualitätscheck vor der Abgabe

- [ ] Vertretungs-Test: Könnte deine Vertretung den Prozess mit diesem Dokument
      morgen ausführen, ohne dich anzurufen?
- [ ] Jeder Schritt hat Wer/Was/Womit/Dauer/Ergebnis.
- [ ] Entscheidungen stehen als WENN/DANN-Regeln da, nicht als „nach Gefühl".
- [ ] Abschnitt 9 (Kopfwissen) hat mindestens 3 ehrliche Einträge.
- [ ] Keine vertraulichen Daten, Rollen statt Namen im Ablauf.

Dann: `status: in_pruefung` setzen und die Vertretung als Reviewer bitten.
