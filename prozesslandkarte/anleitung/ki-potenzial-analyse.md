# KI-Potenzial-Analyse (Phase 4)

**Ziel:** Für jeden dokumentierten Prozess entscheiden, wo KI wirkt — und zwar
nicht nur „schneller machen", sondern ausdrücklich auch „anders machen" und
„weglassen". Durchführung: pro Bereich ein Workshop (2–3 h), Prozess für Prozess.
Voraussetzung: Prozessdokument mit `status: freigegeben` oder `in_pruefung`.

**Endprodukt der Phase ist die KI-Prozessmap** nach
`vorlagen/ki-prozessmap-template.md` — je Schritt: Ziel-Automatisierungsgrad,
was automatisierbar ist, sinnvoller KI-Einsatz, menschliche Verantwortung,
erwarteter Nutzen; dazu Gesamt-Zielbild, Reifegrad, Roadmap, ggf. SLAs, Risiken
& Kontrollen und Prinzipien. Wie das fertig aussieht, zeigt das Referenzbeispiel
`beispiele/unternehmenskommunikation/uk-03-map-krisenkommunikation.md`.
Die Schritte 1–3 unten liefern die Inhalte dafür; Schritt 4 überträgt sie in die Map.

## Schritt 1 — Die Neu-Denken-Frage zuerst (Pflicht, vor jedem Detail)

Bevor auf einzelne Schritte geschaut wird, beantwortet das Team für den
**Gesamtprozess** diese vier Fragen und hält die Antworten in Abschnitt 11 fest:

1. **Zweck-Check:** Welches Problem löst das Ergebnis wirklich — und braucht der
   „Kunde" des Prozesses das Ergebnis (noch) in dieser Form? *(Beispiel: Braucht
   die Geschäftsführung den 10-seitigen Monatsbericht — oder eine Antwort auf
   drei Fragen, die eine KI auf Zuruf aus den Daten beantworten könnte?)*
2. **Grüne-Wiese-Frage:** Wie sähe der Prozess aus, wenn wir ihn heute mit KI
   neu erfinden würden — ohne Rücksicht auf „haben wir immer so gemacht"?
3. **Reihenfolge-Frage:** Existieren Schritte nur, weil Information früher knapp
   oder Abstimmung teuer war? (Sammel-Freigaben, Zwischenstände, Statusrunden)
4. **Weglass-Frage:** Welcher Schritt könnte ersatzlos entfallen, wenn ein
   anderer Schritt KI-gestützt besser würde?

Erst danach geht es in die Schritt-Tabelle. Diese Reihenfolge ist bewusst:
Wer zuerst Schritte optimiert, zementiert den alten Prozess.

## Schritt 2 — Jeden Prozessschritt einordnen

Für jeden Schritt aus Abschnitt 5 des Prozessdokuments eine Zeile in der Tabelle
in Abschnitt 11. Einordnung in vier Stufen:

| Stufe | Bedeutung | Typische Kandidaten |
|---|---|---|
| **automatisieren** | KI/Automatisierung erledigt den Schritt, Mensch prüft stichprobenartig oder gar nicht | Zusammenfassen, Übertragen zwischen Systemen, Erstentwürfe nach klaren Regeln, Recherche-Sammlung, Formatieren, Ablage |
| **unterstützen** | KI liefert Entwurf/Analyse/Vorschlag, Mensch entscheidet und verantwortet | Texte mit Außenwirkung, Bewertungen, Priorisierung, Qualitätsprüfung |
| **neu denken** | Der Schritt (oder der ganze Prozess) wird anders geschnitten oder fällt weg | Berichte → Abfragen auf Zuruf; serielle Freigaben → Freigabe-Kriterienkatalog, den KI vorprüft; Statusmeetings → automatischer Lagebericht |
| **Mensch** | Bleibt bewusst beim Menschen | Beziehungen, Verhandlung, finale Verantwortung, Vertrauliches, rechtlich zwingende Entscheidungen |

**Daumenregel für die Einordnung:** Folgt der Schritt **beschreibbaren Regeln**
(auch komplexen)? → mindestens „unterstützen", oft „automatisieren". Beruht er
auf **Urteilsvermögen mit Verantwortung** oder **persönlichem Vertrauen**? → „Mensch"
oder „unterstützen". Wenn niemand die Regel benennen kann, fehlt meist Kopfwissen
in Abschnitt 9 — zurück zu Phase 3, nicht raten.

## Schritt 3 — Bewerten und priorisieren

Pro Idee zwei Einschätzungen (grob reicht: hoch/mittel/niedrig):

- **Nutzen:** gesparte Zeit × Häufigkeit, plus Qualitäts-/Geschwindigkeitsgewinn,
  plus strategischer Wert (z. B. schnellere Reaktion in Krisenfällen).
- **Aufwand:** Wie viel Einführungsarbeit? Sind die nötigen Daten/Vorlagen
  digital vorhanden? Gibt es Freigabe-/Datenschutz-Hürden?

Priorisierung pro Bereich:
1. **Sofort (Pilot):** Nutzen hoch/mittel + Aufwand niedrig → 1–2 Piloten starten.
2. **Planen:** Nutzen hoch + Aufwand hoch → als Projekt einplanen.
3. **Später/Nein:** Nutzen niedrig → dokumentieren und liegen lassen.

## Schritt 4 — In die KI-Prozessmap übertragen und rückkoppeln

- Ergebnisse in eine neue KI-Prozessmap übertragen
  (`vorlagen/ki-prozessmap-template.md`, Dateiname `<kürzel>-<nr>-map-<name>.md`).
  Die Stufen-Tabelle aus Schritt 2 wird dort je Prozessschritt zu den vier Listen
  „Was kann automatisiert werden" / „KI-Einsatz" / „Menschliche Verantwortung" /
  „Erwarteter Nutzen"; die Priorisierung aus Schritt 3 wird zur Roadmap
  (Quick Wins 0–3 Monate → Integrierter Workflow → Agentischer Prozess).
- Kurzfassung zusätzlich in Abschnitt 11 des IST-Prozessdokuments eintragen und
  `ki_potenzial` im YAML-Kopf setzen (hoch/mittel/niedrig).
- Pilot-Prozesse bekommen eine:n Umsetzungsverantwortliche:n und ein Zieldatum.
- **Nach jeder Umsetzung:** Prozessdokument aktualisieren (neuer Ablauf, neue
  Version). Das Dokument beschreibt immer den IST-Zustand — sonst verliert die
  Landkarte ihren Wert als KI-Grundlage.

## Warnhinweise aus der Praxis

- **Nicht den kaputten Prozess automatisieren:** Wenn Abschnitt 10 (Schmerzpunkte)
  lang ist, erst neu denken, dann automatisieren.
- **Qualitätskriterien sind der Hebel:** Ein Schritt ist nur so gut automatisierbar
  wie Abschnitt 7 präzise ist. Vage Kriterien → erst Kriterien schärfen.
- **Mensch-Stufe ist eine Entscheidung, kein Rest:** Bewusst benennen, was beim
  Menschen bleibt und warum — das nimmt Ängste und schafft Klarheit.
