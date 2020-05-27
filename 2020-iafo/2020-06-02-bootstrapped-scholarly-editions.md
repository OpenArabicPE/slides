---
title: "Open Arabic Periodical Editions (OpenArabicPE)"
author: Till Grallert
date: 2020-06-02
duration: 20
---

<!-- To do -->
<!-- - comments on collaborations -->


## Open Arabic Periodical Editions: a framework for bootstrapped scholarly editions outside the Global North

Till Grallert, Orient-Institut Beirut (OIB), @[tillgrallert](https://twitter.com/tillgrallert)

Journée d’études 'L’interopérabilité des données de la recherche: textes, images, bases de données', IFAO, 2 June 2020

Slides: [https://OpenArabicPE.github.io/slides/2020-ifao/](https://OpenArabicPE.github.io/slides/2020-ifao/index.html)

## Outline of today's paper

1. Problem: The promised wasteland of *digitised* Arabic periodicals
2. Idea: Bootstrapping digital scholarly editions
3. Implementation: Open Arabic Periodical Editions

# 1. The promised wasteland of *digitised* Arabic periodicals
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

1. Preservation:
    + Active **destruction** of cultural artefacts: iconoclasm, neoliberalism
    + **Decay** through neglect: fragile materiality
2. Access:
    + Absence / destruction of infrastructure / channels of knowledge transmission: lack of access to institutions, hardware, software, internet connections
    + widely-dispersed collections
    + absence of technologies: OCR
    <!-- + technical skills: lack of basic scripting skills -->

## 1.2 A two-fold problem

![Map: geographic distribution of library holdings of *al-Muqtabas*](../assets/maps/map-oclc_4770057679-holdings-vol_1-9.png)

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

## 1.3 Digitisation as problem(s)
<!-- elaborate the problems:-->

It's **labour and resource intensive**. It really is!

1. get the data
    - text: transcription, train OCR/HTR
    - facsimiles: scanning
    - bibliographic metadata: transcription, validated iterative generation
2. transform the data into a human and machine readable edition
    - model the source
    - identify entities and link them to authority files
3. host, share and preserve the data

## 1.3 Digitisation as problem(s)

![Global [map of DH centers](http://dhcenternet.org/centers)](../assets/maps/map_dhcenters.png)

# 1.4 State of digitisation
## 1.4.1 state of digitisation: text

- "crowd"-sourced transcriptions / gray online libraries, e.g. [*al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523), [*Mishkāt*](http://almeshkat.net/), [*Ṣayd al-Fawāʾid*](http://saaid.net/), [*al-Waraq*](http://www.alwaraq.net/) etc.
    + lack of / faulty metadata
    + unknown editing principles
    + unknown quality
    + very limited structural mark-up
    + cannot be reliably cited
- Automated transcriptions (OCR): [HathiTrust](https://www.hathitrust.org/), East View's [Global Press Archive (GPA)](https://www.eastview.com/resources/gpa/crl-mena/)
    + partially hidden behind paywalls, geo-fencing
    + unknown quality but commonly extremly bad
    + no structural mark-up
    + proprietary interfaces, no APIs

## 1.4.1 state of digitisation: text

<div class="c_width-60 c_left">
<!-- ![[*al-Muqtabas* on *al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523)](../assets/shamela_muqtabas-1.png) -->

![[*al-Muqtabas* on *al-Maktaba al-Shāmila*](http://shamela.ws/browse.php/book-26523#page-4046)](../assets/shamela_muqtabas-annotated.png)

</div>
<div class="c_width-30 c_right">

- wrong metadata (volume, issue, page)
- limited structural mark-up

</div>

## 1.4.1 state of digitisation: text

<div class="c_width-50 c_left">

![*al-Muqtabas* 6 on [HathiTrust](http://hdl.handle.net/2027/njp.32101073250910), state of OCR (only visible to US IPs)](../assets/hathi_muqtabas-ocr-3.png)

</div>
<div class="c_width-50 c_right">

![*al-Bashīr* 9 Jan. 1880 (#487), p.1 on [GPA](https://gpa.eastview.com/crl/mena/newspapers/bshr18800109-01.1.1), state of OCR](../assets/gpa_bashir-i_487-p_1_ocr.png)

</div>

## 1.4.2 state of digitisation: facsimiles

Digital imagery, e.g. [Endangered Archives Programme (EAP)](http://eap.bl.uk/project/EAP119), [HathiTrust](http://catalog.hathitrust.org/Record/100658549), [*arshīf al-majallāt al-adabiyya wa-l-thaqafiyya al-ʿarabiyya*](http://archive.alsharekh.org/newmagazineYears/125) <!-- formerly sakhrit -->

+ lack of metadata
+ limited licences, paywalls
+ no or very bad text layers

## 1.4.2 state of digitisation: facsimiles

![*al-Muqtabas* 6 on [EAP](https://eap.bl.uk/archive-file/EAP119-1-4-5#?c=0&m=0&s=0&cv=0&xywh=-301%2C-145%2C2174%2C2880)](../assets/eap119-1-4-5-muqtabas-iiif.png)

## 1.4.2 state of digitisation: facsimiles

![[*al-Muqtabas* 6 on HathiTrust without US IP](http://hdl.handle.net/2027/njp.32101073250910)](../assets/hathi_muqtabas-1.png)

## 1.4.2 state of digitisation: facsimiles

![[*al-Muqtabas* 6 on HathiTrust with US IP](http://hdl.handle.net/2027/njp.32101073250910)](../assets/hathi_muqtabas-2.png)

## 1.4.2 state of digitisation: "fakesimiles"

<!-- original facsimile: [EAP](http://images.eap.bl.uk/EAP119/EAP119_1_4_4/463.jp2/full/800,/0/gray.jpg) -->

*al-Muqtabas* 5(7), pp.[463](https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_54.TEIP5.xml#pb_61.d1e2036)--[466](https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_54.TEIP5.xml#pb_64.d1e2045)

<div class="c_width-30">

![facsimile of the original from EAP](../assets/eap_muqtabas-v_5-i_7-p_463.jpg)

</div><div class="c_width-30">

<!-- shamela's transcription -->
![digital text on *shamela.ws*](../assets/shamela_muqtabas-i_54-p_30-31.png)

</div><div class="c_width-30">

<!-- sakhrit's fake facsimile -->
!["fakesimile" from [*arshīf al-majallāt [...] al-ʿarabiyya*](https://archive.alsharekh.org/MagazinePages/Magazine_JPG/AL_moqtabs/Al_moqtabs_1910/Issue_7/605.JPG)](../assets/sakhrit_muqtabas-v_5-i_7-p_605.jpg)

</div>

## 1.4.3 state of digitisation: bibliographic metadata

- needs:
    + reliable bibliographic metadata on the article level
    + across periodicals
- reality:
    + no platform serving machine-actionable bibliographic metadata below the item level

## 1.4.3 state of digitisation: bibliographic metadata

<div class="c_width-60 c_left">

![*al-Muqtabas* 6 on [EAP](https://eap.bl.uk/archive-file/EAP119-1-4-5#?c=0&m=0&s=0&cv=0&xywh=-301%2C-145%2C2174%2C2880)](../assets/eap119-1-4-5-muqtabas-iiif-metadata.png)

</div>
<div class="c_width-30 c_right">

- *hijri* calendar in the original
- Gregorian calendar in the metadata

</div>

# 2. Idea: Bootstrapping digital scholarly editions
## 2.1 Aims and principles

1. ideas:
    - unite **available** facsimiles and transcriptions
    - harvest, generate, validate and share open metadata
2. aims
    + **validate** the transcription against the facsimiles
    - **improve** the transcription with the help of the "crowd"
    - **train** text recognition algorithms
    - **citable** for scholars, **linkable** for machines
    - share all data, metadata and tools with the broadest possible licences to facilitate access and re-use
3. principles
    - re-purpose **available** and **established** tools, technologies, and material
    - preference for **open**, **free**, and **simple** formats and tools

## 2.2 Deliverables: basic components

1. XML/TEI editions with their own [schema for Arabic periodicals](https://github.com/OpenArabicPE/OpenArabicPE_ODD)
    + text links to open-access digital facsimiles
2. Structured bibliographic metadata (MODS, BibTeX)
    + based on XML editions
    + scraped from the web and validated
    + generated through iteration
3. Scripts to
    + scrape full text / bibliographic information from the web
    + convert scraped information into TEI, MODS, BibTeX
    + generate bibliographic through iteration
    + improve the TEI mark-up

## 2.2 Deliverables: Core features

1. Open licences: [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/) (TEI, MODS, BibTeX), MIT license (XSLT, XQuery)
1. Social digital editions hosted on [GitHub](https://github.com): gradually improve transcription and mark-up
2. Releases are archived at [Zenodo](https://zenodo.org): DOI for reliable citation
3. [Static web-view](https://github.com/tillgrallert/tei-boilerplate-arabic-editions)<!--  (doesn't require a permanent internet connection) -->: side-by-side view of facsimiles and text
4. Access to bibliographic metadata through a public [Zotero group](https://www.zotero.org/groups/openarabicpe)

<!-- mention: process of cleaning data and disambiguation of entities -->

<!-- ![[Display of *al-Muqtabas* 6(2)](https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png) -->

## 2.3 Summary

![Figure: Project scheme](../assets/OpenArabicPE_components-layer-1-4.png)

# 3. Implementation Open Arabic Periodical Editions (OpenArabicPE)
## 3. The corpus

| periodical                                                                          | doi                                                                | volumes    | issues    | articles    | words      |
| ----------------------------------------------------------------------------------- | ------------------------------------------------------------------ | ---------: | --------: | ----------: | ---------: |
| [al-Ḥaqāʾiq](https://www.github.com/openarabicpe/digital-haqaiq)                    | [10.5281/zenodo.1232016](https://doi.org/10.5281/zenodo.1232016)   | 3          | 35        | 389         | 298090     |
| [al-Ḥasnāʾ](https://www.github.com/openarabicpe/journal_al-hasna)                   | [10.5281/zenodo.3556246](https://doi.org/10.5281/zenodo.3556246)   | 1          | 12        | 201         | NA         |
| [al-Manār](https://www.github.com/openarabicpe/journal_al-manar)                    |                                                                    | 35         | 537       | 4300        | 6144593    |
| [al-Muqtabas](https://www.github.com/tillgrallert/digital-muqtabas)                 | [10.5281/zenodo.597319](https://doi.org/10.5281/zenodo.597319)     | 9          | 96        | 2964        | 1981081    |
| [al-Ustādh](https://www.github.com/openarabicpe/journal_al-ustadh)                  | [10.5281/zenodo.3581028](https://doi.org/10.5281/zenodo.3581028)   | 1          | 42        | 435         | 221447     |
| [al-Zuhūr](https://www.github.com/openarabicpe/journal_al-zuhur)                    | [10.5281/zenodo.3580606](https://doi.org/10.5281/zenodo.3580606)   | 4          | 39        | 436         | 292333     |
| [Lughat al-ʿArab](https://www.github.com/openarabicpe/journal_lughat-al-arab)       | [10.5281/zenodo.3514384](https://doi.org/10.5281/zenodo.3514384)   | 3          | 34        | 939         | 373832     |
| **total**                                                                           |                                                                    | 56         | 795       | 9664        | 9311376    |


## 3. Basic components and features

![](../assets/OpenArabicPE_components-layer-1-2.png)


## 3.1 Components: Generate a TEI edition

- scrape the [digital text from *shamela.ws*](http://shamela.ws/index.php/book/26523)
- transform it into [TEI XML](http://www.tei-c.org): semi-automatically (mostly XSLT)
    + documented URI design to reference all elements
- add structural mark-up (sections, articles, heads, authors ...): semi-automatically
- link to digital facsimiles from the [British Library's "Endangered Archives Programme" (EAP)](http://eap.bl.uk/database/overview_item.a4d?catId=809;r=12316) and [HathiTrust](http://catalog.hathitrust.org/Record/100658549) or produce your own imagery: semi-automatically (mostly manually)
- host everything but images on [GitHub](https://www.github.com)
    + distributed version control
    + attribution of authorship
- provide a [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/) for all files

<!--  edit bullet point on licences -->


## 3.1 Basis: TEI files

```xml
<text xml:id="text" xml:lang="ar" type="issue" n="i62">
    <pb ed="print" n="177" facs="#facs_181" xml:id="pb_2.d1e1489"/>
    <front xml:lang="ar" xml:id="front_1.d1e1431">
         <div type="masthead">
            <bibl>
               <tei:biblScope unit="issue" n="3">الجزء 3</tei:biblScope>
               <tei:biblScope unit="volume" n="6">المجلد 6</tei:biblScope><lb/>
               <title level="j" xml:lang="ar">المقتبس</title>
            </bibl>
         </div>
    </front>
    <body xml:id="body_1.d1e1485" xml:lang="ar">
        <pb corresp="file:../epub/26523/OEBPS/xhtml/P4092.xhtml" ed="shamela" n="n62-p1" xml:id="pb_1.d1e1487"/>
        <div type="article" xml:id="div_2.d1e1491" xml:lang="ar">
            <head xml:id="head_1.d1e1493" xml:lang="ar">الفتوى في الإسلام</head>
            <p xml:id="p_15.d1e1496" xml:lang="ar">تابع ل <ref target="oclc_4770057679-i_61.TEIP5.xml#div_2.d1e1517" xml:id="ref_5.d1e1694">ما في الجزء الماضي</ref></p>
            <div type="section" xml:id="div_2.d1e1499" xml:lang="ar">
                <head xml:id="head_2.d1e1501" xml:lang="ar">آداب المستفتي وصفته وأحكامه</head>
                <div type="section" xml:id="div_2.d1e1504" xml:lang="ar">
                    <head xml:id="head_3.d1e1506" xml:lang="ar">الأول</head>
                    <p xml:id="p_16.d1e1509" xml:lang="ar">المستفتي كل من لم يبلغ درجة المفتي فهو فيما يسأل عنه من الأحكام الشرعية مستفت بتقليد من نفسه.</p>
                    <p xml:id="p_17.d1e1512" xml:lang="ar">والمختار في التقليد أنه قبول قول من يجوز عليه الإصرار على الخطاء بغير حجة على عين ما قبل قوله فيه.</p>
                    <p xml:id="p_18.d1e1515" xml:lang="ar">ويجب عليه الاستفتاء إذا نزلت به حادثة يجب عليه علم حكمها.</p>
                    <p xml:id="p_19.d1e1518" xml:lang="ar">فإن لم يجد ببلده من يستفتيه وجب عليه الرحيل إلى من يفتيه وإن بعدت داره وقد رحل خلائق من السلف في المسألة الواحدة الأيام والليالي.</p>
                </div>
            </div>
        </div>
    </body>
</text>
```


<!--
## 3.1 Basis: TEI files

![TEI file of *al-Muqtabas* 6(2) in oXygen: author mode](../assets/oxygen_muqtabas-1.png)

-->

## 3.1 Basis: Is this legal?

![External sources, external labour, and the question of copyright](../assets/OpenArabicPE_components-copyright.png)

## 3.1 Basis: Is this legal?

Copyright depends on the jurisdiction of creators, distributors, etc.

1. text of *al-Muqtabas*
    + is in the **public domain**: transcription and imaging is **legal**.^[even in the US as attested to by HathiTrust]
    + the transcribers do not / cannot claim copyright: copying is **legal**
2. images of *al-Muqtabas*
    + digital files are protected by copyright: use is subject to licence, linking is **legal**
    + download and redistribution: almost certainly **illegal**
3. digital edition of *al-Muqtabas*
    + all our work is licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)

## 3.2 Core feature: Continuous improvement

1. Improvements depending on human labour (probably a "crowd")
    - correct the transcription
    - add structural mark-up
    - add semantic mark-up
2. Automatic improvements:
    - provide reliable bibliographic metadata based on the facsimile
    - mark-up of natural entities with link to external reference files (e.g. personal names, toponyms)

## 3.2 Core feature: how to contribute

<div class="c_width-50">

- Go to [GitHub](https://www.github.com) and register a free account
- **Fork** the editions' repositories: e.g. <https://www.github.com/openarabicpe/journal_lughat-al-arab>
- Edit the text (XML)
- Send us a **pull request**
- We will review and merge your changes

</div><div class="c_width-50">

![](../assets/github_branches-1.png)

</div>

## 3.3 Core feature: web-view

- **open**, **free-of-charge**, **client-based**
- Adaptation of the [TEI Boilerplate XSLT stylesheets](http://dcl.slis.indiana.edu/teibp/) to (Arabic) periodical editions
- human-readable and static web-view (either rawgit or gh-pages)
    + generated on-the-fly by the user's browser using XSLT 1 to transform the TEI XML files to HTML.
    + can be run without an internet connection and with local facsimiles.
- parallel display of text and facsimile
    + simple changes to display different facsimiles
- link to metadata on the article level (MODS, BibTeX)
- the code is shared with a [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/) on [GitHub](https://github.com/tillgrallert/tei-boilerplate-arabic-editions)

## 3.3 Core feature: web-view

![[Display of *al-Muqtabas* 6(2)](https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png)

## 3.4 Core feature: Zotero group

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": list view](../assets/zotero-group_openarabicpe-search.png)

## 3.4 Core feature: Zotero group

<div class="c_width-50 c_left">

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": search in mobile view](../assets/zotero-group_openarabicpe-mobile-search.png)

</div>
<div class="c_width-50 c_right">

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": details in mobile view](../assets/zotero-group_openarabicpe-mobile-details.png)

</div>

<!-- the following still needs work -->
## 3.5 Core feature: preservation, DOI

<div class="c_width-50 c_left">

|                                   periodical                                  |                               doi                                |                                                                               release                                                                               |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [al-Ḥaqāʾiq](https://www.github.com/openarabicpe/digital-haqaiq)              | [10.5281/zenodo.1232016](https://doi.org/10.5281/zenodo.1232016) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/digital-haqaiq.svg)](https://github.com/openarabicpe/digital-haqaiq/releases)                 |
| [al-Ḥasnāʾ](https://www.github.com/openarabicpe/journal_al-hasna)             | [10.5281/zenodo.3556246](https://doi.org/10.5281/zenodo.3556246) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_al-hasna.svg)](https://github.com/openarabicpe/journal_al-hasna/releases)             |
| [al-Manār](https://www.github.com/openarabicpe/journal_al-manar)              |                                                                  | <!-- [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_al-manar.svg)](https://github.com/openarabicpe/journal_al-manar/releases)  -->   |
| [al-Muqtabas](https://www.github.com/tillgrallert/digital-muqtabas)           | [10.5281/zenodo.597319](https://doi.org/10.5281/zenodo.597319)   | [![GitHub release](https://img.shields.io/github/release/tillgrallert/digital-muqtabas.svg)](https://github.com/tillgrallert/digital-muqtabas/releases)             |
| [al-Ustādh](https://www.github.com/openarabicpe/journal_al-ustadh)            | [10.5281/zenodo.3581028](https://doi.org/10.5281/zenodo.3581028) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_al-ustadh.svg)](https://github.com/openarabicpe/journal_al-ustadh/releases)           |
| [al-Zuhūr](https://www.github.com/openarabicpe/journal_al-zuhur)              | [10.5281/zenodo.3580606](https://doi.org/10.5281/zenodo.3580606) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_al-zuhur.svg)](https://github.com/openarabicpe/journal_al-zuhur/releases)             |
| [Lughat al-ʿArab](https://www.github.com/openarabicpe/journal_lughat-al-arab) | [10.5281/zenodo.3514384](https://doi.org/10.5281/zenodo.3514384) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_lughat-al-arab.svg)](https://github.com/openarabicpe/journal_lughat-al-arab/releases) |

</div><div class="c_width-50 c_right">

![](../assets/zenodo_muqtabas.png)

</div>


# 4. To do
## ongoing work

- Editorial decisions: TEI schema design
    <!-- + TEI is rooted in the western episteme -->
- Editorial work:
    + correcting transcriptions
    + add non-Arabic words omitted by *shamela.ws*
    + add footnotes
- Web-display:
    + needs some polishing
    + search functions beyond the Zotero group and individual issues (project can be searched on GitHub)
- Scanning:

# 5. Experiences
## simple, fast, sustainable

- Simple technologies and relatively little coding needed:
    + Initial project set-up took less than four weeks of after-hour labour
- Hosting, collaborative editing, long-term preservation and DOIs are provided free of cost
- Core (but simple) features **cannot** be automated:
    + c.7000 page breaks were manually tagged
    + does **not** require knowledge of XML, TEI or access to more than a syntax-aware text editor.

<!-- - Collaboration in bootstrapped framework with multiple dependencies  -->
<!--     + it took a part-time intern 4 weeks to tag one volume of 800 pages -->
<!-- - TEI editing
    - requires some training
    - patchy support of Arabic across operating systems, Java versions -->
   <!--  + We set-up the sister project [Digital Ḥaqāʾiq](https://www.github.com/tillgrallert/digital-haqaiq) as a digital edition of ʿAbd al-Qādir al-Iskandarānī's monthly journal *al-Ḥaqāʾiq* (1910–12, Damascus) in a single day. -->
    <!-- - Muḥammad Rashīd Riḍā's journal *al-Manār*
        + [full text from shamela](http://shamela.ws/index.php/book/6947): 8605 views
        + [imagery from HathiTrust](http://catalog.hathitrust.org/Record/008882663),[imagery / PDFs from the Internet Archive](https://archive.org/details/almanaralmanar), which are linked from [*al-Maktaba al-Waqfiyya*](http://waqfeya.com/book.php?bid=7374)
    -->

## Workflow

1. get the data
    - facsimiles
        + link to existing facsimiles, preferably through IIIF
        + scan your physical artefacts*
    - text
        + scrape existing transcriptions
        + use [Transkribus]()* with our model trained on 1000+ pages from the OpenArabicPE corpus
2. save and share the data
    - facsimiles: [Internet Archive](https://archive.org) (supports IIIF)
    - working copy of everything else: [GitHub](https://github.com/)
    - longterm preservation: [Zenodo](https://zenodo.org/)
        + make sure to add ORCIDs for all contributors
3. edit the data
4. disseminate the data
    - host webviews, project blogs: [gh-pages]()
    - bibliographic database: [Zotero](https://www.zotero.org/groups/openarabicpe/items/)

# 6. Conclusion
## Summary: OpenArabicPE

- open scholarly **digital editions** of [*[Majallat] al-Muqtabas*](https://github.com/tillgrallert/digital-muqtabas) and [*al-Ḥaqāʾiq*](https://github.com/OpenArabicPE/digital-haqaiq) providing
    + TEI XML files (transcription and links to facsimiles)
    + plain text files
    + MODS and BibTeX files for every article
    + customised version of TEI Boilerplate (XSLT and CSS) with stable URLs for every element
- validated open **bibliographic metadata** (MODS) for
    - [*al-Jinān* (1875--1885)](https://github.com/OpenArabicPE/journal_al-jinan), [*al-Quds* (#1--391, 1908--14)](https://github.com/OpenArabicPE/newspaper_al-quds), [*Ḥadīqat al-Akhbār* (#1--357, 1858--65)](https://github.com/OpenArabicPE/newspaper_hadiqat-al-akhbar), [*Thamarāt al-Funūn* (#1--1695, 1875--1908)](https://github.com/OpenArabicPE/newspaper_thamarat-al-funun)
- within a framework (git, [GitHub](https://github.com/openarabicpe), [Zenodo](https://zenodo.org/), [Zotero](https://www.zotero.org/groups/openarabicpe/items/)) that allows for / provides
    + collaborative, open, version-controlled improvements
    + re-use of the data, metadata and tools
    + long-term preservation and DOIs
    + discovery <!-- in CLARIN -->

## Thank you!

- Contributors to OpenArabicPE: Jasper Bernhofer, Dimitar Dragnev, Patrick Funk, Talha Güzel, Hans Magne Jaatun, Xaver Kretzschmar, Daniel Lloyd, Klara Mayer, Tobias Sick, Manzi Tanna-Händel and Layla Youssef
- Links:
    + Slides: [https://OpenArabicPE.github.io/slides/2020-ifao/](https://OpenArabicPE.github.io/slides/2020-ifao/index.html)
    <!-- + Paper (draft): <https://doi.org/10.5281/zenodo.1413610> -->
    + Project URLs: [https://www.github.com/OpenArabicPE](https://www.github.com/OpenArabicPE), <!-- [https://www.github.com/tillgrallert/digital-muqtabas](https://www.github.com/tillgrallert/digital-muqtabas), [https://www.github.com/OpenArabicPE/digital-haqaiq](https://www.github.com/OpenArabicPE/digital-haqaiq) -->
    + Project blog: [https://openarabicpe.github.io](https://openarabicpe.github.io)
    + Twitter: @[tillgrallert](https://twitter.com/tillgrallert)
    + Email: <grallert@orient-institut.org> <till.grallert@fu-berlin.de>
- Licence: slides and images are licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)
