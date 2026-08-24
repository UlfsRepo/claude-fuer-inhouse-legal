---
name: zielstand-review
description: Wöchentlicher oder monatlicher Fortschritts-Check gegen Jahresziele mit Stufenlogik (100 % / Übererfüllung) — Ampelstatus je Ziel, Lückenanalyse, Priorisierung der nächsten Woche. IMMER verwenden, wenn der Nutzer seinen Zielstand prüfen, Prioritäten gegen Ziele setzen oder einen Ziel-Review vorbereiten will.
---

# Zielstand-Review

Hält Jahresziele im Wochentakt auf Kurs. Kern-Idee: Ziele scheitern selten an Können, sondern an Sichtbarkeit — dieser Review macht jede Woche sichtbar, was auf welches Ziel einzahlt und wo die Lücke ist.

## Voraussetzung: lokale Zielstand-Datei

Der Skill arbeitet mit einer **lokalen Datei des Nutzers** (nicht im Repo, nicht in der Cloud eines Dritten), z. B. `zielstand.md`. Existiert sie nicht, lege sie im Interview an. Struktur je Ziel:

```markdown
## Ziel <N>: <Kurztitel>
- **Messlatte 100 %:** <was muss fertig sein — als abhakbare Ergebnisse>
- **Übererfüllung (150/200 %):** <Zusatzergebnisse>
- **Frist:** <Datum>
- **Erledigt:** <Liste mit Datum>
- **Offen:** <Liste, priorisiert>
- **Blockiert durch:** <Abhängigkeiten, z. B. IT-Mitwirkung>
```

Vertrauliche Details (Beträge, Namen, interne Bezeichnungen) gehören nur in diese lokale Datei — nie in Prompts an fremde Systeme ohne Prüfung (Skill `vertraulichkeits-gate`).

## Workflow

### Schritt 1: Stand erfassen
Lies die Zielstand-Datei. Erfrage, was seit dem letzten Review erledigt wurde, und trage es mit Datum ein.

### Schritt 2: Ampel je Ziel
Bewerte jedes Ziel nach Restzeit und Restaufwand:
- 🟢 **Auf Kurs:** Restaufwand passt bequem in die Restzeit
- 🟡 **Angespannt:** passt nur, wenn ab jetzt kontinuierlich geliefert wird
- 🔴 **Gefährdet:** braucht Kurswechsel (Umpriorisierung, Hilfe, Zuschnitt-Gespräch)

Begründe jede Ampel in einem Satz mit dem konkreten Engpass.

### Schritt 3: Lückenanalyse
Je Ziel: Was fehlt bis 100 %? Erst wenn 100 % gesichert ist: Was fehlt bis zur Übererfüllungsstufe? **Regel: Kein Übererfüllungs-Aufwand, solange ein anderes Ziel rot ist.**

### Schritt 4: Wochenprioritäten
Leite maximal 3 Prioritäten für die kommende Woche ab. Kriterien in dieser Reihenfolge:
1. Entblockt es ein rotes/gelbes Ziel?
2. Hat es eine externe Abhängigkeit mit Vorlauf (früh anstoßen)?
3. Schließt es ein Ziel komplett ab? (Fertige Ziele schlagen viele halbfertige.)

### Schritt 5: Protokoll
Aktualisiere die Zielstand-Datei und gib einen kompakten Review aus:

```
# Zielstand-Review <Datum> — Restzeit: <N> Wochen
| Ziel | Ampel | Erledigt diese Woche | Nächster Meilenstein |
|---|---|---|---|
**Top-3 nächste Woche:** 1. … 2. … 3. …
**Risiken/Abhängigkeiten:** …
```

## Rhythmus
Wöchentlich (empfohlen: Montag, 15 Minuten) — monatlich zusätzlich ein Blick auf die Gesamtlaufzeit: Reicht das Tempo rechnerisch noch für alle Ziele? Wenn nein: Welches Ziel wird aktiv depriorisiert statt still zu scheitern?
