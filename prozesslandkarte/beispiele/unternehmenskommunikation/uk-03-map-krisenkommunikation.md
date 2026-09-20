---
map_id: UK-03-MAP
prozess_id: UK-03
name: Krisenkommunikation (akuter Krisenfall)
bereich: Unternehmenskommunikation
process_owner: Leitung Unternehmenskommunikation — Vertretung Pressesprecher:in, Rufbereitschaft hinterlegt
status: entwurf
version: "0.1"
datum: 2026-09-20
erstellt_von: Beispiel — generisch, frei erfunden
vertraulichkeit: intern
zielbild:
  automatisiert_oder_ki_gestuetzt: "50–65 %"
  vollautomatisiert: "15–25 %"
  menschliche_entscheidung: "40–55 %"
  reaktionszeit_vorher_nachher: ">3 Std → <60 Min"
  aufwandsreduktion: "bis zu 50 % in Monitoring, Q&A und Lagebildern"
---

# KI-Prozessmap: Krisenkommunikation (Beispiel)

> **Generisches, frei erfundenes Beispiel**, das zeigt, wie eine ausgefüllte
> KI-Prozessmap (`vorlagen/ki-prozessmap-template.md`) aussieht. Es gehört zur
> IST-Dokumentation `uk-03-krisenkommunikation.md`.

## Steckbrief

| | |
|---|---|
| 👤 **Process Owner** | Leitung Unternehmenskommunikation; Vertretung Pressesprecher:in |
| 🎯 **Prozessziel** | Im Krisenfall schnell, konsistent und rechtssicher kommunizieren, um Reputations- und Folgeschäden zu begrenzen — aus einem Vorfall soll keine Vertrauenskrise werden. |
| 📋 **Scope / Varianten** | Unfall/Störfall · Produktrückruf · Datenpanne · kritische Berichterstattung · Social-Media-Eskalation |
| ➡️ **Input** | Presseanfragen · interne Vorfallsmeldungen · Monitoring-Ausschläge · Behördenkontakte |
| 📄 **Output** | Holding Statement · Q&A/Sprachregelung · Lagebilder · interne Information · Abschlussbericht mit Learnings |
| 👥 **Zielgruppen** | Geschäftsführung · Medien · Mitarbeitende · ggf. Behörden · betroffene Kunden/Partner |
| 🚚 **Lieferanten** | Betroffener Fachbereich (Fakten) · Rechtsabteilung · Monitoring-Dienstleister |
| 📊 **KPIs** | Zeit bis erste Reaktion · Freigabe-Durchlaufzeit · Konsistenz über Kanäle · Anteil Krisen mit Nachbereitung |

## Gesamt-Zielbild (Zielwerte)

| Kennzahl | Zielwert |
|---|---|
| ⚙️ Operative Tätigkeiten automatisiert oder KI-gestützt | 50–65 % |
| 🤖 Gesamtprozess ohne manuelle Bearbeitung | 15–25 % |
| 👥 Menschliche Entscheidung & Verantwortung | 40–55 % — bewusst hoch: jede externe Aussage bleibt beim Menschen |
| ⏱️ Zeit bis erste Reaktion | >3 Std → <60 Min |
| 📈 Aufwandsreduktion | bis zu 50 % in Monitoring, Q&A-Erstellung und Lagebildern |

## Prozessschritte

### Schritt 1 — Triage & Lagebewertung 🔍
**Ziel-Automatisierungsgrad:** 70 % (hoch)

**Was kann automatisiert werden?**
- Monitoring-Alerts mit Schwellenwerten (Reichweite, Tonalität)
- Krisenkriterien-Checkliste als geführte Abfrage
- Automatische Info an Leitung UK bei Stufe ≥ 2

**KI-Einsatz (sinnvolle Anwendungen):**
- KI clustert eingehende Signale und bewertet Dynamik
- KI schlägt Krisenstufe mit Begründung und Vergleichsfall vor

**Menschliche Verantwortung:**
- Verbindliche Stufen-Entscheidung (beobachten / reagieren / Krisenstab)

**Erwarteter Nutzen (Haupteffekte):**
- Einheitliche Einstufung statt Bauchgefühl; frühere Erkennung

### Schritt 2 — Fakten sichern 🔬
**Ziel-Automatisierungsgrad:** 40 % (mittel)

**Was kann automatisiert werden?**
- Krisenkanal + Faktenlog automatisch aufsetzen
- Erinnerungen je offener Faktenfrage; Versionierung des Faktenstands

**KI-Einsatz (sinnvolle Anwendungen):**
- KI trennt gesicherte von ungesicherten Angaben und markiert Widersprüche
- KI baut den Zeitstrahl aus Meldungen und Mails

**Menschliche Verantwortung:**
- Verbindliche Feststellung, was als gesichert gilt

