---
# ── KI-Prozessmap: das Zielbild-Dokument je Prozess (Ergebnis von Phase 4) ──
map_id: XX-00-MAP
prozess_id: XX-00               # Verweis auf die IST-Dokumentation (prozess-template)
name: <Prozessname>
bereich: <Abteilung/Team>
process_owner: <Rolle>
status: entwurf                 # entwurf | in_pruefung | freigegeben
version: "0.1"
datum: JJJJ-MM-TT
erstellt_von: <Name/Team>
vertraulichkeit: intern         # intern | vertraulich
zielbild:
  automatisiert_oder_ki_gestuetzt: "<z. B. 55–70 %>"   # Anteil operativer Tätigkeiten
  vollautomatisiert: "<z. B. 20–30 %>"                  # ohne manuelle Bearbeitung
  menschliche_entscheidung: "<z. B. 35–50 %>"
  reaktionszeit_vorher_nachher: "<z. B. >4 Std → <60 Min>"
  aufwandsreduktion: "<z. B. bis zu 60 % in Taktung & Verteilung>"
---

# KI-Prozessmap: <Prozessname>

> Zielbild und KI-Einsatzplan für den Prozess <Name>. Grundlage: IST-Dokumentation
> `<prozess_id>` und der Workshop nach `anleitung/ki-potenzial-analyse.md`.

## Steckbrief

| | |
|---|---|
| 👤 **Process Owner** | <Rolle; Vertretungs-/Bereitschaftsregel> |
| 🎯 **Prozessziel** | <Wozu gibt es den Prozess — in 2–3 Sätzen, inkl. dem, was verhindert/erreicht werden soll> |
| 📋 **Scope / Varianten** | <Welche Fallarten/Szenarien deckt der Prozess ab?> |
| ➡️ **Input** | <Signale, Meldungen, Anfragen, Daten, die den Prozess speisen> |
| 📄 **Output** | <Alle Ergebnisartefakte> |
| 👥 **Zielgruppen** | <Wer empfängt/nutzt die Outputs?> |
| 🚚 **Lieferanten** | <Wer liefert zu? (interne Bereiche, Dienstleister, Systeme)> |
| 📊 **KPIs** | <Woran wird der Prozess gemessen?> |

## Gesamt-Zielbild (Zielwerte)

| Kennzahl | Zielwert |
|---|---|
| ⚙️ Operative Tätigkeiten automatisiert oder KI-gestützt | <x–y %> |
| 🤖 Gesamtprozess ohne manuelle Bearbeitung | <x–y %> |
| 👥 Menschliche Entscheidung & Verantwortung | <x–y %> — <bewusst hoch/niedrig, weil …> |
| ⏱️ <Kern-Zeitkennzahl, z. B. Zeit bis erste Reaktion> | <vorher → nachher> |
| 📈 Aufwandsreduktion | <bis zu x % in …> |

## Prozessschritte

<!-- Das Kernstück. Ein Block pro Schritt (üblich: 6–12 Schritte).
Der Ziel-Automatisierungsgrad ist eine Schätzung in %, mit Einordnung
(niedrig / mittel / hoch / sehr hoch). Die vier Listen sind Pflicht —
insbesondere „Menschliche Verantwortung": bewusst benennen, nie leer lassen. -->

### Schritt 1 — <Name> <Emoji>
**Ziel-Automatisierungsgrad:** <x %> (<Einordnung>)

**Was kann automatisiert werden?**
- <regelbasierte Tätigkeiten, Trigger, Routing, Vorlagen, Protokollierung …>

**KI-Einsatz (sinnvolle Anwendungen):**
- <wo KI erkennt, bündelt, entwirft, prüft, vorschlägt …>

**Menschliche Verantwortung:**
- <Entscheidungen, Freigaben, Bewertungen, die bewusst beim Menschen bleiben>

**Erwarteter Nutzen (Haupteffekte):**
- <quantifiziert wo möglich: −x % Zeit, x % dokumentiert, „X statt Y" …>

### Schritt 2 — <Name>
<!-- … gleiche Struktur für alle Schritte … -->

## Ein Prozess — verschiedene Fälle

<!-- 2–4 reale (anonymisierbare) Fälle aus der Praxis, die zeigen, dass derselbe
Prozess unterschiedliche Verläufe trägt. Stärkt Akzeptanz: gelernt wird der
Prozess, nicht das Einzelszenario. -->

| Fall | Typ/Variante | Auslöser & Charakter | Wo der Prozess besonders gefordert ist | Was der Fall gelehrt hat |
|---|---|---|---|---|
| | | | | |

## Automatisierungs-Verteilung im Prozess (Ziel)

| Kategorie | Anteil |
|---|---|
| Automatisiert (ohne menschliche Bearbeitung) | <x–y %> |
| KI-gestützt (Mensch entscheidet) | <x–y %> |
| Menschliche Entscheidung / Verantwortung | <x–y %> |

## Automatisierungs-Reifegrad (Zielbild)

| Stufe | Beschreibung | Status |
|---|---|---|
| 👤 Manuell | <z. B. Zuruf, Wissen in Köpfen, keine Taktung> | <heute/…> |
| ⚙️ Teilautomatisiert | <Templates & Verteiler vorhanden, Erinnerungen manuell> | |
| 🔗 Integriert | <End-to-End-Workflow, eine Statusquelle, SLA & Audit-Trail> | |
| 🤖 Intelligent (Ziel) | <KI erkennt, entwirft, taktet — der Mensch entscheidet> | Ziel |

## Umsetzungs-Roadmap (Empfehlung)

| Phase | Zeitraum | Maßnahmen |
|---|---|---|
| 1 — Quick Wins | 0–3 Monate | <organisatorisch zuerst: Rollen, Vorlagen, Bibliothek, eingeübte Abläufe> |
| 2 — Integrierter Workflow | 3–9 Monate | <Workflows, SLA-Uhren, automatische Verteilung, erste KI-Entwürfe> |
| 3 — Agentischer Prozess | 9–18 Monate | <KI-Agenten, Konsistenzprüfung, Learning Loop> |

## SLA-Empfehlung *(falls der Prozess zeitkritisch ist)*

| Schritt | Zielzeit |
|---|---|
| | |

## Wichtige Risiken & Kontrollen

<!-- Format: ⚠️ <Risiko> — <Kontrolle/Regel, die es verhindert> -->
- ⚠️ <Risiko> — <Kontrolle>
- 🤖 KI-Entwurf ungeprüft — Vier-Augen-Prinzip, jede Aussage bleibt menschlich verantwortet

## Wichtige Prinzipien

- ✓ <Prinzip — kurz und einprägsam>

---
**Wichtig:** Automatisierung beschleunigt und entlastet — die menschliche
Verantwortung bleibt entscheidend für <Fakten, Freigaben, Tonalität, Außenwirkung — je nach Prozess anpassen>.
