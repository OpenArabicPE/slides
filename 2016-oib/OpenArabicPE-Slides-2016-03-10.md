---
title: "Digital Arabic Periodical Editions: presentation at the internal OIB colloquium"
author: Till Grallert
date: 2016-03-10
duration: 30
---

## #freebassel

Bassel Khartabil / باسل خرطبيل

+ Syrian software engineer
+ leading advocat for open access and Creative Commons (CC) in Syria
+ author of the Arabic CC licences
+ detained by the regime since 15 March 2012
+ moved to an unknown location and probably killed in Oct 2015

## Hacking academia? Open scholarly digital editions of the Damascene journals *al-Muqtabas* (1906–19) and *al-Ḥaqāʾiq* (1910–12) between Shamela.ws, HathiTrust, and GitHub

Project URL: [https://www.github.com/openarabicpe/journal_al-muqtabas](https://www.github.com/openarabicpe/journal_al-muqtabas)

Slides: [https://tinyurl.com/oib-2016-03-10](https://tillgrallert.github.io/Slides/OIBColloquium2016)

Twitter: @tillgrallert

Email: <grallert@orient-institut.org>

# Introduction
## 1.1 Importance of mundane texts / periodicals

- They are at the core of various discourses
    + Modernity / -ism at the end of empire
    + Arabic renaissance
    + Arab nationalism
    + Islamic reform movement
- They form large corpora with an equal distribution along a temporal axis (*al-Muqtabas*: 12 yrs, *al-Manār*: 43 yrs, *al-Muqtaṭaf*: 76 yrs)
    + linguistic analysis
    + historical semantics
    + data sets for social history

## 1.2 A two-fold problem

- Preservation:
    + Active destruction of cultural artifacts: iconoclasm, neoliberalism
    + Negelct: fragile materiality
- Access:
    + Absence / destruction of infrastructure / channels of knowledge transmission: lack of access to institutions, hardware, software, internet connections
    + widely-dispersed collections
    + technologies: absence of reliable OCR
    + technical skills: lack of basic scripting skills

The consequence is a focus on "high" culture and canonical texts

## 1.3 State of digitisation
<!-- This should be a demo session, otherwise one needs screenshots -->

1. gray online libraries / "crowd"-sourced transcriptions, e.g. [*al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523), [*Mishkāt*](http://almeshkat.net/), [*Ṣayd al-Fawāʾid*](http://saaid.net/), [*al-Waraq*](http://www.alwaraq.net/) etc.
2. Digital imagery, e.g. [Endangered Archives Programme (EAP)](http://eap.bl.uk/database/overview_project.a4d?projID=EAP119;r=63), [HathiTrust](http://catalog.hathitrust.org/Record/100658549)


## 1.3.1 state of digitisation: text

gray online libraries / "crowd"-sourced transcriptions, e.g. [*al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523), [*Mishkāt*](http://almeshkat.net/), [*Ṣayd al-Fawāʾid*](http://saaid.net/), [*al-Waraq*](http://www.alwaraq.net/) etc.

+ lack of / faulty metadata
+ unknown editing principles
+ unknown quality
+ very limited structural mark-up
+ cannot be reliably cited

## 1.3.1 state of digitisation: text

<!-- ![[*al-Muqtabas* on *al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523)](../assets/shamela_muqtabas-1.png) -->

![[*al-Muqtabas* on *al-Maktaba al-Shāmila*](http://shamela.ws/browse.php/book-26523#page-4046)](../assets/shamela_muqtabas-2.png)

## 1.3.2 state of digitisation: images

Digital imagery, e.g. [Endangered Archives Programme (EAP)](http://eap.bl.uk/database/overview_project.a4d?projID=EAP119;r=63), [HathiTrust](http://catalog.hathitrust.org/Record/100658549)

+ lack of metadata
+ limited licences, paywalls
+ no or very bad text layers

## 1.3.2 state of digitisation: images

![[*al-Muqtabas* 6 on EAP](http://eap.bl.uk/database/overview_item.a4d?catId=810;r=288)](../assets/eap119-1-4-5-muqtabas.png)

## 1.3.2 state of digitisation: images

![[*al-Muqtabas* 6 on HathiTrust without US IP](http://hdl.handle.net/2027/njp.32101073250910)](../assets/hathi_muqtabas-1.png)

## 1.3.2 state of digitisation: images

![[*al-Muqtabas* 6 on HathiTrust with US IP](http://hdl.handle.net/2027/njp.32101073250910)](../assets/hathi_muqtabas-2.png)

## 1.3.2 state of digitisation: images

![[*al-Muqtabas* 6 on HathiTrust, state of OCR (only visible to US IPs)](http://hdl.handle.net/2027/njp.32101073250910)](../assets/hathi_muqtabas-ocr-2.png)

# 2. Proposed solution
## 2. unite facsimile and transcription

1. aims
    + *validate* the transcription against the facsimiles
    - *improve* the transcription with the help of the "crowd"
    - make everything *citable* for scholars, *linkable* for machines
    - provide the new edition with the broadest possible licence to facilitate access and re-use
2. principles
    - re-purpose *available* and *established* tools, technologies, and material
    - preference for *open* and *simple* formats and tools

# 3. Test case: digital *Muqtabas*
## 3. Test case: digital *Muqtabas*

1. Basis: Generate and share a TEI edition of all 96 issues (c. 7000 pages) of Muḥammad Kurd ʿAlī's *Majallat al-Muqtabas* with a [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/)
2. Core feature: gradually improve the digital edition (text and mark-up)
3. Sugar on top: Static web-view (doesn't require a permanent internet connection)

## 3. Test case: digital *Muqtabas*

![Project scheme](../assets/OpenArabicPE-organigramme_horizontal.png)

<!-- # 3.1 Basis: Generate the TEI edition

![](../assets/OpenArabicPE-organigramme_vertical-input.png)

![](../assets/OpenArabicPE-organigramme_vertical-edition.png) -->

## 3.1 Basis: Generate the TEI edition

- crawl the [digital text from *shamela.ws*](http://shamela.ws/index.php/book/26523)
- transform it into [TEI XML](http://www.tei-c.org): semi-automatically (mostly XSLT)
    + documented URI design to reference all elements
- add structural mark-up (sections, articles, heads, authors ...): semi-automatically
- link to digital facsimiles from the [British Library's "Endangered Archives Programme" (EAP)](http://eap.bl.uk/database/overview_item.a4d?catId=809;r=12316) and [HathiTrust](http://catalog.hathitrust.org/Record/100658549) or produce your own imagery: semi-automatically (mostly manually)
- host everything but images on [GitHub](https://www.github.com)
    + distributed version control
    + attribution of authorship
- provide a [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/) for all files: edition, tools, webview

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
        <!-- ... -->
    </body>
</text>
```

## 3.1 Basis: TEI files

![TEI file of *al-Muqtabas* 6(2) in oXygen: author mode](../assets/oxygen_muqtabas-1.png)

## 3.1 Basis: Is this legal?

![](../assets/OpenArabicPE-organigramme_vertical-input.png)

## 3.1 Basis: Is this legal?

Copyright depends on the jurisdiction of creators, distributors, etc.

1. text of *al-Muqtabas*
    + is in the public domain: transcription is *legal*
    + the transcribers do not / cannot claim copyright: copying is *legal*
2. images of *al-Muqtabas*
    + digital files are protected by copyright: use is subject to licence, linking is *legal*
    + download and redistribution: almost certainly *illegal*
3. digital edition of *al-Muqtabas*
    + all our work is licenced as [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/)

## 3.2 Core feature: Continuous improvement

![](../assets/OpenArabicPE-organigramme_vertical-crowd.png)

## 3.2 Core feature: Continuous improvement

1. Improvements depending on human labour (probably a "crowd")
    - correct the transcription
    - add structural mark-up
    - add semantic mark-up
2. Automatic improvements:
    - provide reliable bibliographic metadata based on the facsimile
    - mark-up of natural entities with link to external reference files (e.g. personal names, toponyms)

## 3.2 Core feature: how to contribute

- go to [GitHub](https://www.github.com) and register a free account
- *fork* the the [edition's repository](https://www.github.com/openarabicpe/journal_al-muqtabas): [https://tinyurl.com/muqtabas](https://tinyurl.com/muqtabas)
- edit the text
- send us a *pull request*
- changes will be reviewed and merged

## 3.3 Sugar on top: web-view

![[Display of *al-Muqtabas* 6(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas-2.png)

## 3.3 Sugar on top: web-view

- Adaptation of [TEI Boilerplate XSLT stylesheets](http://dcl.slis.indiana.edu/teibp/)
- human-readable and static web-view (either rawgit or gh-pages)
    + generated on-the-fly by the user's browser using XSLT to transform the TEI XML files.
    + can be run without an internet connection and with local facsimiles.
- parallel display of text and facsimile
    + simple changes to display different facsimiles
- link to metadata on the article level (BibTeX)
- the code is shared with a [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/) on [GitHub](https://github.com/tillgrallert/tei-boilerplate-arabic-editions)

## 3.3 Sugar on top: Zotero group

![Zotero group "[digital-muqtabas](https://www.zotero.org/groups/digital-muqtabas/items/)": list view](../assets/zotero-group_digital-muqtabas-1.png)

## 3.3 Sugar on top: Zotero group

![Zotero group "[digital-muqtabas](https://www.zotero.org/groups/digital-muqtabas/items/)": item view](../assets/zotero-group_digital-muqtabas-2.png)

# Conclusion
## 4. To do, ongoing work

- Schema design
    + mark-up of some text features has not yet been decided
- mark-up of page breaks
- Web-view needs some polishing

## 5. Experiences: simple, fast, sustainable

- Simple technologies and relatively little coding needed: Initial set-up took less than four weeks of after-hour labour
- Hosting with GitHub is free
- Core (but simple) features cannot be automated: all c.7000 page breaks must be manually tagged
- Code that can be re-purposed for---inter alia---Muḥammad Rashīd Riḍā's journal *al-Manār*
    + [full text from shamela](http://shamela.ws/index.php/book/6947): 8605 views
    + [imagery from HathiTrust](http://catalog.hathitrust.org/Record/008882663),[imagery / PDFs from the Internet Archive](https://archive.org/details/almanaralmanar), which are linked from [*al-Maktaba al-Waqfiyya*](http://waqfeya.com/book.php?bid=7374)

## Summary

- open scholarly digital editions of *[Majallat] al-Muqtabas* and *al-Ḥaqāʾiq* providing
    + TEI XML files (transcription and links to facsimiles)
    + plain text files
    + BibTeX files for every article
    + customised version of TEI Boilerplate (XSLT and CSS) with stable URLs for every element
- within a framework (git and GitHub) that allows for
    + collaborative, open, version-controlled improvements of the edition
    + re-use of the text