**Erwarteter Nutzen (Haupteffekte):**
- Belastbare Basis für alle Aussagen; keine vorläufigen Zahlen nach außen

### Schritt 3 — Holding Statement entwerfen ✍️
**Ziel-Automatisierungsgrad:** 60 % (mittel–hoch)

**Was kann automatisiert werden?**
- Vorlagen je Krisentyp, vorab rechtlich freigegebene Bausteine
- Vorbefüllung aus dem Faktenlog

**KI-Einsatz (sinnvolle Anwendungen):**
- KI erstellt Entwurf nach Muster (Ernstnehmen → Fakten → Maßnahmen → nächstes Update)
- KI prüft gegen No-Gos (Spekulation, Schuldzuweisung, verbrannte Formulierungen)

**Menschliche Verantwortung:**
- Inhalt, Tonalität und Empathie jeder Aussage; was bewusst NICHT gesagt wird

**Erwarteter Nutzen (Haupteffekte):**
- Entwurf in Minuten statt einer halben Stunde, konstante Qualität

### Schritt 4 — Freigabe 🛡
**Ziel-Automatisierungsgrad:** 30 % (niedrig)

**Was kann automatisiert werden?**
- Freigabe-Routing mit Frist-Uhr, Erinnerungen und dokumentiertem Verlauf

**KI-Einsatz (sinnvolle Anwendungen):**
- KI fasst Änderungswünsche zusammen und zeigt Abweichungen zur Vorversion

**Menschliche Verantwortung:**
- Freigabe durch Recht und Geschäftsführung — ohne Ausnahme

**Erwarteter Nutzen (Haupteffekte):**
- Freigabe-Durchlaufzeit von 90 auf ~20 Minuten; 100 % dokumentiert

### Schritt 5 — Aussenden & veröffentlichen 🌐
**Ziel-Automatisierungsgrad:** 80 % (hoch)

**Was kann automatisiert werden?**
- Versand an Verteiler, Website-/Intranet-Publikation aus einer Quelle
- Regel „intern vor extern" technisch verankern

**KI-Einsatz (sinnvolle Anwendungen):**
- KI erstellt kanalgerechte Varianten und prüft Konsistenz

**Menschliche Verantwortung:**
- Finale Publish-Entscheidung, Zeitpunkt und Reichweite

**Erwarteter Nutzen (Haupteffekte):**
- Eine Botschaft, alle Kanäle; Mitarbeitende erfahren es nicht aus der Presse

### Schritt 6 — Q&A & Sprachregelung 💬
**Ziel-Automatisierungsgrad:** 65 % (hoch)

**Was kann automatisiert werden?**
- Q&A-Bibliothek: 60 % der Fragen kehren wieder — Wiederverwendung statt Neuanfang

**KI-Einsatz (sinnvolle Anwendungen):**
- KI entwirft Antworten aus Faktenlog + Bibliothek, erkennt Fangfragen
- KI hält Q&A bei neuem Faktenstand aktuell

**Menschliche Verantwortung:**
- Freigabe jeder Antwort; Umgang mit heiklen Einzelfragen

**Erwarteter Nutzen (Haupteffekte):**
- Q&A v1 in unter einer Stunde statt in zwei

### Schritt 7 — Monitoring & Lagebild 📊
**Ziel-Automatisierungsgrad:** 75 % (hoch)

**Was kann automatisiert werden?**
- Laufendes Monitoring inkl. Nacht/Wochenende mit Alarmschwellen
- Lagebild-Gerüst 2x täglich automatisch aus Monitoring + Anfragenregister

**KI-Einsatz (sinnvolle Anwendungen):**
- KI fasst Berichterstattung und Tonalität zusammen, erkennt Gegennarrative
- KI schlägt Handlungsempfehlung vor

**Menschliche Verantwortung:**
- Bewertung der Lage und Entscheidung über nächste Schritte

**Erwarteter Nutzen (Haupteffekte):**
- Lagebild in 10 statt 45 Minuten; keine Monitoring-Lücken mehr

### Schritt 8 — Deeskalation & Nachbereitung 📈
**Ziel-Automatisierungsgrad:** 60 % (mittel–hoch)

**Was kann automatisiert werden?**
- Chronologie und Berichtsgerüst automatisch aus Krisenlog
- Erinnerung: Nachbereitung ist Pflichtschritt

**KI-Einsatz (sinnvolle Anwendungen):**
- KI erstellt Learnings-Entwurf und schlägt Vorlagen-Updates vor

**Menschliche Verantwortung:**
- Bewertung der Learnings; Entscheidung über Prozessänderungen

**Erwarteter Nutzen (Haupteffekte):**
- Aus jedem Fall wird Kompetenz; Vorlagen werden mit jedem Vorfall besser

