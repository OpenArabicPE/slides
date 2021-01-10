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

## Forschungsfragen

- Was sind die wichtigsten Knoten (Autor_innen, Periodika, Orte etc.) im diskursiven Feld der Presse?
- Produktionsgeschichte:
    + Wie wurden Periodika produziert?
    + Wer verfasste die mehrheitlich anonymen Texte?
    + Wie hoch ist die Wiederverwertungsrate?
- Rezeptionsgeschichte:
    + Wer hat was, wo und wann gelesen (und darüber geschrieben)?

## Forschungsansätze

- (historische/ soziale) Netzwerkanalyse
- Bibliometrie
- Stylometrie

## Benötigte Daten?

- Bibliographische Angaben auf der Artikelebene
- Volltext mit Auszeichnung von *named entities*
- Normdatensätze (z.B. GND, VIAF, Wikidata) für
    - Disambiguierung: "Paris" als konkreter Ort oder konkrete Person
    - Anreicherung von Daten: z.B. Raumdaten oder Lebensdaten

## Vorhandene Daten: [Open Arabic Periodical Editions](https://openarabicpe.github.io)

Modellierter Volltext (TEI XML), bibliographische Metadaten (MODS, RDF, BibTeX), Normdaten (TEI XML)

| periodical                                                                        | doi                                                              | volumes | issues | articles | words   | words per article |
| :--------                                                                         | :--                                                              | ----:   | ----:  | ----:    | ----:   | ----:             |
| [**al-Ḥaqāʾiq**](https://www.github.com/openarabicpe/digital-haqaiq)              | [10.5281/zenodo.1232016](https://doi.org/10.5281/zenodo.1232016) | 3       | 35     | 389      | 298090  | 832.66            |
| [**al-Ḥasnāʾ**](https://www.github.com/openarabicpe/journal_al-hasna)             | [10.5281/zenodo.3556246](https://doi.org/10.5281/zenodo.3556246) | 1       | 12     | 201      | NA      | NA                |
| [al-Manār](https://www.github.com/openarabicpe/journal_al-manar)                  |                                                                  | 35      | 537    | 4300     | 6144593 | 1437.73           |
| [**al-Muqtabas**](https://www.github.com/tillgrallert/digital-muqtabas)           | [10.5281/zenodo.597319](https://doi.org/10.5281/zenodo.597319)   | 9       | 96     | 2964     | 1981081 | 873.34            |
| [al-Ustādh](https://www.github.com/openarabicpe/journal_al-ustadh)                | [10.5281/zenodo.3581028](https://doi.org/10.5281/zenodo.3581028) | 1       | 42     | 435      | 221447  | 582.21            |
| [al-Zuhūr](https://www.github.com/openarabicpe/journal_al-zuhur)                  | [10.5281/zenodo.3580606](https://doi.org/10.5281/zenodo.3580606) | 4       | 39     | 436      | 292333  | 695.09            |
| [**Lughat al-ʿArab**](https://www.github.com/openarabicpe/journal_lughat-al-arab) | [10.5281/zenodo.3514384](https://doi.org/10.5281/zenodo.3514384) | 3       | 34     | 939      | 373832  | 485.21            |
| **total**                                                                         |                                                                  | 56      | 795    | 9664     | 9311376 |                   |

## Vorhandene Daten: [Project Jarāʾid](https://projectjaraid.github.io)

- Bibliographische Metadaten zu allen (3300+) arabischen Periodika bis 1929 (TEI XML)
- Normdaten (TEI XML)

## Netzwerk erwähnter Periodika

<div class="c_width-60 c_left">

![Figure: Network of periodicals mentioned *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab* and *al-Muqtabas*; weights per issue](../assets/networks/network_oape-p3a6afa20_referenced-periodicals-per-issue_circular-n-size_in-degree.svg)

</div>
<div class="c_width-30 c_right">

1. only a few nodes are of relative importance (44 of 465)
2. *al-Muqtabas* accounts for the vast majority of references
3. all periodicals are primarly self-referential
4. confirms the bias on Cairo and Beirut (8 of 9)
2. highly centralised in terms of geographic distribution (10 locations)
3. surprising members

</div>

## Soziales Netzwerk von Autor_innen

<div class="c_width-60 c_left">

![Figure: Network of authors with bylines in *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab* and *al-Muqtabas*](../assets/networks/network_oape-p3a6afa20_authors_unimodal-n-size_out-degree.svg)

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

## Geographisches Netzwerk von Autor_innen

<div class="c_width-50 c_left c_height-50">

![Map: Locations in bylines in *al-Muqtabas* (Cairo and Damascus)](../assets/maps/map-oclc_4770057679-bylines-middle-east.png)

</div><div class="c_width-50 c_right c_height-50">

![Map: Locations in bylines in *al-Ḥaqāʾiq* (Damascus)](../assets/maps/map-oclc_644997575-bylines-middle-east.png)

</div><div class="c_width-50 c_left c_height-50">

![Map: Locations in bylines in *al-Ḥasnāʾ* (Beirut)](../assets/maps/map-oclc_792756327-bylines-middle-east.png)

</div><div class="c_width-50 c_right c_height-50">

![Map: Locations in bylines in *Lughat al-ʿArab* (Baghdad)](../assets/maps/map-oclc_472450345-bylines-middle-east.png)

</div>