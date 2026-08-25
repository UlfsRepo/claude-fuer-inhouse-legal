---
name: delegation-of-authority
description: Baut eine Delegation-of-Authority-Regelung (DoA) für ein Unternehmen oder eine Unternehmensgruppe — Bestandsaufnahme, DoA-Matrix mit Freigabeschwellen, Unterschriften-/Signature-Policy und Maßnahmenplan als Antwort auf Audit-Findings. IMMER verwenden, wenn der Nutzer Zeichnungsbefugnisse, Freigabeschwellen, eine Unterschriftenrichtlinie, ein DoA-Konzept oder ein Audit-Finding zu Vollmachten und Approvals bearbeitet.
---

# Delegation of Authority (DoA)

Regelt, wer im Unternehmen was entscheiden und unterschreiben darf — nach außen und nach innen. Typischer Auslöser ist ein Audit-Finding nach dem Muster: „Es existiert keine Signature Policy über alle Kerngeschäftsprozesse; Freigabeschwellen und verbindliche Autorisierungsregeln fehlen; ein Regelungsentwurf liegt seit langem unfreigegeben vor." Ergebnis dieses Skills: eine formal freigegebene, veröffentlichte Regelung statt eines ewigen Entwurfs.

## Grundprinzipien

1. **Externe Vertretung ≠ interne Freigabe.** Die wichtigste Trennung der gesamten Regelung:
   - **Externe Vertretung:** rechtsverbindliche Erklärungen gegenüber Dritten — Vertragsabschlüsse, Kündigungen, sonstige Willenserklärungen. Rechtsgrundlage sind Organstellung, Prokura, Handlungs- und Einzelvollmachten. Ein Verstoß berührt die Wirksamkeit nach außen.
   - **Interne Freigabebefugnisse:** Freigaben mit finanzieller oder organisatorischer Wirkung — Investitionen, Personalmaßnahmen, Budgetentscheidungen. Sie wirken nur im Innenverhältnis; ein Verstoß macht das Geschäft nicht unwirksam, hat aber arbeitsrechtliche und Compliance-Folgen.
   Beide Ebenen gehören in eine Regelung, aber in getrennte Abschnitte — wer sie vermischt, produziert Widersprüche zwischen Handelsregister und Freigabematrix.
