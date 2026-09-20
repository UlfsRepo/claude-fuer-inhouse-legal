# Vertraulichkeitsregeln für KI-Interviews in der Rechtsabteilung

Die generische Regel des Frameworks („keine Kundendaten, Personalia,
Konditionen") reicht für eine Rechtsabteilung nicht: Hier unterliegen Vorgänge
dem Mandats- bzw. Berufsgeheimnis, sind privilege-relevant oder betreffen
laufende Verfahren. **Grundsatz: Dokumentiert wird der Prozess, nie der Fall.**

## Block zum Einfügen in die GPT-Instructions / den Claude-Skill

> Den folgenden Text in den Instructions unter „Schütze Vertraulichkeit"
> ERGÄNZEN (die generische Regel bleibt bestehen):

---

Besondere Regeln für die Rechtsabteilung — dokumentiert wird der Prozess, nie
der Fall. Ins Dokument dürfen NICHT:

- Mandats- oder Einzelfallbezüge: keine Fallnamen, Aktenzeichen, Gegenparteien,
  Vertragspartner oder erkennbar beschriebene laufende/abgeschlossene Verfahren.
- Rechtliche Bewertungen konkreter Fälle (Prozessrisiken, Erfolgsaussichten,
  Vergleichsbereitschaft) — das ist Anwaltsprodukt, kein Prozesswissen.
- Beträge mit Fallbezug: Streitwerte, Vergleichssummen, Rückstellungen,
  Kanzleihonorare einzelner Mandate.
- Namen externer Kanzleien in Verbindung mit konkreten Fällen — als Rolle
  („externe Kanzlei") ist die Nennung im Ablauf in Ordnung.
- Personalia und Betriebsrats-/HR-Einzelfälle, auch anonymisiert erkennbare.
- Interne Schwellenwerte als Zahl (Freigabegrenzen, Budgetgrenzen) — die REGEL
  bleibt erhalten, die Zahl wird ersetzt durch „oberhalb der internen
  Freigabegrenze (siehe interne Richtlinie)".

Nennt die interviewte Person solche Details, nutze sie zum Verstehen des
Prozesses, übernimm ins Dokument aber nur die verallgemeinerte Regel — und
weise einmal freundlich darauf hin, dass Fallbezüge nicht ins Dokument gehören.
Beispiel: Aus „Im Verfahren gegen <Gegner> haben wir bei <Summe> verglichen,
weil Richter <Name>…" wird höchstens: „WENN Prozessrisiko als hoch bewertet
DANN Vergleichsoption prüfen — Bewertung erfolgt je Einzelfall durch die
zuständige Jurist:in."

---

## Prüfliste für das Review (Phase 3) in der Rechtsabteilung

Zusätzlich zum normalen Vertretungs-Test prüft der/die Reviewer:in jedes
Legal-Prozessdokument vor der Freigabe auf:

- [ ] Kein Fall, keine Partei, kein Verfahren identifizierbar (auch nicht
      durch Kombination von Details: Branche + Zeitraum + Summe kann reichen!)
- [ ] Keine rechtlichen Einzelfall-Bewertungen enthalten
- [ ] Keine konkreten Beträge mit Fallbezug, keine internen Schwellenwerte als Zahl
- [ ] Externe Kanzleien nur als Rolle, nicht als Name-im-Fall
- [ ] Entscheidungsregeln bleiben trotzdem vollständig (WENN/DANN erhalten,
      nur die vertrauliche Ausprägung ersetzt)
- [ ] Ablage des Dokuments entspricht der internen Informationsklassifizierung

## Hinweis zur Werkzeug-Umgebung

Diese Regeln steuern, was ins **Dokument** gelangt. Unabhängig davon gilt:
Ob und welche Inhalte überhaupt in ein KI-Werkzeug eingegeben werden dürfen,
regelt die interne KI-/IT-Richtlinie des Unternehmens — im Zweifel vor dem
ersten Interview mit Datenschutz/IT-Sicherheit klären. Für Interviews genügt
es fast immer, ganz ohne Fallbeispiele mit echten Namen zu erzählen: „ein
Lieferant", „ein laufendes Verfahren", „eine Behörde" tragen dieselbe
Prozessinformation.
