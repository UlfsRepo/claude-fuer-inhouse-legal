# Claude für Inhouse-Legal

Installierbare Claude-Code-Plugins für Rechtsabteilungen international tätiger Unternehmen: Skills für Legal Operations, Quality-Gates und Testakten — gebaut nach dem Muster erprobter Fach-Skill-Sammlungen (Methodik im Repo, vertrauliche Daten bleiben lokal, Mensch entscheidet).

> ⚠️ **Experimentell. Keine Rechtsberatung.** Die Skills unterstützen Legal-Professionals bei Struktur-, Dokumentations- und Organisationsarbeit — sie ersetzen weder juristische Prüfung noch unternehmensinterne Freigaben. Alle Inhalte sind generisch; unternehmensspezifische oder vertrauliche Daten gehören **niemals** in dieses Repository.

## Das Vertraulichkeitsprinzip

Dieses Repo enthält ausschließlich **Methodik**: wie man eine Wissensbibliothek strukturiert, eine Matterliste führt, ein Playbook aufbaut. Die **konkreten Daten** — echte Mandate, Ziele, Namen, Zahlen, Schwellenwerte — leben ausschließlich lokal beim Nutzer (z. B. im eigenen M365) und werden den Skills erst zur Laufzeit gegeben. Zum gefahrlosen Ausprobieren liegt jedem Modul eine **fiktive Testakte** bei.

## Installation

**Als Claude-Code-Plugin:**

```
/plugin marketplace add UlfsRepo/claude-fuer-inhouse-legal
/plugin install legal-operations@claude-fuer-inhouse-legal
```

**Modellunabhängig (ChatGPT & Co.):** Jede `SKILL.md` ist ein eigenständiger, vollständiger Arbeits-Prompt. Datei öffnen, Inhalt (ohne den Frontmatter-Block zwischen den `---`-Zeilen) in ein beliebiges LLM kopieren, eigene Angaben ergänzen — fertig. Kompakte Einstiege: [Schnellstart-Prompts](legal-operations/legal-operations-schnellstart.md).

## Module

| Plugin | Status | Inhalt |
|---|---|---|
| **[legal-operations](legal-operations/)** | ✅ v0.2.0 | Wissensbibliothek-Architekt, Matter-Intake-System, M&A-Playbook-Baukasten, Self-Service-Playbooks für Landesgesellschaften, Delegation-of-Authority-Baukasten, Zielstand-Review, Governance-Format, Vertraulichkeits-Gate, Testakte |
| vertragsarbeit | 🔜 geplant | Playbook-gestützte Vertragsprüfung, Klausel-Bibliothek, Eskalationsmarker |
| compliance-und-datenschutz | 🔜 geplant | DSGVO-Arbeitsabläufe, Schulungsunterlagen, Audit-Vorbereitung |
| legal-reporting | 🔜 geplant | Management-Reports, KPI-Definitionen, Quartalsberichte |

## Bauprinzip aller Module

1. **Methodik öffentlich, Daten lokal** — Skills beschreiben das Wie; das Was (Mandate, Ziele, Zahlen) bleibt beim Nutzer
2. **Produktions-Skills** — strukturierte Arbeitsschritte mit klaren Zwischenergebnissen; nichts erfinden, Unbelegtes markieren
3. **Verpflichtendes Vertraulichkeits-Gate** — vor jedem Artefakt, das die eigene Maschine verlässt, wird auf vertrauliche Inhalte geprüft
4. **Mensch entscheidet** — kein Skill versendet, veröffentlicht oder committet etwas ohne menschliches Go
5. **Testakte je Modul** — ein fiktives Unternehmen zum gefahrlosen Ausprobieren

## Lizenz & Mitwirken

MIT-Lizenz (siehe [LICENSE](LICENSE)). Feedback und Praxiserfahrungen aus Rechtsabteilungen sind willkommen (Issues).