2. **Vertretung ist gesellschaftsbezogen.** Jeder Rechtsträger wird nach seinem eigenen Statut vertreten. Führungskräfte anderer Konzerngesellschaften — auch übergeordneter regionaler Einheiten — können eine Gesellschaft ohne eigene Organstellung oder Vollmacht **nicht** rechtlich vertreten. Für nicht eigenständig aufgestellte Einheiten braucht die Regelung dafür eine ausdrückliche Klarstellung.
3. **Rollen statt Personen.** Befugnisse hängen an Funktionen („Leitung Einkauf"), nie an Namen — sonst veraltet die Regelung mit jedem Personalwechsel.
4. **Signaturform ist nicht Befugnis.** Eingescannte Unterschriften, E-Signatur-Tools und Signaturbilder sind Ausführungsdetails und gehören nicht in die DoA-Regelung (bei Bedarf: separate E-Signatur-Richtlinie).
5. **Ein Entwurf zählt nicht.** Für Audit-Zwecke existiert nur, was formell freigegeben, veröffentlicht und versioniert ist. Der Weg vom Entwurf zur Freigabe ist Teil des Auftrags, nicht Nachspiel.

## Baustein 1: Bestandsaufnahme

Sammle und bewerte, was schon existiert — meist mehr als gedacht, nur verstreut:
- Gesellschaftsrechtlicher Rahmen: Satzung/Gesellschaftsvertrag, Geschäftsordnungen, Handelsregisterstand (Organe, Prokuren)
- Vollmachten: Register vorhanden? Einzelvollmachten auffindbar? Widerrufsprozess?
- Interne Regelwerke: Vier-Augen-Prinzip-Policy, Unterschriftenrichtlinien-Entwürfe, Beschaffungs-/Investitionsrichtlinien, IKS-Kontrollen
- Gelebte Praxis: Wer gibt heute tatsächlich frei — und weicht das von der Papierlage ab?

Ergebnis: Tabelle mit Spalten `Regelwerk / Status (in Kraft, Entwurf, veraltet, fehlt) / deckt ab / Lücke`. Die Lückenliste ist die Grundlage für alles Weitere und die direkte Antwort auf ein Finding.

## Baustein 2: DoA-Matrix

Kern der Regelung: eine Matrix `Geschäftsvorfall × Wertstufe × Freigaberolle(n) × Unterschriftsregel`. Typische Geschäftsvorfallgruppen (an Bedarf anpassen):
- Einkaufs- und Verkaufsverträge, Rahmenverträge
- Investitionen (CapEx), außerplanmäßige Ausgaben
- Personalmaßnahmen (Einstellung, Vergütung, Trennung)
- Bank- und Zahlungsverkehr, Bürgschaften, Sicherheiten
- Prozessführung, Vergleiche, Verzicht auf Forderungen
- Immobilien, Miet- und Leasingverträge
- Konzerninterne Verträge

Regeln für die Matrix:
- **Wertstufen konkret und messbar** (`bis [BETRAG 1]`, `bis [BETRAG 2]`, `darüber`) — nie „im Zweifel höher freigeben lassen". Die konkreten Beträge sind unternehmensspezifisch und bleiben lokal; im Template stehen Platzhalter.
- Je Zelle: Freigaberolle(n), Einzel- oder Gemeinschaftsbefugnis, Vier-Augen-Anforderung, Dokumentationsweg der Freigabe.
- Jede Zeile endet mit einer Eskalationsstufe (Geschäftsführung/Gremium) — keine Zeile ohne Obergrenze.

## Baustein 3: Policy-Dokument

Gliederung der Unterschriften-/DoA-Policy:
```
1. Zweck & Geltungsbereich      — welche Gesellschaften, welche Geschäftsvorfälle
2. Grundsätze                    — Trennung extern/intern, Rollenprinzip, Vier-Augen-Prinzip
3. Externe Vertretung            — Organe, Prokuren, Vollmachten; Regel für nicht
                                   eigenständige Einheiten; Vollmachtsregister
4. Interne Freigaben             — Verweis auf die DoA-Matrix (Anlage)
5. Delegation & Dokumentation    — wer darf weiterdelegieren, wie wird jede Delegation
                                   dokumentiert (Template als Anlage)
6. Ausnahmen & Eilfälle          — nachträgliche Freigabe binnen definierter Frist
7. Pflege                        — Eigentümer-Rolle, Überprüfungsrhythmus, Versionierung
```

**Formatentscheidung — eigenständige Policy oder Anhang?** Existiert bereits eine etablierte, freigegebene Policy mit inhaltlicher Nähe (z. B. zum Vier-Augen-Prinzip), ist ein Anhang dort oft der schnellere Weg: ein Freigabeprozess statt zwei, ein Fundort statt zwei. Eigenständig lohnt sich, wenn die DoA mehrere Gesellschaften oder Regelwerke überspannt. Kriterium: Wo würde ein Fachbereich zuerst suchen? Frühzeitig abstimmen mit Controlling (Schwellenlogik), dem zuständigen Governance-Gremium (Freigabe) und den Fachbereichen, deren Prozesse die Matrix abbildet.

## Baustein 4: Audit-Response

Wenn der Auslöser ein Audit-Finding ist, zusätzlich:
1. **Finding zerlegen:** Jede bemängelte Einzelaussage (fehlende Policy, fehlende Schwellen, unfreigegebener Entwurf …) wird eine Zeile im Maßnahmenplan.
2. **Maßnahmenplan:** Je Zeile Maßnahme, verantwortliche Rolle, Termin, Nachweisdokument. Zusagen an die Revision nur mit Terminen, die die formelle Freigabe realistisch einschließen.
3. **Nachweis:** Die finalisierte, freigegebene Policy aktiv an die Revision übergeben — das Finding schließt nicht mit dem Dokument, sondern mit dem dokumentierten Nachweis.
4. **Wiedervorlage:** Termin für den Umsetzungs-Check nach Rollout (stichprobenartig: laufen Freigaben tatsächlich nach Matrix?).

## Workflow

1. **Auslöser & Scope klären:** Audit-Finding oder proaktiv? Eine Gesellschaft oder Gruppe? Frist?
2. **Bestandsaufnahme** (Baustein 1) — bei Gruppen je Gesellschaft.
3. **Formatentscheidung & Stakeholder** (Baustein 3) — vor dem Schreiben, nicht danach.
4. **DoA-Matrix entwerfen** (Baustein 2) und mit Controlling/Fachbereichen validieren.
5. **Policy-Entwurf** im Governance-Format (siehe Skill `governance-format`).
6. **Formelle Freigabe & Veröffentlichung** — Freigabeweg, Datum und Version im Dokument.
7. **Rollout & ggf. Audit-Nachweis** (Baustein 4).

## Übergabe

Liefere: Bestandsaufnahme mit Lückenliste, DoA-Matrix mit Platzhalter-Schwellen, Policy-Entwurf (oder Anhangs-Entwurf zur bestehenden Policy), Delegations-Dokumentations-Template, bei Audit-Auslöser den Maßnahmenplan. Vor Weitergabe: Skill `vertraulichkeits-gate`.

**Grenze:** Ob eine konkrete Vollmacht oder Prokura wirksam erteilt ist und wie ein Rechtsträger nach lokalem Gesellschaftsrecht vertreten wird, ist juristische Einzelfallprüfung — dieser Skill strukturiert die Regelung, ersetzt aber keine Rechtsberatung.
