# Triage-Logik (Kategorien, Prioritäten, Rückfragen-Bausteine)

> Arbeitsdokument – im Team abstimmen, dann als Wissensdatei in den
> Custom GPT hochladen. Dieses Dokument ist zugleich die fachliche Blaupause für
> das spätere Ticketing-Intake.

## 1. Rechtsgebiete (Kategorienliste)

| Kürzel | Rechtsgebiet | Typische Anfragen | Zuständig (Routing) |
|--------|--------------|-------------------|---------------------|
| VERT | Vertragsrecht | Prüfung, Verhandlung, Kündigung | |
| KD | Gewährleistung / Kundendienst | Kundenforderungen, Kulanz | |
| DS | Datenschutz | Auskunft, Löschung, AVV | |
| IP | Marken / IP | | |
| ARB | Arbeitsrecht | | |
| COMP | Compliance / Exportkontrolle | | |
| GES | Gesellschaftsrecht | | |
| SONST | Sonstiges | | |

## 2. Matter-Schema (genau eine Kategorie je Anfrage)

| Kategorie | Definition | Reaktionszeit (Ziel) |
|-----------|------------|----------------------|
| **Kritisch** | Klage/Behörde/Medien/Personenschaden oder erheblicher drohender Schaden | sofort, gleicher Tag |
| **Frist** | Konkrete Frist erkennbar oder zu vermuten | vor Fristablauf mit Puffer, Frist sofort verifizieren |
| **Neu** | Normale neue Anfrage ohne Frist-/Krisenindikator | innerhalb __ Arbeitstagen |
| **Warten** | Bearbeitung erst möglich, wenn Rückfragen beantwortet / Unterlagen da | Wiedervorlage nach __ Tagen |

## 3. Dringlichkeitslogik

- **Hoch:** Kategorie Kritisch; oder Frist < __ Arbeitstage
- **Mittel:** Frist ≥ __ Arbeitstage; oder Management-Attention erkennbar
- **Niedrig:** keine Frist, Routineanfrage

## 4. Rückfragen-Bausteine je Anfragetyp

> Je Anfragetyp die Standard-Rückfragen, die der GPT in den E-Mail-Entwurf
> übernimmt. Beim Testen ergänzen.

### Vertragsprüfung
1. Aktueller Vertragsentwurf als Datei (Word bevorzugt)
2. Vertragspartner und beteiligte eigene Gesellschaft
3. Gewünschter Unterzeichnungstermin / Deadline
4. Wirtschaftlicher Hintergrund und kritische Punkte aus Sicht des Fachbereichs
5. Vorversionen / bestehende Verträge mit dem Partner

### Kundendienstfall
1. Produkt, Seriennummer, Kaufdatum, Kaufbeleg
2. Reklamations-/Reparaturhistorie
3. Konkrete Forderung des Kunden (inkl. Betrag)
4. Bisherige Korrespondenz
5. Fristen aus Kundenschreiben (Anwalt beteiligt?)

### Datenschutzanfrage
1. Betroffene Person und Art des Begehrens (Auskunft/Löschung/…)
2. Eingangsdatum der Anfrage (Monatsfrist!)
3. Betroffene Systeme/Datenkategorien

### (Weitere Typen ergänzen …)

## 5. Eskalationsindikatoren (→ „🚨 SOFORT ESKALIEREN")

- Klage-/Mahnbescheid zugestellt, anwaltliches Schreiben mit Frist
- Behördenschreiben (Datenschutzbehörde, Marktüberwachung, Zoll, Staatsanwaltschaft)
- Presse-/Medienanfrage
- Personenschaden oder Rückruf-Verdacht
- Verdacht auf Compliance-Verstoß
