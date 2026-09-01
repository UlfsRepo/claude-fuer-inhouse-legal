# Ablage-Taxonomie, Namenskonvention und SharePoint-Struktur

> Prozessschritte 1–2 des Steckbriefs: Ziel-Taxonomie für SharePoint und
> Namenskonventionen definieren, Metadaten-Set festlegen. Im Team abstimmen,
> dann als Wissensdatei in den Filing-Assistant-GPT hochladen.

## 1. Dokumenttypen (Taxonomie)

| Kürzel | Dokumenttyp | Beispiele |
|--------|-------------|-----------|
| VERTRAG | Vertrag (unterzeichnet) | Einkauf, NDA, SaaS, Dienstleistung |
| ENTWURF | Vertragsentwurf / Redline | |
| NACHTRAG | Nachtrag / Änderungsvereinbarung | |
| KUEND | Kündigung / Beendigung | |
| KORR | Korrespondenz | Anwaltsschreiben, Behörden |
| MEMO | Internes Memo / Vermerk | |
| VOLLM | Vollmacht | |
| GES | Gesellschaftsrechtliches Dokument | Beschlüsse, HR-Auszüge |
| RECH | Kanzleirechnung | → auch Use Case 5 |
| SONST | Sonstiges | |

## 2. Metadaten-Set (Pflichtfelder)

1. Dokumenttyp (Taxonomie oben)
2. Matter/Mandat (Schema: `M-JJJJ-NNN` oder bestehende Matter-Liste – abstimmen!)
3. Parteien (eigene Gesellschaft + externe Partei(en))
4. Dokumentdatum
5. Laufzeit (Beginn/Ende), automatische Verlängerung ja/nein
6. Kündigungsfrist

## 3. Namenskonvention

```
JJJJ-MM-TT_[TYP]_[Partei-extern]_[Kurzbeschreibung]_[Version/Status]
```

Beispiele:
- `2026-03-15_VERTRAG_MusterGmbH_Rahmenvertrag-Logistik_final-signiert.pdf`
- `2026-08-20_ENTWURF_ACME-Corp_NDA_v2-redline.docx`

Regeln:
- Datum = Dokumentdatum (nicht Ablagedatum)
- Keine Umlaute, keine Leerzeichen (Bindestriche), keine Sonderzeichen
- Status: `entwurf`, `redline`, `final`, `final-signiert`

## 4. SharePoint-Zielstruktur

```
/Legal/
├── 01_Vertraege/
│   ├── [Externe Partei A–Z oder je Matter]/
├── 02_Matter/
│   ├── M-JJJJ-NNN_[Kurzname]/
├── 03_Gesellschaftsrecht/
├── 04_Korrespondenz/
├── 05_Kanzleirechnungen/
├── 90_Unklar/          ← alles mit Konfidenz „niedrig"
```

> Entscheidung im Team: Ablage primär **je Partei** oder **je Matter**?
> (Empfehlung: je Matter, Partei als Metadatum/SharePoint-Spalte.)

## 5. Offene Punkte für IT & Data Privacy

- Berechtigungskonzept (wer sieht was in /Legal/?)
- Aufbewahrungs- und Löschfristen je Dokumenttyp
- Umgang mit personenbezogenen Daten in Korrespondenz
