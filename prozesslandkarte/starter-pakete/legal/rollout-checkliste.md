# Rollout-Checkliste: Prozesslandkarte in der Rechtsabteilung (ChatGPT Enterprise)

Von null bis zum laufenden Betrieb in vier Etappen. Aufwand: Etappe 1–2 ein
Tag für eine Person, Etappe 3 eine Woche nebenher, Etappe 4 verteilt über
4–6 Wochen. **Kritischer Pfad:** Nur die IT-/Datenschutz-Freigabe (Punkt 1)
hat Wartezeit — alles bis Etappe 2 lässt sich parallel vorbereiten; ob die
Freigabe formal schon vor dem Eigentest oder erst vor der Teamfreigabe
(Punkt 10) vorliegen muss, regelt die interne KI-Richtlinie.

## Etappe 1 — Setup (eine Person, ~halber Tag)

- [ ] **1. IT-/Datenschutz-Freigabe anstoßen** — zuerst, weil einziger Schritt
      mit Wartezeit. Argumentationshilfe: Es wird nur Prozesswissen
      verarbeitet, keine Mandats-/Falldaten; Checkliste in
      `chatgpt/einrichtung-custom-gpt.md`.
- [ ] **2. Repository auf den Arbeitsrechner holen** (GitHub → Code →
      Download ZIP → entpacken).
- [ ] **3. GPT „Prozess-Interviewer" anlegen** (~15 Min):
      Instructions aus `chatgpt/gpt-instructions-prozess-interview-legal.md`
      (Legal-Edition, Vertraulichkeitsregeln enthalten) · Knowledge:
      `vorlagen/prozess-template.md` · **Code Interpreter an** (Datei-Downloads)
      · Sichtbarkeit zunächst „Nur ich".
- [ ] **4. GPT „Prozessmap-Studio" anlegen** (~10 Min):
      Instructions aus `chatgpt/gpt-instructions-prozessmap-studio.md` ·
      Knowledge: `vorlagen/ki-prozessmap-template.md`,
      `anleitung/ki-potenzial-analyse.md`,
      `vorlagen/prozessmap-visual-template.html` · **Code Interpreter an**.
- [ ] **5. Ablageort anlegen** (z. B. SharePoint-Ordner
      `prozesslandkarte/prozesse/legal/`) und in beide GPT-Beschreibungen
      eintragen.

## Etappe 2 — Generalprobe (dieselbe Person, ~1–2 Stunden)

- [ ] **6. Probe-Interview führen:** entweder zu einem eigenen, unkritischen
      Prozess — oder mit dem Drehbuch `tests/fixtures/testfall-1-vollstaendig.md`.
      Prüfen (Kriterien: `tests/testplan.md`, Testfälle 1 und 3): max. 1–2
      Fragen pro Nachricht · alle 5 Kopfwissen-Fragen einzeln · Ergebnis kommt
      als Download · nichts Fallbezogenes, keine Namen im Dokument.
- [ ] **7. Map + Poster erzeugen:** heruntergeladene IST-Doku ins
      Prozessmap-Studio anhängen → „Map und Poster bitte" → beide Downloads
      prüfen (Kriterien: Testfall 7) · HTML im Browser öffnen · Probedruck:
      Drucken → „Als PDF speichern" (A4 quer ist eingebaut).
- [ ] **8. Befunde festhalten** (`tests/pruefbogen.md`); nicht Bestandenes →
      Instructions anpassen → nur die betroffenen Punkte wiederholen.

## Etappe 3 — Validierung mit Menschen (~1 Woche nebenher)

- [ ] **9. Einsteiger-Test (Testfall 6):** Eine ungebriefte Person bekommt nur
      den `LEITFADEN-EINSTEIGER.md` und dokumentiert einen unkritischen
      Prozess. Beobachten, nicht helfen; jede nötige Hilfe notieren und in den
      Leitfaden einarbeiten.
- [ ] **10. GPTs freigeben:** Sichtbarkeit auf „Personen mit Link" (nicht
      „öffentlich") und Links ans Team geben — sofern Freigabe aus Punkt 1
      vorliegt.
- [ ] **11. Team-Demo (~20 Min):** Problem benennen („Wissen steckt in Köpfen,
      KI kann nur unterstützen, was dokumentiert ist") → kurzes Live-Interview
      im GPT → die Kette IST-Doku → Map → Poster am Beispiel zeigen. Wirksamste
      Stelle: Abschnitt 9 (Kopfwissen) vorlesen und darauf hinweisen, dass die
      WENN/DANN-Regeln aus Abschnitt 6 genau die Kriterien sind, die „es
      angeblich nicht gibt". Ausblick: die „Menschliche Verantwortung"-Spalte —
      niemand wird wegdokumentiert.

## Etappe 4 — Rollout (Team, Wochen 2–6)

- [ ] **12. Inventur-Workshop** (90 Min): Starter-Landkarte
      (`landkarte-legal-starter.md`) durchgehen — streichen, umbenennen,
      ergänzen, zuordnen; pro Person die ersten 2–3 eigenen Prozesse markieren
      (Priorität: Was macht nur eine Person? Was frisst Zeit? Was ist
      fristenkritisch?). Ablauf: README dieses Starter-Pakets.
- [ ] **13. Phase 2 laufen lassen:** Jede:r dokumentiert die markierten
      Prozesse per Interview-GPT (~45 Min/Prozess), Peer-Review durch die
      Vertretung („Könnte ich das morgen allein?"), Ablage am vereinbarten Ort.
- [ ] **14. Phase-4-Workshop** (2–3 h, nach den ersten 5–8 Dokumenten):
      Maps im Studio erzeugen lassen und gemeinsam validieren — besonders die
      Spalte „Menschliche Verantwortung" ist eine Team-Entscheidung, kein
      KI-Vorschlag. Danach 1–2 **Piloten** mit dem besten
      Nutzen-Aufwand-Verhältnis starten.
- [ ] **15. Pflege verankern:** Quartals-Review der Landkarte; jede umgesetzte
      Automatisierung aktualisiert das Prozessdokument (Version hochzählen) —
      die Dokumente beschreiben immer den IST-Zustand.
