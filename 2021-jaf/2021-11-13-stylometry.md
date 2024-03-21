---
title: "How did they do it?"
subtitle: "First attempts at tackling the question of authorship with computational methods"
author: Till Grallert
date: 2021-11-13
ORCID: orcid.org/0000-0002-5739-8094
bibliography: /BachUni/research-projects/OpenArabicPE/assets/bibliography/openarabicpe.csl.json
lang: en-GB
---

## How did they do it? <br/>First attempts at tackling the question of authorship with computational methods


Till Grallert, Humboldt-Universität zu Berlin, @[tillgrallert](https://twitter.com/tillgrallert)

Workshop "Journal as Form", 11--13 November 2021

Slides: [https://openarabicpe.github.io/slides/2021-jaf](https://tillgrallert.github.io/slides/dh/2021-mind-the-gap/index.html)


## Background
### Computational periodical studies (c.1800--c.1920)

::: columns
:::: column

![Undirected network of authors in *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab*, and *al-Muqtabas*. Colour of nodes: betweenness centrality; size of nodes: number of periodicals; width of edges: number of articles.](../assets/networks/network_oape-p3a6afa20_authors_unimodal-n-size_out-degree-n-colour_betweenness-e-colour_grey.png){#fig:network-authors}

::::
:::: column

![Heat map of locations mentioned in bylines in *al-Ḥaqāʾiq* (Damascus)](../assets/maps/map-oclc_644997575-bylines-ME.png){#fig:authors-haqaiq .c_height-50}

![Heat map of locations mentioned in bylines in  *al-Muqtabas* (Cairo and Damascus)](../assets/maps/map-oclc_4770057679-bylines-ME.png){#fig:authors-muqtabas .c_height-50}

::::
:::

## Background
### necessary digital data

::: columns
:::: column

- structured bibliographic (meta)data for each article
	+ i.e. "*Sātisnā* sent this article from *al-Shahbāʾ*"
	+ (semi)automatic extraction depends on: 
		* it being present in the material artefact
		* a modelled digital substitute
	+ problems
		* status of OCR and layout-detection
		* plurality of name forms, initials, etc.

::::
:::: column

- authority data for disambiguation and enriching the data
	+ i.e. 
		* *Sātisnā* is a pen name for *Anastās al-Karmilī*, publisher of *Lughat al-ʿArab*
		* *al-Shahbāʾ* is a name for Aleppo, located at `36.20124, 37.16117`
	+ problems
		* authority files are biased towards the Global North

::::
:::

## The corpus
### Open Arabic Periodical Editions ([OpenArabicPE](https://openarabicpe.github.io), 2015--)

Framework for bootstrapped digital scholarly editions outside the global north

Digital editions based on shadow libraries and digital facsimiles (TEI XML), authority files (TEI XML), Bibliographic metadata on the article level (TEI, MODS, RDF, Zotero)


:::{.c_width-60}

| title                                                                               | volumes    | issues    | articles          | words                        |
| ----------------------------------------------------------------------------------- | ---------: | --------: | ----------:       | ---------:                   |
| [al-Ḥaqāʾiq](https://www.github.com/openarabicpe/journal_al-haqaiq)                    | 3          | 35        | 389               | 298090                       |
| [al-Ḥasnāʾ](https://www.github.com/openarabicpe/journal_al-hasna)                   | 1          | 12        | 201               | NA                           |
| [al-Manār](https://www.github.com/openarabicpe/journal_al-manar)                    | 20         | 387       |                   |                              |
| [al-Muqtabas](https://www.github.com/openarabicpe/journal_al-muqtabas)                 | 9          | 96        | 2964              | 1981081                      |
| [al-Ustādh](https://www.github.com/openarabicpe/journal_al-ustadh)                  | 1          | 42        | 435               | 221447                       |
| [al-Zuhūr](https://www.github.com/openarabicpe/journal_al-zuhur)                    | 4          | 39        | 436               | 292333                       |
| [Lughat al-ʿArab](https://www.github.com/openarabicpe/journal_lughat-al-arab)       | 3          | 34        | 939               | 373832                       |
| **total**                                                                           | 41         | 645       | 5364<!-- 9664 --> | c. 6 million<!-- 9311376 --> |

Table: The OpenArabicPE corpus until 1918 {#tbl:openarabicpe-corpus}

:::
:::{.c_width-30}

![[Webview of *al-Muqtabas* 6(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png){#fig:webview-muqtabas}

:::

# The elefant in the room
## missing bylines

- 80% of all articles or 66% of all words carry no byline
- problems:
	1. commonly ignored 
	2. implicit hypothesis is implausible and untested

## stylometric authorship attribution

::: columns
:::: column

### comparative method

+ empirically validated
+ comparison of "style" (*most frequent words*, MFW)
+ nummeric measures of difference (*delta*)
+ self-validation through voting (*consensus*) of multiple iterations

::::
:::: column

### challenges

- first application to Arabic
- comparison dependent on input
- reliability depends on a minimal length of texts

::::
:::

## stylistic differences between journals
### *al-Ḥaqāʾiq*, *Lughat al-ʿArab*, and *al-Muqtabas*

:::{.c_width-30}

![PCA covariance matrix for the 100 MFWs in a corpus of ... issues of *al-Ḥaqāʾiq*, *Lughat al-ʿArab*, and *al-Muqtabas* ](../assets/stylometry/comb_muqtabas-haqaiq-lughat_PCA_100_MFWs_Culled_0__PCA__001.png){#fig:pca-halumu-100}

:::
:::{.c_width-30}

- *Lughat al-ʿArab* and *al-Muqtabas* are indistinguishable
- *al-Ḥaqāʾiq* is different
- some issues of *al-Muqtabas* are very different

:::
:::{.c_width-30}

![PCA covariance matrix for the 900 MFWs in a corpus of ... issues of *al-Ḥaqāʾiq*, *Lughat al-ʿArab*, and *al-Muqtabas* ](../assets/stylometry/comb_muqtabas-haqaiq-lughat_PCA_900_MFWs_Culled_0__PCA__001.png){#fig:pca-halumu-900}

:::

## stylistic differences between journals
### *Lughat al-ʿArab*, *al-Muqtabas*, and *al-Zuhūr*

:::{.c_width-30}

![PCA covariance matrix for the 100 MFWs in a corpus of ... issues of *Lughat al-ʿArab*, *al-Muqtabas*, and *al-Zuhūr*](../assets/stylometry/comb_muqtabas-lughat-zuhur_PCA_100_MFWs_Culled_0__PCA__001.png){#fig:pca-lumuzu-100}

:::
:::{.c_width-30}

- Strong stylistic similarities between all three periodicals
- some issues of *al-Muqtabas* are very different

:::
:::{.c_width-30}

![PCA covariance matrix for the 900 MFWs in a corpus of ... issues of *Lughat al-ʿArab*, *al-Muqtabas*, and *al-Zuhūr*](../assets/stylometry/comb_muqtabas-lughat-zuhur_PCA_900_MFWs_Culled_0__PCA__001.png){#fig:pca-lumuzu-900}

:::

## authorship signal
### al-Muqtabas

:::{.c_width-60 .c_left}

![Bootstrap consensus network of articles in *al-Muqtabas* (size >= 5000 words, 100--1000 MFWs). Colour indicates *modularity group*](../assets/stylometry/stylo_oape-p3a6afa20_articles-w_5000-modularity_1-label_authors.png){#fig:stylometry-muqtabas-w5000}

:::
:::{.c_width-30}

- reliable signals for
    + authorship
    + translation
    + editing
- additional (sub) signal for
    + genre
- authorship question:
	+ there is at least another, unknown, contributor in addition to Muḥammad Kurd ʿAlī
:::



## authorship signal
### Lughat al-ʿArab

:::{.c_width-60 .c_left}

![Bootstrap consensus network of sections in *Lughat al-ʿArab* (> 5000 words), articles by Anastās Mārī al-Karmilī and Kāẓim al-Dujaylī, the title's known editors, and by Muḥammad Kurd ʿAlī as an unlikely control author (size >= 5000 words, 100--1000 MFWs). Colour indicates *modularity group*](../assets/stylometry/stylo-lughat-al-arab_sections-w_5000-modularity_1-label_author-id-annotated.png)

:::
:::{.c_width-30}


+ Kāẓim al-Dujaylī is likely the author of sections
+ Anastās Mārī al-Karmilī seemingly did not contribute much to his own journal

:::

## Thank you!

- Contributors to OpenArabicPE: Jasper Bernhofer, Dimitar Dragnev, Patrick Funk, Talha Güzel, Hans Magne Jaatun, Jakob Koppermann, Xaver Kretzschmar, Daniel Lloyd, Klara Mayer, Tobias Sick, Manzi Tanna-Händel, and Layla Youssef
- Links:
    + Slides: [https://OpenArabicPE.github.io/slides/2021-jaf/](https://OpenArabicPE.github.io/slides/2021-jaf/index.html)
    + Paper: <https://doi.org/10/gkhrjr>
    + Project URLs: [https://www.github.com/OpenArabicPE](https://www.github.com/OpenArabicPE)
    + Project blog: [https://openarabicpe.github.io](https://openarabicpe.github.io)
    + Twitter: \@[tillgrallert](https://twitter.com/tillgrallert)
    + Email: <till.grallert@fu-berlin.de>
- Licence: slides and images are licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)
