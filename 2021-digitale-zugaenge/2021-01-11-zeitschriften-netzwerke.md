---
title: "Digitale Zugänge zu Periodika"
subtitle: ""
author: Till Grallert
date: 2021-01-11
ORCID: orcid.org/0000-0002-5739-8094
tags:
    - presentation
    - OpenArabicPE
lang: de
duration: 5
---

## Digitale Zugänge zu Periodika

Till Grallert, Orient-Institut Beirut (OIB), @[tillgrallert](https://twitter.com/tillgrallert)

11 Januar 2021

Slides: [https://OpenArabicPE.github.io/slides/2021-digitale-zugaenge/](https://OpenArabicPE.github.io/slides/2021-digitale-zugaenge/index.html)

## Forschungsfragen

- Was sind die wichtigsten Knoten (Autor_innen, Periodika, Orte etc.) im diskursiven Feld der Presse?
- Produktionsgeschichte:
    + Wie wurden Periodika produziert?
    + Wer verfasste die mehrheitlich anonymen Texte?
    + Wie hoch ist die Wiederverwertungsrate und wie "reisten" Texte?
- Rezeptionsgeschichte:
    + Wer hat was, wo und wann gelesen (und darüber geschrieben)?

## (Digitale) Forschungsansätze

- (historische/ soziale) Netzwerkanalyse
- Bibliometrie
- Stylometrie

## Benötigte Daten?

- Bibliographische Angaben auf der Artikelebene
- Volltext mit Auszeichnung von *named entities*
- Normdatensätze (z.B. [GND](https://www.dnb.de/DE/Professionell/Standardisierung/GND/gnd.html), [VIAF](https://viaf.org/), [Wikidata](https://wikidata.org/)) für
    - Disambiguierung: "Paris" als konkreter Ort oder konkrete Person
    - Anreicherung von Daten: z.B. Raumdaten oder Lebensdaten

## Vorhandene Daten: [Open Arabic Periodical Editions](https://openarabicpe.github.io)

Modellierter Volltext (TEI XML), bibliographische Metadaten (MODS, RDF, BibTeX), Normdaten (TEI XML)

| periodical                                                                        | doi                                                              | volumes | issues | articles | words   | words per article |
| :--------                                                                         | :--                                                              | ----:   | ----:  | ----:    | ----:   | ----:             |
| [**al-Ḥaqāʾiq**](https://www.github.com/openarabicpe/journal_al-haqaiq)              | [10.5281/zenodo.1232016](https://doi.org/10.5281/zenodo.1232016) | 3       | 35     | 389      | 298090  | 832.66            |
| [**al-Ḥasnāʾ**](https://www.github.com/openarabicpe/journal_al-hasna)             | [10.5281/zenodo.3556246](https://doi.org/10.5281/zenodo.3556246) | 1       | 12     | 201      | NA      | NA                |
| [al-Manār](https://www.github.com/openarabicpe/journal_al-manar)                  |                                                                  | 35      | 537    | 4300     | 6144593 | 1437.73           |
| [**al-Muqtabas**](https://www.github.com/openarabicpe/journal_al-muqtabas)           | [10.5281/zenodo.597319](https://doi.org/10.5281/zenodo.597319)   | 9       | 96     | 2964     | 1981081 | 873.34            |
| [al-Ustādh](https://www.github.com/openarabicpe/journal_al-ustadh)                | [10.5281/zenodo.3581028](https://doi.org/10.5281/zenodo.3581028) | 1       | 42     | 435      | 221447  | 582.21            |
| [al-Zuhūr](https://www.github.com/openarabicpe/journal_al-zuhur)                  | [10.5281/zenodo.3580606](https://doi.org/10.5281/zenodo.3580606) | 4       | 39     | 436      | 292333  | 695.09            |
| [**Lughat al-ʿArab**](https://www.github.com/openarabicpe/journal_lughat-al-arab) | [10.5281/zenodo.3514384](https://doi.org/10.5281/zenodo.3514384) | 3       | 34     | 939      | 373832  | 485.21            |
| **total**                                                                         |                                                                  | 56      | 795    | 9664     | 9311376 |                   |

## Vorhandene Daten: [Project Jarāʾid](https://projectjaraid.github.io)


<div class="c_width-50 c_left">
- Bibliographische Metadaten zu allen (3300+) arabischen Periodika bis 1930 (TEI XML)

```xml
<biblStruct type="periodical">
  <monogr>
     <title level="j" xml:lang="ar-Latn-x-ijmes">Al-Iqbāl</title>
     <title level="j" xml:lang="ar">الاقبال</title>
     <idno type="jaraid">t1r2353</idno>
     <textLang mainLang="ar"/>
     <editor>
        <persName ref="jaraid:pers:1926" xml:lang="ar-Latn-x-ijmes">ʿAbd al-Bāsiṭ al-Unsī</persName>
     </editor>
     <imprint>
        <pubPlace>
           <placeName ref="jaraid:place:2">Beirut</placeName>
        </pubPlace>
        <date type="onset" when="1902-04-09">1902</date>
     </imprint>
  </monogr>
</biblStruct>
```

</div><div class="c_width-50 c_right">

- Normdaten (TEI XML)

```xml
<person>
    <persName xml:lang="ar-Latn-x-ijmes">ʿAbd al-Bāsiṭ al-Unsī</persName>
    <persName xml:lang="ar">عبد الباسط الانسي</persName>
    <idno type="jaraid">1926</idno>
    <idno type="VIAF">22151654727108281690</idno>
    <birth resp="#org_viaf" when="1867">1867</birth>
    <death resp="#org viaf" when="1940">1940</death>
</person>
```

```xml
<place type="town">
    <placeName xml:lang="en">Beirut</placeName>
    <placeName source="#org_geon" xml:lang="ar">بيروت</placeName>
    <placeName source="#org_geon" xml:lang="fr">Beyrouth</placeName>
    <location source="#org_geon">
        <geo>33.88894, 35.49442</geo>
    </location>
    <idno type="jaraid">2</idno>
    <idno type="url">http://en.wikipedia.org/wiki/Beirut</idno>
    <idno type="geon">276781</idno>
</place>
```

</div>

## Netzwerk erwähnter Periodika (OpenArabicPE)

<div class="c_width-60 c_left">

![Figure: Network of periodicals mentioned *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab* and *al-Muqtabas*; weights per issue. Node size/colour: in-degree](../assets/networks/network_oape-p3a6afa20_referenced-periodicals-per-issue_circular-n-size_in-degree.svg)

</div>
<div class="c_width-30 c_right">

1. only a few nodes are of relative importance (44 of 465)
2. *al-Muqtabas* accounts for the vast majority of references
3. all periodicals are primarly self-referential
4. confirms the bias on Cairo and Beirut (8 of 9)
2. highly centralised in terms of geographic distribution (10 locations)
3. surprising members

</div>

## Soziales Netzwerk von Autor_innen (OpenArabicPE)

<div class="c_width-60 c_left">

![Figure: Network of authors with bylines in *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab* and *al-Muqtabas*. Number of nodes: 321; node size/colour: out-degree; edge size: number of articles](../assets/networks/network_oape-p3a6afa20_authors_unimodal-n-size_out-degree.svg)

</div><div class="c_width-30 c_right">

1. only a few nodes are of relative importance
2. limited overlap between journals from the same city
3. nodes are connected by various other social networks (education, imperial service, family relations etc.)
4. many Iraqis
2. few Syrians
3. few Christians
2. many poets
3. majority not covered by scholarly literature

</div>

## Soziales Netzwerk von Herausgeber_innen (Jarāʾid)

<div class="c_width-60 c_left">

![Figure: Network of publishers, 1800--1929. Number of nodes: 2702;  node size: betweenness centrality](../assets/networks/network_project-jaraid_people-titles-n-size_betweenness-centrality.svg)

</div><div class="c_width-30 c_right">

1. Network?
2. Very limited collaboration
3. Due to data/knowledge **bias**!

</div>

## Geographisches Netzwerk von Autor_innen

<div class="c_width-50 c_left c_height-50">

![Map: Locations in bylines in *al-Muqtabas* (Cairo and Damascus)](../assets/maps/map-oclc_4770057679-bylines-ME.png)

</div><div class="c_width-50 c_right c_height-50">

![Map: Locations in bylines in *al-Ḥaqāʾiq* (Damascus)](../assets/maps/map-oclc_644997575-bylines-ME.png)

</div><div class="c_width-50 c_left c_height-50">

![Map: Locations in bylines in *al-Ḥasnāʾ* (Beirut)](../assets/maps/map-oclc_792756327-bylines-ME.png)

</div><div class="c_width-50 c_right c_height-50">

![Map: Locations in bylines in *Lughat al-ʿArab* (Baghdad)](../assets/maps/map-oclc_472450345-bylines-ME.png)

</div>

## Probleme

- *Digital divide*
    + Digitalität ist resourcenintensiv!
    + Hardware, Software, Standards, Infrastrukturen sind im Globalen Norden verortet
- Digitale Unzugänglichkeit
    + Bezahlschranken, mangelnde maschinenlesbarkeit, Datensilos
    + Mangelnde Kenntnisse des Materials bei den Digitalisierenden
    + ungeeigneter technischer Apparat (*technology stack*)
        + für Geisteswissenschaftler_innen praktisch dysfunctionales OCR
    - mangelnde (Forschungs-)Infrastrukturen
- Postkoloniale digitale Unsichtbarkeit
    + mangelnde Corpora, Normdatensätze
    + methodologische Rückständigkeit
    + (stark) eingeschränkte Forschung(smöglichkeiten)