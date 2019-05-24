---
title: "Open Arabic Periodical Editions (OpenArabicPE): an attempt to unite gray online libraries, social editing, and scholarly rigour"
author: Till Grallert, Orient-Institut Beirut (OIB)
date: 2017-04-10
duration: 20
---

## Open Arabic Periodical Editions (OpenArabicPE): an attempt to unite gray online libraries, social editing, and scholarly rigour

Till Grallert, Orient-Institut Beirut (OIB)
10 April 2017, Digital Humanities Abu Dhabi, NYU Abu Dhabi

Extended slides: [https://OpenArabicPE.github.io/slides/2017-dhad/](https://OpenArabicPE.github.io/slides/2017-dhad/index.html)

## outline

1. Introduction to the problems at hand
2. Proposed solution: OpenArabicPE
3. Test case: Digital *Muqtabas*
4. Experiences

# 1. Introduction
## 1.1 Importance of mundane texts / periodicals

- At the core of various discourses
    + Modernity / -ism at the end of empire
    + Arabic renaissance
    + Arab nationalism
    + Islamic reform movement
- Large corpora with an equal distribution along a temporal axis (*al-Muqtabas*: 12 yrs, *al-Manār*: 43 yrs, *al-Muqtaṭaf*: 76 yrs)
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

- Consequence: focus on facsimile editions of rare manuscripts

# 1.3 Digitisation as promised remedy
## 1.3.1 state of digitisation: text

"crowd"-sourced transcriptions / gray online libraries, e.g. [*al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523), [*Mishkāt*](http://almeshkat.net/), [*Ṣayd al-Fawāʾid*](http://saaid.net/), [*al-Waraq*](http://www.alwaraq.net/) etc.

+ lack of / faulty metadata
+ unknown editing principles
+ unknown quality
+ very limited structural mark-up
+ cannot be reliably cited

## 1.3.1 state of digitisation: text

![[*al-Muqtabas* on *al-Maktaba al-Shāmila*](http://shamela.ws/browse.php/book-26523#page-4046)](../assets/shamela_muqtabas-annotated.png)

## 1.3.1 state of digitisation: text

![[*al-Muqtabas* 6 on HathiTrust](http://hdl.handle.net/2027/njp.32101073250910), state of OCR (only visible to US IPs)](../assets/hathi_muqtabas-ocr-2.png)

## 1.3.2 state of digitisation: images

Digital imagery, e.g. [Endangered Archives Programme (EAP)](http://eap.bl.uk/database/overview_project.a4d?projID=EAP119;r=63), [HathiTrust](http://catalog.hathitrust.org/Record/100658549)

+ lack of metadata
+ limited licences, paywalls
+ no or very bad text layers

## 1.3.2 state of digitisation: images

![[*al-Muqtabas* 6 on EAP](http://eap.bl.uk/database/overview_item.a4d?catId=810;r=288)](../assets/eap119-1-4-5-muqtabas-annotated.png)

## 1.3.2 state of digitisation: images

![[*al-Muqtabas* 6 on HathiTrust](http://hdl.handle.net/2027/njp.32101073250910) without US IP](../assets/hathi_muqtabas-1.png)

## 1.3.2 state of digitisation: images

![[*al-Muqtabas* 6 on HathiTrust](http://hdl.handle.net/2027/njp.32101073250910) with US IP](../assets/hathi_muqtabas-2.png)

## 1.3.2 state of digitisation: images

![[*al-Muqtabas* 6 on HathiTrust](http://hdl.handle.net/2027/njp.32101073250910), state of OCR (only visible to US IPs)](../assets/hathi_muqtabas-ocr-2.png)

## 1.3.2 state of digitisation: images

!["Fake" scan of *al-Muqtabas* on [*sakhrit*](http://archive.sakhrit.co/MagazinePages/Magazine_JPG/AL_moqtabs/AL_moqtabs_1910/Issue_7/605.JPG) based on *shamela*'s transcription'](../assets/sakhrit_muqtabas-1910-7-605.jpg)

## 1.3.3 state of digitisation: bibliographic metadata

+ on the item (issue, volume) level: faulty metadata
+ on the article level: inexistent or of unknown quality
+ across periodicals: bound to digitisation projects from the same source
+ very limited access to machine-actionable serialisations

# 2. Proposed solution: Unite facsimile and transcription
## 2.1 Aims and principles

1. aims
    + **validate** the transcription against the facsimiles
    - **improve** the transcription with the help of a "crowd"
    - make everything **citable** for scholars, **linkable** for machines
    - provide the new edition with the broadest possible licence to facilitate access and re-use
2. principles
    - re-purpose **available** and **established** tools, technologies, and material
    - preference for **open** and **simple** formats and tools

## 2.2 Deliverables

1. Basis:
    1. XML/TEI editions with their own [schema](https://github.com/OpenArabicPE/OpenArabicPE_ODD)
        + text links to open-access digital facsimiles
        + licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)
    2. Structured bibliographic metadata (MODS, BibTeX)
    3. Tools to
        + scrape full text / bibliographic information from the web
        + convert scraped information into TEI, MODS, BibTeX
        + improve the TEI mark-up

## 2.2 Deliverables

2. Core features:
    1. Social digital edition hosted on GitHub: gradually improve transcription and mark-up
    2. Releases are archived at [Zenodo](https://zenodo.org) and receive a DOI
3. Sugar on top:
    1. [Static web-view](https://github.com/tillgrallert/tei-boilerplate-arabic-editions) (doesn't require a permanent internet connection) providing side-by-side view of facsimiles and text
    <!-- - bibliographic metadata for all issues and articles (MODS, BibTeX) -->
    3. Access to bibliographic metadata through a public Zotero group


# 3. Test case: digital *Muqtabas*
## 3. Test case: The journal of *al-Muqtabas*

*al-Muqtabas* / المقتبس

- "monthly" journal published by Muḥammad Kurd ʿAlī between 1906 and 1918/19 in Cairo and, from 1908 onwards, in Damascus.
    + 9 volumes, 96 issues (at least 2 double issues), c. 7000 pages
- Muḥammad Kurd ʿAlī (1876-1952): Ottoman bureaucrat, journalist, president of the Syrian Academy of Sciences, minister of education.
- available at c. 30 libraries (North America, Europe, Middle East):
    + original prints (mostly incomplete)
    + some copies of a "gray" reprint
    + a number of microfiche copies from a single source

<!--     + Palestine: 1 incomplete copy
    + Lebanon: at least 2 complete physical copies
    + Germany: 1 complete physical copy (in Beirut), 4 incomplete (?) microfiche copies
    + USA: 1 complete copy (Chicago) that is the base for most microfiche copies -->

## 3. Test case: digital *Muqtabas*

![[Web-view of *al-Muqtabas* 6(2)](https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas-1.png)

## 3. Test case: digital *Muqtabas*

![TEI file of *al-Muqtabas* 6(2) in oXygen: author mode](../assets/oxygen_muqtabas-1.png)

## 3. Test case: digital *Muqtabas*

![TEI file of *al-Muqtabas* 6(2) in oXygen: plain XML](../assets/oxygen_muqtabas-2.png)

## 3. Test case: digital *Muqtabas*

1. Basis:
    - XML/TEI edition of all 96 issues (c. 7000 pages) of Muḥammad Kurd ʿAlī's *Majallat al-Muqtabas*
    - The text links to open-access digital facsimiles
    - licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)
2. Core feature:
    - social digital edition: gradually improve text and mark-up
    - releases are archived at [Zenodo](https://zenodo.org) and receive a DOI
3. Sugar on top:
    - Static web-view (doesn't require a permanent internet connection)
    - bibliographic metadata for all issues and articles (MODS, BibTeX)
    - access to bibliographic metadata through a public Zotero group

## 3. Test case: digital *Muqtabas*

![Project scheme](../assets/OpenArabicPE-organigramme_horizontal.png)

## 3.1 Basis: Generate the TEI edition

![](../assets/OpenArabicPE-organigramme_horizontal-input.png)

## 3.1 Basis: Generate the TEI edition

- scrape the [digital text from *shamela.ws*](http://shamela.ws/index.php/book/26523)
- transform it into [TEI XML](http://www.tei-c.org): semi-automatically (mostly XSLT)
  <!--   + documented URI design to reference all elements -->
- add structural mark-up (sections, articles, heads, authors ...): semi-automatically
- link to digital facsimiles from the [British Library's "Endangered Archives Programme" (EAP)](http://eap.bl.uk/database/overview_item.a4d?catId=809;r=12316) and [HathiTrust](http://catalog.hathitrust.org/Record/100658549): semi-automatically (mostly manually)
- host everything but images on [GitHub](https://www.github.com)
    + distributed version control
    + attribution of authorship
- provide a [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/) for all files

## 3.1 Basis: TEI files

```xml
<text xml:id="text" xml:lang="ar" type="issue" n="i62">
    <pb ed="print" n="177" facs="#facs_181" xml:id="pb_2.d1e1489"/>
    <front xml:lang="ar" xml:id="front_1.d1e1431">
         <div type="masthead">
            <bibl>
               <tei:biblScope unit="issue" from="3" to="3">الجزء 3</tei:biblScope>
               <tei:biblScope unit="volume" from="6" to="6">المجلد 6</tei:biblScope><lb/>
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

## 3.1 Basis: TEI files

![TEI file of *al-Muqtabas* 6(2) in oXygen: author mode](../assets/oxygen_muqtabas-1.png)

<!-- ## 3.1 Basis: Is this legal?

![External sources, external labour, and the question of copyright](../assets/OpenArabicPE-organigramme_horizontal-input.png) -->

## 3.1 Basis: Is this legal?

Copyright depends on the jurisdiction of creators, distributors, etc.

1. text of *al-Muqtabas*: **public domain**
    + transcription and imaging is **legal**.^[even in the US as attested to by HathiTrust]
    + copying is **legal**
2. images of *al-Muqtabas*: protected by copyright
    + use is subject to licence, linking is **legal**
    + download and redistribution: almost certainly **illegal**
3. our digital edition of *al-Muqtabas*: [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)

## 3.2 Core feature: Continuous improvement

![A social and GitHub-hosted digital edition](../assets/OpenArabicPE-organigramme_vertical-crowd.png)

## 3.2 Core feature: Continuous improvement

1. Improvements depending on human labour (probably a "crowd")
    - correct the transcription
    - add structural mark-up
    - add semantic mark-up
2. Automatic improvements:
    - provide reliable bibliographic metadata based on the facsimile
    - mark-up of natural entities with link to external reference files (e.g. personal names, toponyms)

## 3.2 Core feature: how to contribute

- Go to [GitHub](https://www.github.com) and register a free account
- **Fork** the edition's repository: [https://www.github.com/tillgrallert/digital-muqtabas](https://www.github.com/tillgrallert/digital-muqtabas)
- Edit the text (XML)
- Send us a **pull request**
- We will review and merge your changes

![Branches on GitHub](../assets/github_branches-1.png)

## 3.3 Sugar on top: web-view

- Adaptation of the [TEI Boilerplate XSLT stylesheets](http://dcl.slis.indiana.edu/teibp/) to (Arabic) periodical editions
- human-readable and static web-view (either rawgit or gh-pages)
    + generated on-the-fly by the user's browser <!-- using XSLT 1 to transform the TEI XML files to HTML. -->
    + can be run without an internet connection and with local facsimiles.
- parallel display of text and facsimile
- link to metadata on the article level (MODS, BibTeX)
- the code is shared with a [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/) on [GitHub](https://github.com/tillgrallert/tei-boilerplate-arabic-editions)

## 3.3 Sugar on top: web-view

![[Display of *al-Muqtabas* 6(2)](https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas-1.png)

## 3.3 Sugar on top: Zotero group

[www.zotero.org/groups/OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)

- Metadata for every article (currently *al-Muqtabas*, *al-Ḥaqāʾiq*, *al-Ḥilāl*)
+ Public repository
+ Machine-actionable metadata available through API
+ May generate human-readable citations
+ links to the GitHub-hosted webview

## 3.3 Sugar on top: Zotero group

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": list view](../assets/zotero-group_digital-muqtabas-1.png)

## 3.3 Sugar on top: Zotero group

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": item view](../assets/zotero-group_digital-muqtabas-2.png)

# 4. Experiences after some 18 months
## 4.1 experiences

<!-- needs some pro and contra -->

- Simple technologies and relatively little coding needed: Initial set-up took less than four weeks of after-hour labour
- Hosting, long-term preservation and DOIs are provided free of cost
- Code can be re-purposed:
    + the digital edition of [ʿAbd al-Qādir al-Iskandarānī's monthly journal *al-Ḥaqāʾiq* (1910–12, Damascus)](https://www.github.com/OpenArabicPE/digital-haqaiq) was set up in a single day.
- Core (but simple) features **cannot** be automated:
    + thousands of page breaks must be manually tagged
    <!-- + it took a part-time intern 4 weeks to tag one volume of 800 pages -->

## 4.2 on-going work

- Editorial decisions: modelling and TEI schema design
    + mark-up of some text features has not yet been decided
    + future plan: one article per file
- Editorial work:
    + mark-up of page breaks (1-2 h per issue)
    + correcting transcriptions
    + add non-Arabic words omitted by *shamela.ws*
    + add footnotes omitted by *shamela.ws*
    + correct publication dates for all issues
- Web-display:
    + needs some polishing
    + search functions beyond the Zotero group and individual issues (project can be searched on GitHub)
- Documentation and engagement

## 4.3 applications

- validation of existing digitised editions / platforms:
    + [*shamela.ws*](http://shamela.ws/index.php/book/26523) and derivatives
        * incomplete transcription: all footnotes and non-Arabic text missing, sometimes lengthy omissions
        * faulty transcription: "corrections" and errors
    + [*sakhrit*](http://archive.sakhrit.co/)
        * incomplete and erroneous metadata on the article level
        * percentage of "fake" facsimiles

<!-- # 6. Conclusion
## Summary

- open scholarly digital editions of *[Majallat] al-Muqtabas* and *al-Ḥaqāʾiq* providing
    + TEI XML files (transcription and links to facsimiles)
    + plain text files
    + MODS and BibTeX files for every article
    + customised version of TEI Boilerplate (XSLT and CSS) with stable URLs for every element
- within a framework (git, GitHub, Zenodo) that allows for / provides
    + collaborative, open, version-controlled improvements of the edition
    + re-use of the text
    + long-term preservation and DOIs -->

## Thank you!

- Links:
    + Project URLs: [https://www.github.com/tillgrallert/digital-muqtabas](https://www.github.com/tillgrallert/digital-muqtabas), [https://www.github.com/OpenArabicPE](https://www.github.com/OpenArabicPE)
    + Project blog: [https://tillgrallert.github.io/digital-muqtabas](https://tillgrallert.github.io/digital-muqtabas)
    + Slides: [https://OpenArabicPE.github.io/slides/2017-dhad/](https://OpenArabicPE.github.io/slides/2017-dhad/index.html)
    + Twitter: @[tillgrallert](https://twitter.com/tillgrallert)
    + Email: <grallert@orient-institut.org>

- Licence: The slides are licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)