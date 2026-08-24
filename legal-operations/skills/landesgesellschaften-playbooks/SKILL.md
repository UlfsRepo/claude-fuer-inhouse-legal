---
name: landesgesellschaften-playbooks
description: Erstellt englischsprachige Self-Service-Playbooks, mit denen lokale Einheiten (Landesgesellschaften, Vertriebsgesellschaften) juristische Standardfälle selbst lösen — plus Reserved-Matters-Katalog mit Entscheidungsbaum und Wesentlichkeitsschwellen für die Abgabe an die Zentrale. IMMER verwenden, wenn der Nutzer dezentrale Einheiten juristisch befähigen, Standardanfragen reduzieren oder eine Reserved-Matters-Logik aufbauen will.
---

# Self-Service-Playbooks für Landesgesellschaften

Befähigt lokale Einheiten, Standardfälle selbst zu lösen — und schafft zugleich Klarheit, welche Angelegenheiten zwingend zur Zentrale müssen. Ergebnis: weniger Routineanfragen im HQ, schnellere Antworten vor Ort, sauberes Governance-Fundament.

## Grundregel

Jedes Playbook beantwortet drei Fragen in dieser Reihenfolge:
1. **Solve:** Was kann die lokale Einheit selbst entscheiden — mit welchen Schritten und Vorlagen?
2. **Check:** Woran erkennt sie, dass der Fall NICHT Standard ist?
3. **Escalate:** Was genau übergibt sie an die Zentrale — in welchem Format, mit welchen Informationen?

Sprache: Englisch (Arbeitssprache dezentraler Einheiten), kurze Sätze, keine Paragraphenketten ohne Erklärung.

## Baustein 1: Themen-Playbooks

Typische Standardthemen (Auswahl an Bedarf anpassen):
- **Warranties & liability** in Kundenverträgen (was ist akzeptabel, was nie)
- **Standard terms / T&Cs** (wann eigene AGB, wann Kundenbedingungen verhandelbar)
- **Litigation intake** (was tun bei Klage/Abmahnung: Fristen sichern, nichts zugestehen, melden)
- **Corporate governance** (Vollmachten, Zeichnungsregeln, Gremienpflichten der lokalen Einheit)
- **Product liability** (Meldewege bei Produktvorfällen, Behördenkontakt)

Struktur je Playbook (2–4 Seiten, mehr nicht):
```
1. Scope           — what this playbook covers / does not cover
2. You can decide  — standard cases, steps, approved templates
3. Red flags       — signs this is NOT a standard case
4. Escalate when   — hard criteria (see Reserved Matters)
5. How to escalate — handover format, required information, response time
```

## Baustein 2: Reserved-Matters-Katalog

Eine Liste der Angelegenheiten, die zwingend der Zentrale vorbehalten sind. Je Eintrag: Gegenstand, Begründung (ein Satz), Wesentlichkeitsschwelle. Typische Kandidaten:
- Streitwerte / Haftungsrisiken oberhalb einer definierten Schwelle
- Vertragsstrafen, unbegrenzte Haftung, IP-Übertragungen
- Behörden- und Gerichtsverfahren ab bestimmter Stufe
- Presse-/Krisenrelevantes
- Verträge außerhalb des Standardgeschäfts (M&A, Immobilien, Finanzierung)

**Wesentlichkeitsschwellen:** immer als konkrete, lokal messbare Kriterien formulieren (Betrag, Laufzeit, Vertragstyp) — nie als „im Zweifel fragen". Die konkreten Beträge sind unternehmensspezifisch und bleiben lokal; im Playbook-Template stehen Platzhalter (`[THRESHOLD]`).

## Baustein 3: Entscheidungsbaum

Erzeuge einen einseitigen Entscheidungsbaum als Abgabe-Kriterium:
```
Anfrage → Ist das Thema in einem Playbook? 
  ja → Red Flag vorhanden? 
    nein → lokal lösen (Playbook folgen)
    ja  → eskalieren (Handover-Format)
  nein → Reserved Matter? 
    ja  → eskalieren
    nein → Kurzanfrage an Zentrale (Antwort wird ggf. neues Playbook-Kapitel)
```
Jede Eskalation, die keinem Playbook zuzuordnen war, ist ein Kandidat für das nächste Playbook — so wächst die Sammlung aus echten Anfragen.

## Workflow bei Erstellung

1. **Anfrage-Analyse:** Sammle die dokumentierten Anfragen der letzten 6–12 Monate aus den lokalen Einheiten; clustere nach Thema und Häufigkeit.
2. **Priorisierung:** Die 3–5 häufigsten Themen zuerst — nicht alle auf einmal.
3. **Abstimmung:** Entwürfe mit den lokalen Ansprechpartnern validieren (verstehen Nicht-Juristen jeden Schritt?).
4. **Ablage:** In der Wissensbibliothek (siehe Skill `wissensbibliothek`), Änderungsstand sichtbar.

## Übergabe
Liefere: Playbook-Template, 1 ausgearbeitetes Beispiel-Playbook zum gewählten Thema, Reserved-Matters-Katalog mit Platzhalter-Schwellen, Entscheidungsbaum. Vor Weitergabe: Skill `vertraulichkeits-gate`.
