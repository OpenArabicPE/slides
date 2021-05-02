---
title: "Open Arabic Periodical Editions"
subtitle: "Contributing to the *digital commons* without the help we cannot get"
author: Till Grallert
date: 2021-04-30
ORCID: orcid.org/0000-0002-5739-8094
duration: 10
---


# Open Arabic Periodical Editions (OpenArabicPE)
## Overwiew

:::{.c_width-50 .c_left}

- Corpus of 6 full-text scholarly digital editions (TEI XML) of Arabic magazines from Baghdad, Cairo, Damascus with c.800 issues and more than 9 million words.
- A client-based webview showing text and facsimiles side-by-side (based on TEI Boilerplate).
- Bibliographic metadata (MODS, BibTeX, Zotero RDF)
    - on the article level for the entire corpus plus 2 additional magazines
    - on the issue level for 7 additional newspapers
    - on the title level for 3300+ periodicals (in collaboration with [Project Jarāʾid](https://projectjaraid.github.io))
- Authority files (TEI XML): gazetteer, personography
- A [Zotero group](https://zotero.org/groups/openarabicpe) to search the metadata and access the digital editions
- Code and workflows

:::
:::{.c_width-50 .c_right}

![[Webview of *al-Muqtabas* 6(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png){#fig:webview-muqtabas}

:::

##  Aims and principles

1. ideas:
    - unite **available** facsimiles and transcriptions
    - harvest, generate, validate and share open metadata
2. aims
    + **validate** and **improve** the transcription with the facsimiles
    - **train** text and layout recognition algorithms to make the textual heritage accessible to digitisation efforts
    - **citable** for scholars, **linkable** for machines to facilitate use and adoption of the resources
    - **open licences** to facilitate re-use
3. principles
    - use as few as possible **open** and **simple** formats and tools
    - re-use/purpose **available** and **established** tools, technologies, and material
    - use **free-to-use** platforms without lock-in of data

## Affordances/ constrains

## Why spend the effort? Shouldn't others do it?

OpenArabicPE addresses a clear need, fundamental rights, and our scholarly duties:

1. Societies of the Global South have a **right** to unhampered access to their **own cultural record**---a cultural record that is frequently held by institutions of the Global North---and **on their own terms**
2. The general public and scholarly communities **need** access to an important local and quotidian source to tell and recover local stories
3. Scholarly communities have a duty of care

# Digitisation as the promised solution to all our problems?
## Digitisation != online != accessible

# Workflow / components of OpenArabicPE
## to do

<!-- merge the following section into this nice and conside workflow -->

## 1. get the data

- facsimiles
    + link to existing facsimiles from [British Library's "Endangered Archives Programme" (EAP)](http://eap.bl.uk/), [HathiTrust](http://hathitrust.org/) and [*Arshīf al-majallāt [...] al-ʿarabiyya*](http://archive.alsharekh.org/), preferably through [IIIF](https://iiif.io/)
    + scan/ photograph your physical artefacts (at the lowest sustainable resolution)
- text
    + scrape existing transcriptions from [*shamela.ws*](http://shamela.ws/index.php/book/26523), et al.
    + use [Transkribus](https://transkribus.eu/), [eScripta](https://escripta.hypotheses.org)/[eScriptorium](https://www.https://escriptorium.fr/) for HTR (with our model trained on 1000+ pages from the OpenArabicPE corpus)

## 2. save and share the data

- facsimiles: [Internet Archive](https://archive.org) (supports [IIIF](https://iiif.io/))
- working copy of everything else: distributed version control platforms ([GitHub](https://github.com/), [GitLab](https://about.gitlab.com/))
- longterm preservation: publicly-funded, open repository ([Zenodo](https://zenodo.org/))
    + make sure to add [ORCID](https://orcid.org)s for all contributors
- provide suitable open licenses for re-use: [Creative Commons](https://creativecommons.org/), [MIT]()

## 3. model the data
### This is a scholarly endeavour!

- use open, plain-text file formats<!-- : proprietary formats will cause a lock-in -->
- widely accepted standard for textual editions: [Text Encoding Initiative](https://tei-c.org/) (TEI, serialised as XML)
    - active community
    - pre-requisite for grant funding
- re-use / adapt domain specific encoding schemas within the TEI
- try to script basic modellation using patterns in your source text:
    + regular expressions
    + XSLT, Python, R, whatever you are most comfortable with
- automatically model derivative bibliographic data: MODS, METS, BibTeX, ...

## 4. edit the data

- editing tools depend on modelling decisions and file formats
- make use of version control and stable IDs (e.g. [ORCID](https://orcid.org)) for **transparent authorship attribution** and **damage control**: [.git] is open source and built into some OSs
- plain-text (including XML)
    - support for RTL in free text editors varies between OS
    - use syntax aware text editors
- XML
    - validation of the XML based on schema files
    - There are open, publicly-funded alternatives to [oXygen](): [TextGrid Lab](https://textgrid.de/index)

## 5. disseminate the data <!-- change the title of this slide -->
### presentation layers and access for human readers

:::{.c_width-60}

- Convert XML to static webviews: [TEI Boilerplate](http://dcl.slis.indiana.edu/teibp/), [CETEICEan](https://github.com/TEIC/CETEIcean)
    - on the fly: XSLT1 or JS to render XML files in the client's web browser
    - pre-computed: [GitHub actions](https://github.com/features/actions)
    - removes need for backend, databases etc.
    - minimises traffic
- host webviews, project blogs: [gh-pages](https://pages.github.com/)
- bibliographic database: [Zotero group](https://www.zotero.org/groups/openarabicpe/items/)
    + browse and search independent of file structure
- full-text search: [Google's programmable search engine](https://cse.google.com/cse?cx=012251040084107011117:jof1v_ejndo)

:::
:::{.c_width-30 .c_right}

![[Display of *al-Muqtabas* 6(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png)

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": search in mobile view](../assets/zotero-group_openarabicpe-mobile-search.png)

:::

## 5. disseminate the data
### Zotero group

:::{.c_width-50 .c_left}

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": search in mobile view](../assets/zotero-group_openarabicpe-mobile-search.png)

:::
:::{.c_width-50 .c_right}

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": details in mobile view](../assets/zotero-group_openarabicpe-mobile-details.png)

:::

# Beware: character encoding != rendering

# Beware: Bootstrapping relies on the work of others
## All dependencies will eventually break / need repair

- Reliance on external data providers: link rot
    - links to facsimiles broke twice in four years
- Reliance on free tools and services: link rot
    + URLs to our editions had to be changed once
- XSLT1 in web browsers: will fall victim to JSON and security features
    + over the last 5 years support has markedly decreased
- Full-text search across issues and periodicals without a backend<!-- : **not** available out-of-the-box -->
    + [Google's programmable search engines](https://cse.google.com/cse?cx=012251040084107011117:jof1v_ejndo): requires internet connection (and Google account!)



## 1. Basis: TEI files

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
         :::
    </front>
    <body xml:id="body_1.d1e1485" xml:lang="ar">
        <pb corresp="file:../epub/26523/OEBPS/xhtml/P4092.xhtml" ed="shamela" n="n62-p1" xml:id="pb_1.d1e1487"/>
        <div type="item" subtype="article" xml:id="div_2.d1e1491" xml:lang="ar">
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
                :::
            :::
        :::
    </body>
</text>
```


<!--
## 3.1 Basis: TEI files

![TEI file of *al-Muqtabas* 6(2) in oXygen: author mode](../assets/oxygen_muqtabas-1.png)

-->



## 3.2 Core feature: Continuous improvement

1. Improvements depending on human labour (probably a "crowd")
    - correct the transcription
    - add structural mark-up
    - add semantic mark-up
2. Automatic improvements:
    - provide reliable bibliographic metadata based on the facsimile
    - mark-up of natural entities with link to external reference files (e.g. personal names, toponyms)

## 3.2 Core feature: how to contribute

:::{.c_width-50 .}

- Go to [GitHub](https://www.github.com) and register a free account
- **Fork** the editions' repositories: e.g. <https://www.github.com/openarabicpe/journal_lughat-al-arab>
- Edit the text (XML)
- Send us a **pull request**
- We will review and merge your changes

:::
:::{.c_width-50}>

![](../assets/github_branches-1.png)

:::

## 3.3 Core feature: web-view

![[Display of *al-Muqtabas* 6(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png)

## 3.3 Core feature: web-view

- **open**, **free-of-charge**, **client-based**
- Adaptation of the [TEI Boilerplate XSLT stylesheets](http://dcl.slis.indiana.edu/teibp/) to (Arabic) periodical editions
- static web-view hosted on [gh-pages](https://pages.github.com/)
    + generated on-the-fly by the user's browser using XSLT 1
    + works without an internet connection and with local facsimiles.
- parallel display of text and facsimile
- link to metadata on the article level (MODS, BibTeX)
- Available on [GitHub](https://github.com/tillgrallert/tei-boilerplate-arabic-editions) with a [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/)

## 3.4 Core feature: Zotero group

:::{.c_width-60 .c_left}

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": list view](../assets/zotero-group_openarabicpe-search.png)

:::
:::{.c_width-30 .c_right}

- entry into editions
- search metadata across periodicals
- (potentially) search full-text

:::



<!-- the following still needs work -->
## 3.5 Core feature: preservation, DOI

:::{.c_width-50 .c_left}

|                                   periodical                                  |                               doi                                |                                                                               release                                                                               |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [al-Ḥaqāʾiq](https://www.github.com/openarabicpe/digital-haqaiq)              | [10.5281/zenodo.1232016](https://doi.org/10.5281/zenodo.1232016) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/digital-haqaiq.svg)](https://github.com/openarabicpe/digital-haqaiq/releases)                 |
| [al-Ḥasnāʾ](https://www.github.com/openarabicpe/journal_al-hasna)             | [10.5281/zenodo.3556246](https://doi.org/10.5281/zenodo.3556246) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_al-hasna.svg)](https://github.com/openarabicpe/journal_al-hasna/releases)             |
| [al-Manār](https://www.github.com/openarabicpe/journal_al-manar)              |                                                                  | <!-- [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_al-manar.svg)](https://github.com/openarabicpe/journal_al-manar/releases)  -->   |
| [al-Muqtabas](https://www.github.com/tillgrallert/digital-muqtabas)           | [10.5281/zenodo.597319](https://doi.org/10.5281/zenodo.597319)   | [![GitHub release](https://img.shields.io/github/release/tillgrallert/digital-muqtabas.svg)](https://github.com/tillgrallert/digital-muqtabas/releases)             |
| [al-Ustādh](https://www.github.com/openarabicpe/journal_al-ustadh)            | [10.5281/zenodo.3581028](https://doi.org/10.5281/zenodo.3581028) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_al-ustadh.svg)](https://github.com/openarabicpe/journal_al-ustadh/releases)           |
| [al-Zuhūr](https://www.github.com/openarabicpe/journal_al-zuhur)              | [10.5281/zenodo.3580606](https://doi.org/10.5281/zenodo.3580606) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_al-zuhur.svg)](https://github.com/openarabicpe/journal_al-zuhur/releases)             |
| [Lughat al-ʿArab](https://www.github.com/openarabicpe/journal_lughat-al-arab) | [10.5281/zenodo.3514384](https://doi.org/10.5281/zenodo.3514384) | [![GitHub release](https://img.shields.io/github/release/openarabicpe/journal_lughat-al-arab.svg)](https://github.com/openarabicpe/journal_lughat-al-arab/releases) |

:::
:::{.c_width-50 .c_right}

![Archived release of *al-Muqtabas* on [Zenono](https://doi.org/10.5281/zenodo.597319)](../assets/zenodo_muqtabas.png)

:::

# Conclusion
## Thank you!

- Contributors to OpenArabicPE: Jasper Bernhofer, Dimitar Dragnev, Patrick Funk, Talha Güzel, Hans Magne Jaatun, Jakob Koppermann, Xaver Kretzschmar, Daniel Lloyd, Klara Mayer, Tobias Sick, Manzi Tanna-Händel, and Layla Youssef
- Links:
    + Slides: [https://OpenArabicPE.github.io/slides/2020-dh-jamia/](https://OpenArabicPE.github.io/slides/2020-dh-jamia/index.html)
    + Project URLs: [https://www.github.com/OpenArabicPE](https://www.github.com/OpenArabicPE)
    + Project blog: [https://openarabicpe.github.io](https://openarabicpe.github.io)
    + Twitter: @[tillgrallert](https://twitter.com/tillgrallert)
    + Email: <grallert@orient-institut.org> <till.grallert@fu-berlin.de>
- Licence: slides and images are licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)
