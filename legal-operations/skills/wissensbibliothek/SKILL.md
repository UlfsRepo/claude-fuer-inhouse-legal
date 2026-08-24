---
name: wissensbibliothek
description: Entwirft die zentrale Wissens- und Mandatsbibliothek einer Rechtsabteilung — Ordnerstruktur, Namenskonvention, Ablageregeln, Migrationsplan und Governance-1-Pager, umsetzbar mit M365-Bordmitteln. IMMER verwenden, wenn der Nutzer ein Dokumentenmanagement, eine Wissensbibliothek, Ablagestruktur oder Namenskonvention für Legal aufbauen oder verbessern will.
---

# Wissensbibliothek-Architekt

Baut das Fundament eines Legal-DMS: eine Struktur, die jeder im Team ohne Schulung versteht, mit einer Ein-Ort-Regel, die Duplikate und Schatten-Ablagen beendet. Maßstab: Ein neues Teammitglied findet jedes Dokument in unter einer Minute.

## Grundsätze

- **Ein-Ort-Regel:** Jedes Dokument hat genau einen verbindlichen Speicherort. E-Mail-Anhänge, lokale Kopien und Chat-Uploads sind Arbeitskopien, nie die Quelle.
- **Flach schlagen tief:** Maximal 3 Ordnerebenen. Was tiefer will, braucht stattdessen eine bessere Namenskonvention.
- **Konvention schlägt Disziplin:** Regeln müssen so einfach sein, dass sie nebenbei eingehalten werden — maximal 10 Ablageregeln, eine Seite.
- **Bordmittel zuerst:** Alles muss mit vorhandenen M365-Mitteln (SharePoint/Teams/OneDrive) funktionieren — ohne Tool-Beschaffung, Budget oder externe Freigaben.

## Workflow

### Schritt 1: Bestandsaufnahme (Interview)
Erfrage, falls nicht angegeben:
- Welche Dokumenttypen fallen an? (Verträge, Gutachten, Schriftsätze, Vorlagen, Gremienunterlagen, Korrespondenz …)
- Wo liegt heute was? (Laufwerke, Postfächer, Teams-Kanäle, lokale Ordner)
- Wer greift zu — nur Legal oder auch Fachbereiche? Gibt es Vertraulichkeitsstufen?
- Welche 10 Vorlagen werden am häufigsten gebraucht?

### Schritt 2: Strukturentwurf
Schlage eine Struktur mit zwei getrennten Wurzeln vor und begründe jede Abweichung:

```
📁 Wissensbibliothek        (themen-orientiert, langlebig)
   ├── Vorlagen/            (nach Dokumenttyp)
   ├── Playbooks/           (Prüf- und Verhandlungsleitfäden)
   ├── Wissen/              (Merkblätter, Rechtsprechungsnotizen, FAQ)
   └── Governance/          (Regeln der Bibliothek selbst)
📁 Mandatsbibliothek        (vorgangs-orientiert, abschließbar)
   └── <Jahr>/<Matter-ID Kurztitel>/
```

### Schritt 3: Namenskonvention
Standard-Muster, an Nutzerbedarf anpassen:
`JJJJ-MM-TT_Dokumenttyp_Gegenstand_vNN` — z. B. `2026-03-14_NDA_Lieferant-Beispiel_v02`.
Regeln: keine Leerzeichen-Kreativität, keine Umlaute in Dateinamen wenn Systeme Probleme machen, `vNN` statt „final_final", Entwürfe tragen `ENTWURF` im Namen.

### Schritt 4: Ablageregeln (max. 10)
Formuliere höchstens 10 Regeln als Imperativsätze auf eine Seite. Muster:
1. Jedes Dokument liegt an genau einem Ort (Ein-Ort-Regel).
2. Mandatsdokumente in die Mandats-, Wissen in die Wissensbibliothek.
3. Dateiname nach Konvention — sonst gilt das Dokument als nicht abgelegt.
4. Neue Version = neue `vNN`, alte Version bleibt liegen.
5. Abgeschlossene Mandate werden binnen 4 Wochen archiviert.
(… an Kontext anpassen, nie mehr als 10.)

### Schritt 5: Migrationsplan Top-Vorlagen
Erzeuge eine Checkliste: die 10 wichtigsten Vorlagen identifizieren → bereinigen (aktuelle Fassung bestimmen, Altversionen markieren) → nach Konvention umbenennen → in `Vorlagen/` einstellen → alte Fundorte mit Verweis versehen.

### Schritt 6: Governance-1-Pager
Erzeuge einen One-Pager für das Nutzer-Briefing: Zweck der Bibliothek (3 Sätze), die Struktur als Bild/Baum, die 10 Ablageregeln, Ansprechperson, Startdatum. Eine Seite, keine zweite.

## Ausbaustufen (optional)
- **Playbook-Bereich:** je häufigem Vertragstyp ein Prüf-Playbook in `Playbooks/` (siehe Skill `ma-playbook` als Strukturvorbild).
- **Geschützter Bereich:** separater Bereich mit eigener Berechtigungsgruppe für besonders vertrauliche Dokumente — Zugriffsliste dokumentieren, IT einbinden.

## Übergabe
Liefere am Ende: Strukturbaum, Namenskonvention, Ablageregeln-Seite, Migrations-Checkliste, Governance-1-Pager — jeweils als eigenes, kopierfähiges Artefakt. Vor Weitergabe an Dritte: Skill `vertraulichkeits-gate` durchlaufen.
