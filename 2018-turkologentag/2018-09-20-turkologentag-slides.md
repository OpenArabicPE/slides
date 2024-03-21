---
title: "Catch me if you can!"
author: Till Grallert
date: 2018-09-18 13:49:53 +0200
duration: 20
tags:
- presentation
- OpenArabicPE
---

## Catch me if you can! Attempts to track networks of authors and publication reviews in the wasteland of 'digitised' Arabic periodicals from the Ottoman Empire

Till Grallert, Orient-Institut Beirut (OIB)

Turkologentag 2018, Bamberg

Slides: [https://OpenArabicPE.github.io/slides/2018-turkologentag/](https://OpenArabicPE.github.io/slides/2018-turkologentag/index.html)

## Outline of today's paper

1. Introduction: the promised wasteland of *digitised* Arabic periodicals
2. OpenArabicPE: making truly *digital* editions
3. First attempts to map the late Ottoman ideosphere of *Bilād al-Shām*

# 1. Introduction: the promised wasteland of *digitised* Arabic periodicals
## 1.1 Importance of mundane texts / periodicals

<!-- add core questions of today's presentation  -->

- They are at the core of various discourses
    + Modernity / -ism at the end of empire
    + Arabic renaissance
    + Arab nationalism
    + Islamic reform movement
- They form large corpora with an equal distribution along a temporal axis (*al-Muqtabas*: 12 yrs, *al-Manār*: 43 yrs, *al-Muqtaṭaf*: 76 yrs)
    + linguistic analysis
    + historical semantics
    + rich data sets for social history

## 1.2 A two-fold problem

- Preservation:
    + Active destruction of cultural artifacts: iconoclasm, neoliberalism
    + Neglect: fragile materiality
- Access:
    + Absence / destruction of infrastructure / channels of knowledge transmission: lack of access to institutions, hardware, software, internet connections
    + widely-dispersed collections
    + technologies: absence of reliable OCR
    <!-- + technical skills: lack of basic scripting skills -->

## 1.3 Digitisation as solution

1. Promise: instant **access** to 100s of **digitised** periodicals and 100.000s of issues
2. Expectations: answers to core questions
    - extent of text re-use
    - identify authors
    - track authors across periodicals
2. Reality
    - limited access
    - limited data
    - limited metadata

<!-- elaborate the problems:

1. get the data:
    - text:
        - OCR and HTR are still dysfunctional
        - require ground truth and extensive training
    - bibliographic metadata
2. turn the data into a human and machine readable edition
    - model the source
    - identify entities and link them to authority files -->

## 1.3.2 state of digitisation: facsimiles

Digital imagery, e.g. [Endangered Archives Programme (EAP)](http://eap.bl.uk/database/overview_project.a4d?projID=EAP119;r=63), [HathiTrust](http://catalog.hathitrust.org/Record/100658549)

+ lack of metadata
+ limited licences, pay walls
+ no or very bad text layers

## 1.3.2 state of digitisation: facsimiles

![[*al-Muqtabas* 6 on EAP](http://eap.bl.uk/database/overview_item.a4d?catId=810;r=288)](../assets/eap119-1-4-5-muqtabas-annotated.png)

## 1.3.2 state of digitisation: facsimiles

![[*al-Muqtabas* 6 on HathiTrust without US IP](http://hdl.handle.net/2027/njp.32101073250910)](../assets/hathi_muqtabas-1.png)

## 1.3.2 state of digitisation: facsimiles

![[*al-Muqtabas* 6 on HathiTrust with US IP](http://hdl.handle.net/2027/njp.32101073250910)](../assets/hathi_muqtabas-2.png)

## 1.3.2 state of digitisation: facsimiles

![[*al-Muqtabas* 6 on HathiTrust, state of OCR (only visible to US IPs)](http://hdl.handle.net/2027/njp.32101073250910)](../assets/hathi_muqtabas-ocr-2.png)

## 1.3.1 state of digitisation: text

"crowd"-sourced transcriptions / gray online libraries, e.g. [*al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523), [*Mishkāt*](http://almeshkat.net/), [*Ṣayd al-Fawāʾid*](http://saaid.net/), [*al-Waraq*](http://www.alwaraq.net/) etc.

+ lack of / faulty metadata
+ unknown editing principles
+ unknown quality
+ very limited structural mark-up
+ cannot be reliably cited

## 1.3.1 state of digitisation: text

<!-- ![[*al-Muqtabas* on *al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523)](../assets/shamela_muqtabas-1.png) -->

![[*al-Muqtabas* on *al-Maktaba al-Shāmila*](http://shamela.ws/browse.php/book-26523#page-4046)](../assets/shamela_muqtabas-annotated.png)


## 1.3.3 state of digitisation: bibliographic metadata

- needs:
    + reliable bibliographic metadata on the article level and
    + across periodicals
- reality: no platform provides machine-actionable bibliographic metadata below the item level

# 2. [OpenArabicPE](https://github.com/openarabicpe): making truly *digital* editions
## 2.1 Aims and principles

1. idea: unite available facsimiles and transcriptions
2. aims
    + **validate** the transcription against the facsimiles
    - **improve** the transcription with the help of the "crowd"
    - make everything **citable** for scholars, **linkable** for machines
    - provide the new edition with the **open licence** to facilitate access and re-use
3. principles
    - re-purpose **available** and **established** tools, technologies, and material
    - preference for **open** and **simple** formats and tools

## 2.2 Deliverables: basic components

1. XML/TEI editions with their own [schema for Arabic periodicals](https://github.com/OpenArabicPE/OpenArabicPE_ODD)
    + text links to open-access digital facsimiles
    + licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)
2. Structured bibliographic metadata (MODS, BibTeX)
3. Tools to
    + scrape full text / bibliographic information from the web
    + convert scraped information into TEI, MODS, BibTeX
    + improve the TEI mark-up

## 2.2 Deliverables: Core features

1. Social digital edition hosted on [GitHub](https://github.com): gradually improve transcription and mark-up
2. Releases are archived at [Zenodo](https://zenodo.org): receive a DOI for reliable citation
3. [Static web-view](https://github.com/tillgrallert/tei-boilerplate-arabic-editions)<!--  (doesn't require a permanent internet connection) -->: provides side-by-side view of facsimiles and text
4. Access to bibliographic metadata through a public [Zotero group](https://www.zotero.org/groups/openarabicpe)

<!-- mention: process of cleaning data and disambiguation of entities -->

![[Display of *al-Muqtabas* 6(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png)

## 2.3 Project scheme

![](../assets/OpenArabicPE-organigramme_horizontal.png)

# 3. First attempts to map the late Ottoman ideosphere of *Bilād al-Shām*
## networks of authors: available data

<div class="c_width-50">

### *al-Muqtabas*, 1906--1917/18

|         token          |   total   |  author |     NA    |
|------------------------|-----------|---------|-----------|
| volumes                | 9         |         |           |
| issues                 | 96        |         |           |
| pages                  | c.7,000   |         |           |
| articles (total)       | 2,737     | 323     | 2,414     |
| articles (independent) | 717       | 284     | 433       |
| words                  | 1,953,952 | 625,333 | 1,328,619 |

</div>
<div class="c_width-50">

### *al-Ḥaqāʾiq*, 1910--1913/14

|  token   |  total  | author |    NA   |
|----------|---------|--------|---------|
| volumes  | 3       |        |         |
| issues   | 36      |        |         |
| pages    | 1,446   |        |         |
| articles | 360     | 76     | 284     |
| words    | 300,186 | 40,868 | 259,318 |

</div>

## networks of authors: quality of data

- data source: bylines and comments in the text
    + many accronyms
    + plurality of name forms
- manual mark-up: authors and locations
- manual disambiguation: links to authority files (*semantic web*)
- automatic enriching: from semantic web
    + life dates
    + works
    + geocoded locations

## *al-Muqtabas*: authors by number of bylines

| rank |                     author.id                      |                                    author.name                                    | author.birth | articles | word.count |
|------|----------------------------------------------------|-----------------------------------------------------------------------------------|--------------|----------|------------|
|    1 | [viaf:14924300](https://viaf.org/viaf/14924300/)   | [معروف الرصافي](https://en.wikipedia.org/wiki/Maarouf_Al_Rasafi)                  |         1875 |       24 |      12437 |
|    2 | [viaf:40250618](https://viaf.org/viaf/40250618/)   | [عيسى أفندي اسكندر المعلوف](https://ar.wikipedia.org/wiki/عيسى_إسكندر_المعلوف)    |         1869 |       20 |      23297 |
|    3 | [viaf:39370998](https://viaf.org/viaf/39370998/)   | [ساتسنا (بطرس بن جبرائيل عواد)](https://en.wikipedia.org/wiki/Anastas_Al-Karmali) |         1866 |       14 |      19849 |
|    4 |                                                    | يوسف جرجس زخم                                                                     |              |       13 |      21613 |
|    5 | [viaf:93607460](https://viaf.org/viaf/93607460/)   | [جمال الدين القاسمي](https://ar.wikipedia.org/wiki/جمال_الدين_القاسمي)            |         1866 |        8 |      38541 |
|    6 | [viaf:118432135](https://viaf.org/viaf/118432135/) | [عبد القادر أفندي المغربي](https://ar.wikipedia.org/wiki/عبد_القادر_المغربي)      |         1867 |        7 |      14074 |
|    7 | [viaf:19737865](https://viaf.org/viaf/19737865/)   | [أحمد بك تيمور](https://en.wikipedia.org/wiki/Ahmed_Taymour)                      |         1871 |        7 |       7905 |
|    8 | [viaf:22006374](https://viaf.org/viaf/22006374/)   | [محمد رضا الشبيبي](https://en.wikipedia.org/wiki/Mohammed_Ridha_Al-Shabibi)       |         1889 |        7 |      17894 |
|    9 | [viaf:28125663](https://viaf.org/viaf/28125663/)   | [رفيق بك العظم](https://ar.wikipedia.org/wiki/رفيق_العظم)                         |         1865 |        7 |      13237 |
|   10 | [viaf:32272677](https://viaf.org/viaf/32272677/)   | [محمد كرد علي](https://en.wikipedia.org/wiki/Muhammad_Kurd_Ali)                   |         1876 |        7 |      42489 |
|   11 | [viaf:49218655](https://viaf.org/viaf/49218655/)   | [أحمد بك زكي](https://en.wikipedia.org/wiki/Ahmad_Zaki_Pasha)                     |         1866 |        7 |      40311 |

<!-- ## *al-Muqtabas*: authors by number of bylines

| rank |            name           | words | articles |
|------|---------------------------|-------|----------|
|    1 | Maʿrūf al-Ruṣāfī          | 12437 |       24 |
|    2 | ʿĪsā Iskandar al-Maʿlūf   | 23297 |       20 |
|    3 | Sātsunā                   | 19849 |       14 |
|    4 | Yūsuf Jirjis Zakham       | 21613 |       13 |
|    5 | Jamāl al-Dīn al-Qāsimī    | 38541 |        8 |
|    6 | Muḥammad Kurd ʿAlī        | 42489 |        7 |
|    7 | Aḥmad Zakī                | 40311 |        7 |
|    8 | Muḥammad Riḍā al-Shabībī  | 17894 |        7 |
|    9 | ʿAbd al-Qādir al-Maghribī | 14074 |        7 |
|   10 | Rafīq al-ʿAẓm             | 13237 |        7 |
|   11 | Aḥmad Taymūr              |  7905 |        7 | -->

## *al-Muqtabas*: authors by number of bylines

![Figure: Word cloud of authors published in *al-Muqtabas*; by number of articles](../assets/plots/word-cloud_muqtabas-authors-bylines.png)

## *al-Ḥaqāʾiq*: authors by number of bylines

| rank |                     author.id                      |       author.name        | author.birth | articles | word.count |
|------|----------------------------------------------------|--------------------------|--------------|----------|------------|
|    1 | [viaf:299025643](https://viaf.org/viaf/299025643/) | محمد عارف المنير الحسيني | 1847/48      |        4 |       3134 |
|    2 |                                                    | ع                        |              |        3 |       2833 |
|    3 |                                                    | عبد الرحمن القصار        |              |        3 |        628 |
|    4 | [viaf:267054449](https://viaf.org/viaf/267054449/) | مختار المؤيد             | 1822         |        3 |        820 |
|    5 | [viaf:17087051](https://viaf.org/viaf/17087051/)   | محمد أبو الخير الطباع    |              |        2 |       2887 |
|    6 |                                                    | محمد القاسمي الحلاق      |              |        2 |       3619 |
|    7 |                                                    | محي الدين الخاني         |              |        2 |         74 |

## *al-Ḥaqāʾiq*: authors by number of bylines

![Figure: Word cloud of authors published in *al-Ḥaqāʾiq*](../assets/plots/word-cloud_haqaiq-authors-bylines.png)

## Worlds apart: *al-Muqtabas* and *al-Ḥaqāʾiq*

![Figure: Authors and periodicals](../assets/plots/network_openarabicpe-authors-publications.png)

## *al-Muqtabas*: locations by number of bylines

![Figure: Locations in bylines in *al-Muqtabas*](../assets/maps/map_muqtabas-bylines-me.png)

## *al-Ḥaqāʾiq*: locations by number of bylines

![Figure: Locations in bylines in *al-Ḥaqāʾiq*](../assets/maps/map_haqaiq-bylines-me.png)

## stylometry

- aim: authorship attribution through comparison
- how:
    + **computation** of frequency tables for each article
    + **comparison** of each frequency table with every other
    + **ranking** of pairs of texts according to similarity of frequency tables
- limits: cannot establish author names beyond the corpus

## *al-Muqtabas*: 1000 MFWs, *Jamāl al-Dīn al-Qāsimī*

|                    source                   |                    target                   | weight |    type    |
|---------------------------------------------|---------------------------------------------|--------|------------|
| القاسمي-oclc_4770057679-i_61-div_2.d1e1517  | القاسمي-oclc_4770057679-i_62-div_2.d1e1491  |     54 | undirected |
| القاسمي-oclc_4770057679-i_62-div_2.d1e1491  | القاسمي-oclc_4770057679-i_61-div_2.d1e1517  |     54 | undirected |
| القاسمي-oclc_4770057679-i_61-div_2.d1e1517  | القاسمي-oclc_4770057679-i_63-div_7.d1e1810  |     52 | undirected |
| القاسمي-oclc_4770057679-i_63-div_7.d1e1810  | القاسمي-oclc_4770057679-i_61-div_2.d1e1517  |     52 | undirected |
| القاسمي-oclc_4770057679-i_49-div_2.d1e1499  | NN-oclc_4770057679-i_48-div_4.d1e1914       |     45 | undirected |
| القاسمي-oclc_4770057679-i_62-div_2.d1e1491  | القاسمي-oclc_4770057679-i_63-div_7.d1e1810  |     44 | undirected |
| القاسمي-oclc_4770057679-i_63-div_7.d1e1810  | القاسمي-oclc_4770057679-i_62-div_2.d1e1491  |     44 | undirected |
| القاسمي-oclc_4770057679-i_52-div_10.d1e2681 | القاسمي-oclc_4770057679-i_53-div_3.d1e3775  |     42 | undirected |
| القاسمي-oclc_4770057679-i_53-div_3.d1e3775  | القاسمي-oclc_4770057679-i_52-div_10.d1e2681 |     42 | undirected |
| القاسمي-oclc_4770057679-i_50-div_4.d1e2033  | القاسمي-oclc_4770057679-i_63-div_7.d1e1810  |     38 | undirected |
| القاسمي-oclc_4770057679-i_63-div_7.d1e1810  | القاسمي-oclc_4770057679-i_50-div_4.d1e2033  |     38 | undirected |
| القاسمي-oclc_4770057679-i_49-div_2.d1e1499  | NN-oclc_4770057679-i_47-div_2.d1e1470       |     31 | undirected |
| القاسمي-oclc_4770057679-i_55-div_23.d1e4814 | NN-oclc_4770057679-i_2-div_21.d1e2160       |     24 | undirected |
| القاسمي-oclc_4770057679-i_49-div_2.d1e1499  | NN-oclc_4770057679-i_87-div_3.d1e696        |     24 | undirected |
| القاسمي-oclc_4770057679-i_50-div_4.d1e2033  | NN-oclc_4770057679-i_64-div_2.d1e1188       |     24 | undirected |
| القاسمي-oclc_4770057679-i_63-div_7.d1e1810  | NN-oclc_4770057679-i_15-div_3.d1e696        |     18 | undirected |
| القاسمي-oclc_4770057679-i_49-div_2.d1e1499  | NN-oclc_4770057679-i_19-div_9.d1e2206       |     17 | undirected |
| القاسمي-oclc_4770057679-i_55-div_23.d1e4814 | NN-oclc_4770057679-i_3-div_18.d1e1764       |     16 | undirected |
| القاسمي-oclc_4770057679-i_61-div_2.d1e1517  | NN-oclc_4770057679-i_33-div_3.d1e696        |     16 | undirected |
| القاسمي-oclc_4770057679-i_39-div_7.d1e2166  | عنحوري-oclc_4770057679-i_54-div_2.d1e1300   |     15 | undirected |

## *al-Muqtabas*: 1000 MFWs, *Maʿrūf al-Ruṣāfī*

|                    source                   |                 target                 | weight |    type    |
|---------------------------------------------|----------------------------------------|--------|------------|
| الرصافي-oclc_4770057679-i_10-div_9.d1e1418  | NN-oclc_4770057679-i_94-div_11.d1e5944 |     27 | undirected |
| الرصافي-oclc_4770057679-i_24-div_9.d1e1716  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     27 | undirected |
| الرصافي-oclc_4770057679-i_36-div_5.d2e3004  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     27 | undirected |
| الرصافي-oclc_4770057679-i_20-div_6.d1e1588  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     26 | undirected |
| الرصافي-oclc_4770057679-i_19-div_6.d1e1081  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     25 | undirected |
| الرصافي-oclc_4770057679-i_28-div_25.d1e3388 | NN-oclc_4770057679-i_2-div_21.d1e2160  |     25 | undirected |
| الرصافي-oclc_4770057679-i_37-div_7.d1e1907  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     25 | undirected |
| الرصافي-oclc_4770057679-i_40-div_14.d1e2780 | NN-oclc_4770057679-i_94-div_11.d1e5944 |     25 | undirected |
| الرصافي-oclc_4770057679-i_13-div_9.d1e1285  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     24 | undirected |
| الرصافي-oclc_4770057679-i_14-div_7.d1e1428  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     24 | undirected |
| الرصافي-oclc_4770057679-i_22-div_9.d1e1772  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     24 | undirected |
| الرصافي-oclc_4770057679-i_31-div_10.d1e2096 | NN-oclc_4770057679-i_2-div_21.d1e2160  |     24 | undirected |
| الرصافي-oclc_4770057679-i_39-div_5.d1e1387  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     24 | undirected |
| الرصافي-oclc_4770057679-i_41-div_7.d1e3728  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     24 | undirected |
| الرصافي-oclc_4770057679-i_25-div_11.d1e2206 | NN-oclc_4770057679-i_2-div_21.d1e2160  |     23 | undirected |
| الرصافي-oclc_4770057679-i_29-div_6.d1e1333  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     23 | undirected |
| الرصافي-oclc_4770057679-i_40-div_4.d1e832   | NN-oclc_4770057679-i_2-div_21.d1e2160  |     21 | undirected |
| الرصافي-oclc_4770057679-i_33-div_5.d1e1329  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     20 | undirected |
| الرصافي-oclc_4770057679-i_35-div_3.d1e696   | NN-oclc_4770057679-i_2-div_21.d1e2160  |     20 | undirected |
| الرصافي-oclc_4770057679-i_68-div_9.d1e4370  | NN-oclc_4770057679-i_2-div_21.d1e2160  |     20 | undirected |

## *al-Muqtabas*: 1000 MFWs, *ʿĪsā Iskandar al-Maʿlūf*

|                    source                   |                   target                   | weight | type           |
|---------------------------------------------|--------------------------------------------|--------|------------|
| المعلوف-oclc_4770057679-i_53-div_2.d1e1568  | NN-oclc_4770057679-i_64-div_3.d1e2089      |     47 | undirected |
| المعلوف-oclc_4770057679-i_53-div_2.d1e1568  | NN-oclc_4770057679-i_35-div_6.d1e2205      |     32 | undirected |
| المعلوف-oclc_4770057679-i_37-div_10.d1e3397 | NN-oclc_4770057679-i_2-div_21.d1e2160      |     27 | undirected |
| المعلوف-oclc_4770057679-i_42-div_9.d1e1281  | NN-oclc_4770057679-i_23-div_25.d1e2996     |     26 | undirected |
| المعلوف-oclc_4770057679-i_53-div_2.d1e1568  | NN-oclc_4770057679-i_56-div_2.d1e1398      |     26 | undirected |
| المعلوف-oclc_4770057679-i_55-div_10.d1e2970 | NN-oclc_4770057679-i_2-div_21.d1e2160      |     26 | undirected |
| المعلوف-oclc_4770057679-i_93-div_8.d1e1268  | NN-oclc_4770057679-i_2-div_21.d1e2160      |     26 | undirected |
| المعلوف-oclc_4770057679-i_54-div_5.d1e1854  | NN-oclc_4770057679-i_2-div_21.d1e2160      |     25 | undirected |
| المعلوف-oclc_4770057679-i_94-div_11.d1e6080 | NN-oclc_4770057679-i_2-div_21.d1e2160      |     25 | undirected |
| المعلوف-oclc_4770057679-i_95-div_51.d1e3324 | NN-oclc_4770057679-i_2-div_21.d1e2160      |     25 | undirected |
| المعلوف-oclc_4770057679-i_44-div_6.d1e1798  | NN-oclc_4770057679-i_2-div_21.d1e2160      |     24 | undirected |
| المعلوف-oclc_4770057679-i_45-div_8.d1e2304  | NN-oclc_4770057679-i_2-div_21.d1e2160      |     24 | undirected |
| المعلوف-oclc_4770057679-i_47-div_6.d1e2816  | NN-oclc_4770057679-i_2-div_21.d1e2160      |     24 | undirected |
| المعلوف-oclc_4770057679-i_55-div_22.d1e4313 | NN-oclc_4770057679-i_2-div_21.d1e2160      |     24 | undirected |
| المعلوف-oclc_4770057679-i_93-div_7.d1e1147  | NN-oclc_4770057679-i_2-div_21.d1e2160      |     24 | undirected |
| المعلوف-oclc_4770057679-i_53-div_33.d1e6920 | NN-oclc_4770057679-i_2-div_21.d1e2160      |     23 | undirected |
| المعلوف-oclc_4770057679-i_63-div_30.d1e2971 | NN-oclc_4770057679-i_2-div_21.d1e2160      |     21 | undirected |

## *al-Muqtabas*: origin of referenced works

![Figure: Origin of referenced works in *al-Muqtabas*](../assets/maps/map_muqtabas-referenced-works-all.png)


# Conclusion
## Summary

- **digitised** periodicals are not **digital** periodicals
- machine-guided analysis depends on the **quality of (meta) data**
<!-- - the better and more homogeneously structured the data, the more applications of machine-guided analysis -->
- digital data and editions require a lot of **manual work**
- tools and formats are grounded in the **Western episteme**

## Thank you!

- Contributors to OpenArabicPE: Dimitar Dragnev, Talha Güzel, Xaver Kretzschmar, Daniel Lloyd, Klara Mayer, Manzi Tanna-Händel and Layla Youssef
- Links:
    + Slides: [https://OpenArabicPE.github.io/slides/2018-turkologentag/](https://OpenArabicPE.github.io/slides/2018-turkologentag/index.html)
    + Paper (draft): <https://doi.org/10.5281/zenodo.1413610>
    + Project URLs: [https://www.github.com/OpenArabicPE](https://www.github.com/OpenArabicPE), [https://www.github.com/openarabicpe/journal_al-muqtabas](https://www.github.com/openarabicpe/journal_al-muqtabas), [https://www.github.com/openarabicpe/journal_al-haqaiq](https://www.github.com/openarabicpe/journal_al-haqaiq)
    + Project blog: [https://openarabicpe.github.io](https://openarabicpe.github.io)
    + Twitter: @[tillgrallert](https://twitter.com/tillgrallert)
    + Email: <grallert@orient-institut.org> <till.grallert@fu-berlin.de>
- Licence: slides and plots are licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)