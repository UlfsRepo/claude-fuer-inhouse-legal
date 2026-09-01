# Use Case 1: Vertragsprüfung gegen Legal Playbook

## Ziel

Die KI erhält einen Vertrag und ein definiertes Prüfraster (Legal Playbook). Sie
identifiziert systematisch die relevanten Klauseln, markiert kritische oder
ungewöhnliche Regelungen, zeigt Abweichungen von den gewünschten Positionen auf und
erstellt eine priorisierte Liste der Punkte für die anschließende juristische
Vertiefung.

**Wichtig (aus dem Use-Case-Steckbrief):** Der GPT ersetzt nicht die juristische
Prüfung, sondern liefert einen möglichst guten, strukturierten **First Review**.

## Status quo (Pain Point)

Wiederkehrende manuelle Prüfung ähnlicher Klauseln in Verträgen; Standards müssen
immer wieder abgeglichen werden.

## Mehrwert

1. Schnellere Erstprüfung
2. Konsistentere Prüfung und Fokus der juristischen Arbeitszeit auf tatsächlich
   kritische Punkte

## Umsetzung mit ChatGPT Enterprise

1. **Playbook erstellen:** [playbook-vorlage.md](playbook-vorlage.md) mit den
   Eigene Standardpositionen je Klauseltyp füllen (Muss/Soll/No-Go + Fallback).
   Pro Vertragstyp (NDA, Einkauf, SaaS …) eine Datei oder ein Kapitel.
2. **Custom GPT anlegen:** ChatGPT Enterprise → GPT erstellen →
   [system-prompt.md](system-prompt.md) als Instructions einfügen.
3. **Wissensbasis hochladen:** das/die Playbook(s) als Knowledge-Dateien anhängen.
4. **Testen:** 1–2 anonymisierte Echt-Verträge hochladen, Ergebnis gegen manuelle
   Prüfung vergleichen → [test-protokoll.md](test-protokoll.md).

## Prozess (Soll)

Upload Vertrag → KI-First-Review anhand Prüfraster → kritische Klauseln / fehlende
Regelungen identifizieren → priorisierte Ergebnisübersicht → ggf. Verhandlungs-/
Formulierungsvorschläge → juristische Prüfung durch das Team → weitere
Vertragsbearbeitung.

## Ausbaustufen

- Playbooks je Vertragstyp getrennt pflegen und versionieren (in diesem Repo).
- Abweichungs-Log führen: welche Playbook-Positionen werden in der Praxis häufig
  überschritten? → Input für Playbook-Updates.
- Export des Ergebnisberichts als Word-Dokument (Code Interpreter im GPT aktivieren).
