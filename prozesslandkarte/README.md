# Prozesslandkarte — Grundlage für die Arbeit mit KI

Dieses Repository dokumentiert alle Arbeitsprozesse des Teams in einem Format, das
**Menschen lesen und pflegen** können und das **KI direkt verarbeiten** kann
(Markdown mit strukturiertem YAML-Kopf, ergänzt durch ein JSON-Schema).

## Warum wir das tun

1. **Transparenz:** Wissen, das bisher nur in Köpfen steckt, wird sichtbar und übergabefähig.
2. **KI-Grundlage:** Ein dokumentierter Prozess kann von KI gelesen, unterstützt und
   später als Skill/Agent abgebildet werden. Ein undokumentierter nicht.
3. **Neu denken statt nur beschleunigen:** Erst wenn ein Prozess schwarz auf weiß
   dasteht, sehen wir, welche Schritte KI übernehmen kann — und welche Schritte
   es überhaupt nicht mehr braucht.

## Ordnerstruktur

```
prozesslandkarte/
├── README.md                  ← dieses Dokument (Methode & Spielregeln)
├── LEITFADEN-EINSTEIGER.md    ← Schritt-für-Schritt für KI-Einsteiger:innen
├── vorlagen/
│   ├── prozess-template.md        ← IST-Dokumentation EINES Prozesses (Phase 2–3)
│   ├── ki-prozessmap-template.md  ← KI-Prozessmap: Zielbild je Prozess (Phase 4)
│   ├── landkarte-template.md      ← Prozessübersicht eines Bereichs (Phase 1)
│   └── prozess-schema.json        ← Maschinenlesbares Schema (Validierung, KI)
├── anleitung/
│   ├── mitarbeiter-leitfaden.md   ← So dokumentierst du deine Prozesse
│   └── ki-potenzial-analyse.md    ← So entsteht aus der IST-Doku die KI-Prozessmap
├── skills/
│   └── prozess-interview/         ← Claude-Skill: führt das Doku-Interview (Phase 2)
├── chatgpt/
│   ├── einrichtung-custom-gpt.md  ← Interview-Skill als Custom GPT (ChatGPT Enterprise)
│   ├── gpt-instructions-prozess-interview.md ← Instructions zum Einfügen
│   └── prompt-ki-prozessmap.md    ← Phase 4: Map-Erstellung per Prompt (kein eigener GPT nötig)
├── tests/
│   ├── testplan.md                ← 6 Testfälle vor dem Go-Live
│   ├── pruefbogen.md              ← Bewertungsbogen je Testlauf
│   └── fixtures/                  ← Drehbücher für die Testfälle
├── starter-pakete/
│   └── legal/                     ← Starter für Rechtsabteilungen: vorbefüllte
│                                    Landkarte + verschärfte Vertraulichkeitsregeln
├── beispiele/
│   └── unternehmenskommunikation/
│       ├── uk-03-krisenkommunikation.md      ← Beispiel IST-Dokumentation
│       └── uk-03-map-krisenkommunikation.md  ← Beispiel KI-Prozessmap
└── prozesse/
    └── <bereich>/                 ← hier entstehen die echten Prozessdokumente
        ├── landkarte.md
        ├── <bereich>-01-<prozessname>.md
        └── <bereich>-01-map-<prozessname>.md
```

**Hinweis Vertraulichkeit:** Dieses Repository ist bewusst generisch — echte
Prozessdokumente, unternehmensspezifische Beispiele und Testergebnisse bleiben
in der internen Ablage (per `.gitignore` ausgeschlossen).

**Zwei KI-Umgebungen:** Der Interview-Skill existiert in zwei Varianten mit
identischer Logik — als Claude-Code-Skill (`skills/prozess-interview/`, kann
Dateien direkt speichern) und als Custom GPT für ChatGPT Enterprise
(`chatgpt/`, Ergebnis wird kopiert und manuell abgelegt). Für Einsteiger:innen:
`LEITFADEN-EINSTEIGER.md`. Vor dem Rollout: `tests/testplan.md` durchlaufen.

**Drei Dokumenttypen, drei Flughöhen:**
1. **Landkarte** (je Bereich): Inventar aller Prozesse — eine Zeile pro Prozess.
2. **Prozessdokumentation** (je Prozess): der IST-Zustand, so wie er heute läuft —
   inklusive Kopfwissen. Das Rohmaterial.
3. **KI-Prozessmap** (je Prozess): das Zielbild — je Schritt Automatisierungsgrad,
   KI-Einsatz, menschliche Verantwortung und Nutzen, plus Roadmap, SLAs, Risiken
   und Prinzipien. So sieht das Endprodukt aus (Beispiel:
   `beispiele/unternehmenskommunikation/uk-03-map-krisenkommunikation.md`).

## Der Weg dorthin — 5 Phasen