## Ein Prozess — verschiedene Fälle

| Fall | Typ/Variante | Auslöser & Charakter | Wo der Prozess besonders gefordert ist | Was der Fall gelehrt hat |
|---|---|---|---|---|
| Produktrückruf (fiktiv) | Rückruf | Selbst festgestellt, planbar im Stundenbereich | Schritte 2 und 4: Zahlen erst gesichert, dann kommuniziert | Erste Mengenangabe war zu klein — Zahlen immer als vorläufig kennzeichnen |
| Shitstorm (fiktiv) | Social-Media-Eskalation | Fremdausgelöst, sehr schnell, emotional | Schritte 1 und 7: Dynamik-Bewertung und enge Taktung | Nicht jede laute Empörung ist eine Krise — Kriterienkatalog schützt vor Überreaktion |
| Datenpanne (fiktiv) | Datenschutzvorfall | Fristen laufen ab Minute eins, Behördenpfad | Schritte 4 und 5: Recht zwingend im Loop, intern vor extern | Meldepflicht-Fristen gehören in die Checkliste, nicht ins Gedächtnis |

## Automatisierungs-Verteilung im Prozess (Ziel)

| Kategorie | Anteil |
|---|---|
| Automatisiert (ohne menschliche Bearbeitung) | 15–25 % |
| KI-gestützt (Mensch entscheidet) | 30–40 % |
| Menschliche Entscheidung / Verantwortung | 40–55 % |

## Automatisierungs-Reifegrad (Zielbild)

| Stufe | Beschreibung | Status |
|---|---|---|
| 👤 Manuell | Zuruf, Wissen in Köpfen, Lagebilder zusammenkopiert | heute |
| ⚙️ Teilautomatisiert | Vorlagen & Verteiler vorhanden, Erinnerungen manuell | teilweise |
| 🔗 Integriert | Krisenlog als eine Quelle, Freigabe-Workflow mit Fristen | Ziel Phase 2 |
| 🤖 Intelligent (Ziel) | KI erkennt, entwirft, taktet — der Mensch entscheidet | Ziel Phase 3 |

## Umsetzungs-Roadmap (Empfehlung)

| Phase | Zeitraum | Maßnahmen |
|---|---|---|
| 1 — Quick Wins | 0–3 Monate | Rufbereitschaftsliste aktuell halten (automatische Erinnerung) · Q&A-Bibliothek aus alten Fällen aufbauen · Holding-Statement-Bausteine je Krisentyp vorab rechtlich freigeben |
| 2 — Integrierter Workflow | 3–9 Monate | Krisenkanal + Faktenlog automatisch aufsetzen · Freigabe-Workflow mit Frist-Uhr · Lagebild-Gerüst automatisiert |
| 3 — Agentischer Prozess | 9–18 Monate | KI-Monitoring rund um die Uhr mit Lagebild-Entwurf · Konsistenzprüfung über Kanäle · Learning Loop in die Vorlagen |

## SLA-Empfehlung

| Schritt | Zielzeit |
|---|---|
| Triage nach Signaleingang | < 30 Min |
| Faktenstand v1 | < 60 Min |
| Holding Statement freigegeben | < 60 Min nach bestätigter Krise |
| Interne Information | vor oder zeitgleich mit extern |
| Lagebild-Taktung | 2x täglich während Akutphase |
| Nachbereitung abgeschlossen | < 10 Arbeitstage nach Krisenende |

## Wichtige Risiken & Kontrollen

- ⚠️ Aussage ohne gesicherte Fakten — kein Versand ohne freigegebenen Faktenstand
- 🤖 KI-Entwurf ungeprüft — Vier-Augen-Prinzip, jede Aussage bleibt menschlich verantwortet
- ⚖️ Rechtliche Bewertung in der Sprachregelung — Recht zeichnet, Kommunikation formuliert
- 🔇 Stille — jede Lücke in der Taktung füllt das Gegennarrativ
- 📕 Vorlagen veralten — Nachbereitung ist Pflichtschritt, nicht Kür

## Wichtige Prinzipien

- ✓ Faktenbasiert — keine Spekulation über Ursache, Dauer oder Verantwortung
- ✓ Intern vor extern — Mitarbeitende erfahren Krisen nie aus der Presse
- ✓ Eine Quelle — alle Kanäle verweisen auf denselben Stand
- ✓ Ohne Schuldzuweisung — weder intern noch extern
- ✓ Dokumentiert — jede Entscheidung mit Zeitstempel und Owner
- ✓ Lernend — jeder Vorfall verbessert Vorlagen und Prozess

---
**Wichtig:** Automatisierung beschleunigt und entlastet — die menschliche
Verantwortung bleibt entscheidend für Fakten, Freigaben, Tonalität und jede
externe Aussage.
