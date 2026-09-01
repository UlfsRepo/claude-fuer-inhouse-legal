# KI-Use-Cases für Inhouse-Legal-Teams

Fünf praxiserprobte KI-Use-Cases für Rechtsabteilungen — entstanden aus einem
realen Hackathon eines Inhouse-Legal-Teams, hier vollständig anonymisiert und
generisch aufbereitet. Jeder Use Case hat einen eigenen Ordner mit
Umsetzungsleitfaden, fertigem System-Prompt und Vorlagen für die Wissensbasis.

Das Tool-Setup (ChatGPT Enterprise, M365/Outlook Copilot ohne Copilot Studio,
GitHub Copilot) entspricht dem, was viele Unternehmen heute freigegeben haben —
die Prompts funktionieren aber in jedem LLM mit Datei-Upload und
Wissensbasis-Funktion (siehe [Vertraulichkeitsprinzip](../README.md) des Repos).

## Die 5 Use Cases

| # | Use Case | Primäres Tool | Workshop-Ziel |
|---|----------|---------------|----------------------|
| 1 | [Vertragsprüfung gegen Legal Playbook](01-vertragspruefung-legal-playbook/) | ChatGPT Enterprise (Custom GPT + Wissensbasis) | Playbook-Struktur + Prompt bauen, mit 1–2 Verträgen testen |
| 2 | [Kundendienst GPT](02-kundendienst-gpt/) | ChatGPT Enterprise (Custom GPT + FAQ-Wissensbasis) | Wissensbasis-Struktur definieren, Prompt bauen |
| 3 | [Legal-Triage-Assistent](03-legal-triage-assistent/) | ChatGPT Enterprise (Custom GPT) | Kategorien-/Prioritätslogik + Prompt, Test mit 5–10 anonymisierten Anfragen |
| 4 | [Filing Assistant](04-filing-assistant/) | ChatGPT Enterprise + Outlook Copilot (Pilot manuell) | Taxonomie, Metadaten-Set, Klassifikations-Prompt, Trefferquote messen |
| 5 | [Legal Invoice Checker](05-legal-invoice-checker/) | ChatGPT Enterprise (Custom GPT + Billing Guidelines) | Guidelines strukturieren, Prompt bauen, Test mit 2–3 anonymisierten Rechnungen |

## Verfügbare Tools und ihre Rolle

- **ChatGPT Enterprise** – Arbeitspferd für alle 5 Use Cases. Custom GPTs mit
  Instructions (System-Prompt) und hochgeladenen Wissensdateien (Playbook, Guidelines,
  FAQ, Taxonomie). Kein Copilot Studio nötig.
- **Microsoft Outlook 365 Copilot** – unterstützend: E-Mail-Entwürfe aus
  Triage-/Kürzungs-Ergebnissen, Zusammenfassen langer Mail-Threads als Input für die
  GPTs, Pilotbetrieb der Ablage-Mailbox (Use Case 4).
- **GitHub Copilot** – für die Ausbaustufen: Skripte für Automatisierung
  (z. B. Power-Automate-Alternativen, Auswertungsskripte für Testprotokolle,
  LEDES-Parser für Rechnungen).

## Empfohlener Workshop-Ablauf

1. **Team aufteilen** – 2er-Teams je Use Case; Use Cases 1 und 5 sind am weitesten
   spezifiziert und liefern am schnellsten vorzeigbare Ergebnisse.
2. **Wissensbasis zuerst** – jeder GPT ist nur so gut wie Playbook/Guidelines/Taxonomie.
   Die Vorlagen in den Ordnern zuerst mit echtem (anonymisiertem) Inhalt füllen.
3. **Custom GPT anlegen** – ChatGPT Enterprise → „GPT erstellen" → System-Prompt aus
   `system-prompt.md` einfügen → Wissensdateien hochladen → Websuche/Code-Interpreter
   nach Bedarf aktivieren.
4. **Testen und protokollieren** – Testprotokoll im jeweiligen Ordner nutzen;
   Trefferquote und Fehlklassifikationen dokumentieren.
5. **Learnings festhalten** – direkt in den README des Use Case; bei Use Case 3
   zusätzlich als Anforderungsliste für das Ticketing-Intake.

## Datenschutz und Compliance (gilt für alle Use Cases)

- **Nur anonymisierte Dokumente** in Tests verwenden (Namen, Beträge ggf.
  verfremden), bis IT & Data Privacy die Verarbeitung freigegeben haben.
- **Mit Kopien arbeiten, keine Originale verschieben** (insbesondere Use Case 4).
- Die GPTs liefern einen **First Review / Entwurf** – die juristische Prüfung und
  Entscheidung bleibt immer beim Team. Diesen Hinweis enthält jeder System-Prompt.
- DSGVO: Berechtigungskonzept und Aufbewahrungsfristen vor Regelbetrieb mit IT &
  Data Privacy klären.

## Repo-Konventionen

- Sprache: Deutsch (Prompts und Doku), da die Arbeitsdokumente deutsch sind.
- `system-prompt.md` = 1:1 kopierbar in die GPT-Instructions.
- Vorlagen (`*-template.md` / `*-vorlage.md`) = Struktur für die Wissensdateien;
  echte Inhalte bleiben intern und werden **nicht** in dieses Repo committet, wenn
  sie vertraulich sind.
