# Starter-Paket: Rechtsabteilung (Inhouse Legal)

Dieses Paket beschleunigt den Start des Frameworks in einer Rechtsabteilung.
Es ist bewusst **generisch** — Unternehmensspezifisches wird im Workshop bzw.
in der internen Ablage ergänzt, nicht hier.

## Inhalt

| Datei | Zweck |
|---|---|
| `landkarte-legal-starter.md` | Vorbefüllte Bereichs-Landkarte mit ~20 typischen Legal-Prozessen — im Workshop streichen, umbenennen, ergänzen statt bei null anfangen |
| `vertraulichkeit-legal.md` | Verschärfte Vertraulichkeitsregeln für das KI-Interview in Rechtsabteilungen (Mandatsgeheimnis!) — zum Einfügen in GPT-Instructions bzw. Claude-Skill, plus Prüfliste fürs Review |

## So nutzt ihr das Paket (Phase 1: Inventur-Workshop, 60–90 Min)

**Vorbereitung (Teamleitung, 15 Min):**
1. `landkarte-legal-starter.md` in die interne Ablage kopieren als
   `prozesse/legal/landkarte.md`.
2. Vertraulichkeitsblock aus `vertraulichkeit-legal.md` in die Instructions
   des Custom GPT (bzw. den Claude-Skill) einfügen — VOR dem ersten Interview.

**Im Workshop:**
1. **Streichen (15 Min):** Zeilen, die es bei euch nicht gibt, löschen.
2. **Umbenennen (15 Min):** Prozessnamen an eure Sprache anpassen ("Legal
   Intake" heißt bei euch vielleicht "Rechtsanfragen-Postfach").
3. **Ergänzen (20 Min):** Was fehlt? Den Vollständigkeits-Check am Ende der
   Landkarte durchgehen (Kalender, Postfach, Jahresrhythmus, Einzelwissen).
4. **Zuordnen (20 Min):** Je Zeile Verantwortliche:n und reale Frequenz
   eintragen; die 3–5 Prozesse markieren, die zuerst dokumentiert werden.
   Faustregel für die Priorität: Was macht nur EINE Person? Was frisst am
   meisten Zeit? Was ist fristenkritisch?

**Danach:** Weiter mit Phase 2 wie im `LEITFADEN-EINSTEIGER.md` beschrieben —
jede:r dokumentiert die eigenen markierten Prozesse per KI-Interview.

## Warum eine eigene Vertraulichkeitsregel für Legal?

Eine Rechtsabteilung dokumentiert Prozesse über Vorgänge, die dem Mandats-
bzw. Berufsgeheimnis unterliegen oder Privilege-relevant sind. Die generische
Regel („keine Kundendaten") reicht dort nicht. Grundsatz:
**Dokumentiert wird der Prozess, nie der Fall.** Details und die konkreten
Formulierungen: `vertraulichkeit-legal.md`.
