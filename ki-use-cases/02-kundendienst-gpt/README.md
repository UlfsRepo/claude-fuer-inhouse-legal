# Use Case 2: Kundendienst GPT

**Zielgruppe:** Kolleginnen und Kollegen aus dem Kundenmanagement und Logistik

## Ziel

KI unterstützt bei allgemeinen Rechtsfragen im Zusammenhang mit
Kundendienstfällen. Diese Fragen sind in der Regel wenig komplex, benötigen aber
meist umfassende Sachverhaltskenntnis und ggf. Recherche in rechtlichen
Datenbanken. Der Kern der rechtlichen Anfragen wiederholt sich in vielen Fällen.

## Status quo (Pain Point)

1. Sichtung der Unterlagen und Klärung des Sachverhalts ist zeitaufwendig.
2. Oft wiederkehrende rechtliche Kernfragen, obwohl der Sachverhalt immer
   unterschiedlich ist.

## Umsetzungsidee mit ChatGPT Enterprise

Zwei Stufen – heute Stufe 1 bauen:

**Stufe 1 (Pilot im Legal-Team):** Custom GPT, der dem Legal-Team die Bearbeitung
beschleunigt: Sachverhalt strukturieren, wiederkehrende Kernfrage erkennen, auf
Basis der hinterlegten FAQ-Wissensbasis einen Antwortentwurf erstellen.

**Stufe 2 (später, nach Freigabe):** Der GPT wird direkt für Kundenmanagement /
Logistik freigegeben und beantwortet Standardfragen selbst; bei Unsicherheit oder
Eskalationsthemen verweist er an Legal (mit vorstrukturierter Anfrage → passt zu
Use Case 3, Triage).

## Erste Schritte

1. **Top-Fragen sammeln:** Die 10–20 häufigsten wiederkehrenden Rechtsfragen aus
   Kundendienstfällen identifizieren (Gewährleistung vs. Kulanz, Verjährung,
   Rücktritt/Minderung, Produkthaftung, Ersatzteilverfügbarkeit, Datenlöschung …).
2. **FAQ-Wissensbasis füllen:** [faq-wissensbasis-vorlage.md](faq-wissensbasis-vorlage.md)
   – je Frage die abgestimmte abgestimmte Antwortlinie inkl. Grenzen.
3. **Custom GPT anlegen** mit [system-prompt.md](system-prompt.md).
4. **Test:** 5 anonymisierte Echt-Anfragen aus der Vergangenheit durchspielen und
   Antwortentwürfe mit den tatsächlich gegebenen Antworten vergleichen.

## Leitplanken

- Der GPT gibt **interne Antwortentwürfe**, keine Rechtsauskünfte an Endkunden.
- Bei Personenschäden, Medienanfragen, Behördenkontakt, drohender Klage → immer
  Eskalation an Legal, keine eigene Antwort.
- Wissensbasis ist die einzige Quelle für Unternehmenspositionen; allgemeines
  Rechtswissen des Modells nur als Hintergrund, deutlich gekennzeichnet.