### Phase 1 — Inventur (pro Bereich, ein 90-Minuten-Workshop)
Jeder Bereich erstellt seine **Landkarte** (`vorlagen/landkarte-template.md`):
eine Liste aller Prozesse mit einer Zeile pro Prozess — Name, Auslöser, Ergebnis,
Häufigkeit, Verantwortliche:r. Noch keine Details. Ziel: Vollständigkeit.
Faustregel: Was mindestens einmal im Quartal vorkommt oder kritisch ist, steht drauf.
Für manche Bereiche gibt es vorbefüllte Starter-Landkarten unter
`starter-pakete/` (z. B. Rechtsabteilung) — dann heißt der Workshop
„streichen, umbenennen, ergänzen" statt „bei null anfangen".

### Phase 2 — Dokumentation (jede:r Mitarbeiter:in, 2–3 Prozesse pro Woche)
Jede:r dokumentiert die **eigenen** Prozesse mit `vorlagen/prozess-template.md`.
Zwei Wege:
- **Selbst schreiben** entlang der Vorlage, oder
- **KI-Interview (empfohlen):** Der Skill `skills/prozess-interview/` führt das
  komplette Interview — Auslöser genügt: „Interviewe mich zu meinem Prozess X".
  Claude fragt in kleinen Schritten, hebt gezielt Kopfwissen und speichert das
  fertige Dokument unter `prozesse/<bereich>/`. Installation: Ordner
  `skills/prozess-interview/` nach `.claude/skills/` des Arbeitsverzeichnisses
  (oder `~/.claude/skills/`) kopieren.
  Anleitung: `anleitung/mitarbeiter-leitfaden.md`, Abschnitt „KI-Interview".

### Phase 3 — Peer-Review & Kopfwissen heben
Ein:e Kolleg:in (idealerweise die Vertretung) liest jedes Dokument und stellt die
Frage: **„Könnte ich diesen Prozess morgen allein ausführen?"** Alles, was fehlt,
kommt in Abschnitt 9 (Kopfwissen). Erst dann wird `status: freigegeben` gesetzt.

### Phase 4 — KI-Potenzial-Analyse → KI-Prozessmap (gemeinsam, pro Bereich)
Mit `anleitung/ki-potenzial-analyse.md` wird jeder Prozess bewertet — ausdrücklich
in drei Stufen: **automatisieren, unterstützen, neu denken.** Die dritte Stufe ist
Pflicht, nicht Kür: Für jeden Prozess wird einmal die Frage beantwortet
„Wie sähe dieser Prozess aus, wenn wir ihn heute mit KI neu erfinden würden?"
**Ergebnis der Phase ist die KI-Prozessmap** (`vorlagen/ki-prozessmap-template.md`):
je Schritt Ziel-Automatisierungsgrad, was automatisierbar ist, wo KI sinnvoll
unterstützt, was bewusst menschliche Verantwortung bleibt und welcher Nutzen
erwartet wird — plus Zielbild, Reifegrad, Umsetzungs-Roadmap und Risiken.
Referenzbeispiel: `beispiele/unternehmenskommunikation/uk-03-map-krisenkommunikation.md`.

### Phase 5 — Pilotieren & pflegen
- Pro Bereich starten die 1–2 Prozesse mit dem besten Verhältnis aus Nutzen und Aufwand.
- **Lebende Dokumente:** Jede Prozessänderung und jede eingeführte KI-Lösung wird
  im Dokument nachgezogen (`version` und `letzte_aktualisierung` im YAML-Kopf).
- Quartals-Review pro Bereich: Stimmt die Landkarte noch? Was ist neu, was ist weg?

## Spielregeln

- **Ehrlichkeit vor Schönheit:** Dokumentiert wird der Prozess, wie er *wirklich*
  läuft — inklusive Workarounds und Schmerzpunkten. Nicht das Soll-Organigramm.
- **Rollen statt Namen** in den Prozessschritten (Namen nur im YAML-Kopf als Kontakt).
- **Keine vertraulichen Inhalte** (Kundendaten, Konditionen, Personalia) — der
  Prozess wird beschrieben, nicht der Einzelfall.
- **Lieber unvollständig als gar nicht:** Ein Entwurf mit Lücken (`status: entwurf`)
  ist wertvoller als ein perfektes Dokument, das nie fertig wird.
- Ein Prozess = eine Datei. Dateiname: `<bereichskürzel>-<nr>-<prozessname>.md`
  (z. B. `uk-03-krisenkommunikation.md`).

## Was danach kommt

Jedes freigegebene Prozessdokument ist die direkte Vorlage für einen KI-Skill oder
Agenten: Die Abschnitte Auslöser, Ablauf, Regeln und Qualitätskriterien sind genau
das, was ein Skill braucht. Die Landkarte wird damit zum Bauplan der KI-Einführung.
