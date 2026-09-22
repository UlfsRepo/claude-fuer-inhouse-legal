# Prompt: KI-Prozessmap aus einer IST-Dokumentation erstellen (Phase 4)

Für die Map-Erstellung braucht es keinen eigenen Custom GPT — ein normaler
ChatGPT-Chat genügt. **Drei Dateien anhängen:**
1. `anleitung/ki-potenzial-analyse.md`
2. `vorlagen/ki-prozessmap-template.md`
3. Die IST-Prozessdokumentation (das Ergebnis aus dem Interview, `status:
   freigegeben` oder `in_pruefung`)

Optional als vierte Datei die Stilreferenz
`beispiele/unternehmenskommunikation/uk-03-map-krisenkommunikation.md`.

## Prompt zum Kopieren

> Erstelle aus der angehängten IST-Prozessdokumentation eine KI-Prozessmap.
> Arbeite streng nach der angehängten Anleitung (ki-potenzial-analyse.md) und
> fülle die angehängte Vorlage (ki-prozessmap-template.md) vollständig aus:
>
> 1. Beantworte ZUERST die vier Neu-Denken-Fragen für den Gesamtprozess —
>    substanziell, mindestens eine Idee, die den Prozess verändert oder
>    Schritte streicht, nicht nur beschleunigt.
> 2. Ordne DANN jeden Schritt der IST-Doku ein (automatisieren / unterstützen /
>    neu denken / Mensch) und baue daraus je Schritt den Map-Block:
>    Ziel-Automatisierungsgrad in % plus die vier Listen. "Menschliche
>    Verantwortung" darf nie leer sein.
> 3. Leite die Roadmap aus der Priorisierung ab — Quick Wins (0–3 Monate)
>    zuerst organisatorisch, nicht "KI-Agent ab Tag 1".
>
> Regeln: Erfinde keine Prozessfakten — alles Prozessuale muss aus der
> IST-Doku stammen; offene TODOs der IST-Doku bleiben offen und werden als
> "(offen in IST-Doku)" markiert. Deine KI-Potenzial-Einschätzungen und
> Zielwerte begründest du aus der IST-Doku, besonders aus den Schmerzpunkten
> (Abschnitt 10) — diese müssen in den Ideen oder der Roadmap wieder
> auftauchen. Zahlen konsistent halten (Verteilung ≈ 100 %). Gib die fertige
> Map als einen Markdown-Codeblock aus.

## Danach

- Ausgabe kopieren und als `<kürzel>-<nr>-map-<prozessname>.md` neben der
  IST-Doku ablegen, `status: entwurf`.
- **Wichtig:** Die KI-generierte Map ist der ENTWURF für den Phase-4-Workshop,
  nicht sein Ersatz. Das Team validiert im Workshop jede Einordnung — vor
  allem die Spalte "Menschliche Verantwortung" ist eine bewusste Team-
  Entscheidung. Erst danach: `status: freigegeben`.
- Qualitätscheck: Testfall 7 im `tests/testplan.md` enthält die Prüfpunkte.
