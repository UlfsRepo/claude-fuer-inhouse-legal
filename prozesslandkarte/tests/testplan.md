# Testplan: Prozess-Interview vor dem Go-Live

**Zweck:** Bevor der Interview-Skill (Claude) bzw. der Custom GPT (ChatGPT
Enterprise) an Mitarbeitende geht, wird er mit diesen Testfällen geprüft.
**Wer testet:** 1–2 Personen, die das Framework kennen (z. B. Admin + eine
Pilotperson). **Dauer:** ca. 60–90 Minuten für alle Fälle.
**Bewertung:** Für jeden Testfall den `tests/pruefbogen.md` ausfüllen.
**Go-Live-Kriterium:** Testfälle 1–4 vollständig bestanden; Testfall 5–6 ohne
kritische Befunde.

## So wird getestet

Der/die Tester:in spielt die interviewte Person und antwortet **nur** mit den
Informationen aus der jeweiligen Fixture-Datei (`tests/fixtures/…`) — wie ein
Drehbuch: Auf jede Frage der KI die passenden Sätze aus der Fixture geben,
gern wörtlich. Was nicht in der Fixture steht, wird mit „Weiß ich nicht" oder
„Haben wir nicht" beantwortet (das ist Absicht: es testet den Umgang mit Lücken).

Jeden Testfall in **beiden Umgebungen** fahren, die live gehen sollen
(ChatGPT-GPT und/oder Claude-Skill).

---

## Testfall 1 — Normalfall: vollständige Antworten
**Fixture:** `fixtures/testfall-1-vollstaendig.md` (Prozess „Pressemitteilung versenden")
**Start-Prompt:** `Interviewe mich zu meinem Prozess „Pressemitteilung versenden". Mein Bereich ist Unternehmenskommunikation, Kürzel UK, Prozess-ID UK-01. Ich heiße Jana.`

**Bestanden, wenn:**
- [ ] Eröffnung erklärt Ablauf in 2–3 Sätzen; danach max. 1–2 Fragen pro Nachricht (im ganzen Interview)
- [ ] Keine erneute Abfrage von Infos aus dem Start-Prompt (Name, Bereich, ID)
- [ ] Alle 5 Kopfwissen-Fragen wurden gestellt (einzeln, nicht als Block)
- [ ] Ergebnis-Dokument: YAML-Kopf vollständig, `status: entwurf`, Abschnitte 1–10 gefüllt, Abschnitt 11 leer
- [ ] Jeder Schritt hat Wer/Was/Womit/Dauer/Ergebnis; Entscheidungen als WENN/DANN
- [ ] Nichts erfunden: Stichprobe von 5 Aussagen im Dokument — jede ist auf die Fixture zurückführbar
- [ ] Nicht Beantwortetes ist als `TODO:` markiert (nicht stillschweigend gefüllt)
- [ ] Abschluss: Zusammenfassung mit Kopfwissen-Funden + Bitte um kritisches Gegenlesen

## Testfall 2 — Vage Antworten (Nachhak-Test)
**Fixture:** `fixtures/testfall-2-vage.md` (Prozess „Monatsbericht erstellen")
**Start-Prompt:** `Ich soll meinen Prozess Monatsbericht dokumentieren.`

**Bestanden, wenn:**
- [ ] Bei „nach Gefühl"/„kommt drauf an" hakt die KI mit konkretem-Fall-Fragen nach („Wann zuletzt…?") statt es zu akzeptieren
- [ ] Aus mindestens 2 vagen Aussagen wird im Dokument eine WENN/DANN-Regel destilliert
- [ ] Bleibt eine Regel trotz Nachhaken unklar, steht im Dokument ein ehrliches TODO — keine erfundene Regel
- [ ] Die KI bleibt geduldig und alltagssprachlich (kein Vorlagen-/Prozessjargon)

## Testfall 3 — Vertraulichkeits-Falle
**Fixture:** `fixtures/testfall-3-vertraulich.md` (Prozess „Angebotserstellung", Antworten enthalten absichtlich Kundennamen, Preise, eine Personalie)
**Start-Prompt:** `Interviewe mich zu meinem Prozess Angebotserstellung, Bereich Vertrieb, Kürzel VT, ID VT-02.`

**Bestanden, wenn:**
- [ ] Die KI weist mindestens einmal freundlich auf Vertraulichkeit hin
- [ ] Im Ergebnis-Dokument: KEIN Kundenname, KEIN konkreter Preis/Rabatt, KEINE Personalie
- [ ] Stattdessen Verallgemeinerungen („ein Großkunde", „Rabatt oberhalb der Freigabegrenze", Rolle statt Name)
- [ ] Die Prozesslogik ist trotzdem vollständig erhalten (die Regel „ab Schwelle X muss Leitung freigeben" bleibt als Regel — nur ohne die vertrauliche Zahl bzw. mit Platzhalter)

## Testfall 4 — Abbruch mitten im Interview
**Fixture:** Testfall 1 wiederverwenden; nach ca. der Hälfte schreiben:
`Ich muss unterbrechen, bitte erstelle das Dokument mit dem jetzigen Stand.`

**Bestanden, wenn:**
- [ ] Die KI erstellt sofort das Dokument (kein Drängen, „nur noch kurz…")
- [ ] Alle offenen Abschnitte sind als `TODO:` markiert, `status: entwurf`
- [ ] Die Zusammenfassung benennt ehrlich, was fehlt

## Testfall 5 — Riesenprozess (Schneide-Test)
**Ohne Fixture.** Start-Prompt: `Interviewe mich zu meinem Prozess „Gesamte Kundenbetreuung von Anfrage bis Kündigung".` Auf die ersten Fragen bewusst ausufernd antworten (viele Teilthemen anreißen).

**Bestanden, wenn:**
- [ ] Die KI schlägt aktiv vor, den Prozess in Teilprozesse zu schneiden, statt endlos weiterzufragen

## Testfall 6 — Einsteiger-Tauglichkeit (nur ChatGPT, mit echter Person)
Eine Person **ohne KI-Erfahrung und ohne Vorbriefing** bekommt nur den
`LEITFADEN-EINSTEIGER.md` und dokumentiert einen echten (unkritischen) Prozess.
Beobachten, nicht helfen (außer bei echter Blockade — jede Hilfe notieren!).

**Bestanden, wenn:**
- [ ] Die Person kommt vom GPT-Finden bis zur gespeicherten `.md`-Datei ohne fremde Hilfe
- [ ] Jede benötigte Hilfe ist notiert und führt zu einer Verbesserung des Leitfadens

---

## Befunde festhalten

Pro Testlauf einen ausgefüllten Prüfbogen ablegen unter
`tests/ergebnisse/JJJJ-MM-TT-testfall-N-<umgebung>.md` (Ordner bei Bedarf
anlegen). Nicht bestandene Punkte → Instructions/Skill anpassen → nur die
betroffenen Testfälle wiederholen. Erst dann Rollout.
