---
title: "How did they do it?"
subtitle: "First attempts at tackling the question of authorship with computational methods"
author: Till Grallert
date: 2021-11-13
ORCID: orcid.org/0000-0002-5739-8094
bibliography: /BachUni/research-projects/OpenArabicPE/assets/bibliography/openarabicpe.csl.json
lang: en-GB
---

## outline

- something

## Background
### Computational periodical studies

:::{.c_width-50}

![Directed network of periodicals referenced  in *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab*, and *al-Muqtabas*, weighted by number of issues. Size and colour of nodes: in-degree.](../assets/networks/network_oape-p3a6afa20_referenced-periodicals-per-issue_circular-n-size_in-degree.png){#fig:network-periodicals}

:::
:::{.c_width-50}

![Undirected network of authors in *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab*, and *al-Muqtabas*. Colour of nodes: betweenness centrality; size of nodes: number of periodicals; width of edges: number of articles.](../assets/networks/network_oape-p3a6afa20_authors_unimodal-n-size_out-degree-n-colour_betweenness-e-colour_grey.png){#fig:network-authors}

:::

## The corpus
### Open Arabic Periodical Editions ([OpenArabicPE](https://openarabicpe.github.io), 2015--)

Framework for bootstrapped digital scholarly editions outside the global north

Digital editions based on shadow libraries and digital facsimiles (TEI XML), authority files (TEI XML), Bibliographic metadata on the article level (TEI, MODS, RDF, Zotero)


:::{.c_width-60}

| title                                                                               | volumes    | issues    | articles          | words                        |
| ----------------------------------------------------------------------------------- | ---------: | --------: | ----------:       | ---------:                   |
| [al-Ḥaqāʾiq](https://www.github.com/openarabicpe/digital-haqaiq)                    | 3          | 35        | 389               | 298090                       |
| [al-Ḥasnāʾ](https://www.github.com/openarabicpe/journal_al-hasna)                   | 1          | 12        | 201               | NA                           |
| [al-Manār](https://www.github.com/openarabicpe/journal_al-manar)                    | 20         | 387       |                   |                              |
| [al-Muqtabas](https://www.github.com/tillgrallert/digital-muqtabas)                 | 9          | 96        | 2964              | 1981081                      |
| [al-Ustādh](https://www.github.com/openarabicpe/journal_al-ustadh)                  | 1          | 42        | 435               | 221447                       |
| [al-Zuhūr](https://www.github.com/openarabicpe/journal_al-zuhur)                    | 4          | 39        | 436               | 292333                       |
| [Lughat al-ʿArab](https://www.github.com/openarabicpe/journal_lughat-al-arab)       | 3          | 34        | 939               | 373832                       |
| **total**                                                                           | 41         | 645       | 5364<!-- 9664 --> | c. 6 million<!-- 9311376 --> |

Table: The OpenArabicPE corpus until 1918 {#tbl:openarabicpe-corpus}

:::
:::{.c_width-30}

![[Webview of *al-Muqtabas* 6(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png){#fig:webview-muqtabas}

:::

## stylistic differences between journals

:::{.c_width-50}

- *Lughat al-ʿArab* and *al-Muqtabas* are indistinguishable
- *al-Ḥaqāʾiq* is different

![PCA covariance matrix for the 100 MFWs in a corpus of ... issues of *al-Ḥaqāʾiq*, *Lughat al-ʿArab*, and *al-Muqtabas* ](/BachUni/BachBibliothek/GitHub/Sihafa/sihafa_stylometry/data/2021-10-19/issues/composite/comb_muqtabas-haqaiq-lughat_PCA_100_MFWs_Culled_0__PCA__001.png)

:::
:::{.c_width-50}

- some issues of *al-Muqtabas* are clearly different

![PCA covariance matrix for the 900 MFWs in a corpus of ... issues of *al-Ḥaqāʾiq*, *Lughat al-ʿArab*, and *al-Muqtabas* ](/BachUni/BachBibliothek/GitHub/Sihafa/sihafa_stylometry/data/2021-10-19/issues/composite/comb_muqtabas-haqaiq-lughat_PCA_900_MFWs_Culled_0__PCA__001.png)

:::

## stylistic differences between journals

:::{.c_width-50}

![PCA covariance matrix for the 100 MFWs in a corpus of ... issues of *Lughat al-ʿArab*, *al-Muqtabas*, and *al-Zuhūr* ](/BachUni/BachBibliothek/GitHub/Sihafa/sihafa_stylometry/data/2021-10-19/issues/composite/comb_muqtabas-lughat-zuhur_PCA_100_MFWs_Culled_0__PCA__001.png)

:::
:::{.c_width-50}

![PCA covariance matrix for the 900 MFWs in a corpus of ... issues of *Lughat al-ʿArab*, *al-Muqtabas*, and *al-Zuhūr* ](/BachUni/BachBibliothek/GitHub/Sihafa/sihafa_stylometry/data/2021-10-19/issues/composite/comb_muqtabas-lughat-zuhur_PCA_900_MFWs_Culled_0__PCA__001.png)

:::