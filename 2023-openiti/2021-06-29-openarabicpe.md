---
title: "Open Arabic Periodical Editions (OpenArabicPE)"
subtitle: "a case study in digital editing outside the Global North"
author: Till Grallert
institute: 
    - Humboldt-Universität zu Berlin
    - Methods Innovation Lab (NFDI 4Memory)
    - Scholarly Makerspace (University Library)
date: 2023-06-29
event: "Digital Publication of Right-to-Left Script Corpora"
url: https://openarabicpe.github.io/slides/2023-openiti/
ORCID: orcid.org/0000-0002-5739-8094
lang: en
bibliography: 
    - /Users/Shared/BachUni/research-projects/OpenArabicPE/assets/bibliography/openarabicpe.csl.json
    - /Users/Shared/BachUni/applications/applications.csl.json
slide-level: 2
license: https://creativecommons.org/licenses/by-sa/4.0/
nocite: |
    @RisamGil2022Introduction; @Gil+2016; 
    @Grallert2022DHQ; @Grallert2021GG; @MestyanEtAl2020JaraidDataset
---

## Open Arabic Periodical Editions ([OpenArabicPE](https://openarabicpe.github.io))

::: columns
:::: wide

- Volunteer-run scholarly editing and infrastructure-building (since 2015)
- Digital scholarly editions
    + 6 Arabic magazines from Baghdad, Cairo, Damascus with c.800 issues and more than 9 million words.
    + full text and facsimiles modelled in TEI XML
    - Bibliographic metadata (MODS, BibTeX, Zotero RDF)
       <!--  - on the article level for the entire corpus plus 2 additional magazines
        - on the issue level for 7 additional newspapers
        - on the title level for 3300+ periodicals (in collaboration with [Project Jarāʾid](https://projectjaraid.github.io)) -->
- Infrastructure:
    + static websites without a backend / database
    + free hosting and archiving
    - [Zotero group](https://zotero.org/groups/openarabicpe) as gateway to search/browse the corpus
- Workflows and tools

::::
:::: narrow

![[Webview of *al-Zuhur* 1(1)](https://openarabicpe.github.io/journal_al-zuhur/tei/oclc_1034545644-i_1.TEIP5.xml)](../assets/boilerplate_zuhur-v_1-i_1.png){#fig:webview-zuhur}

![[Webview of *al-Muqtabas* 3(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_26.TEIP5.xml)](../assets/boilerplate_muqtabas-v_3-i_2.png){#fig:webview-muqtabas}

::::
:::

# Why spend the effort? <br/> Shouldn't others do it?
## Why spend the effort?

::: columns
:::: wide

1. Neo-colonial invisibility of cultural artefacts from the Global South in the digital domain
    - knowledge gap, collection and cataloguing bias -> digitisation bias
2. Periodicals are an important local and quotidian source to tell and recover local stories
3. We as scholars have a duty of care and nobody else was doing it

::::
:::: narrow


|      periodicals       | --1918 |       | --1929 |               |
|  :-------------------  | ----:  | ----: | ----:  |     ----:     |
|       published        |  2054  |       |  3550  |               |
|     known holdings     |  540   |       |  775   |               |
|       % of total       |        | 26.29 |        | [21.83]{.red} |
|------------------------|--------|-------|--------|---------------|
| digitized              |    156 |       |    233 |               |
| % of total             |        |  7.59 |        | [6.56]{.red}  |
|------------------------|--------|-------|--------|---------------|
| multiple digitisations |     51 |       |     66 |               |
| % of total             |        |  2.48 |        | 1.86          |
| % of digitised         |        | 32.69 |        | [28.33]{.red} |

Table: Periodical holdings and digitization {#tbl:jaraid-holdings}

::::
:::

![Geographic distribution of library holdings of *al-Muqtabas*](../assets/maps/map-oclc_4770057679-holdings-vol_1-9.png)


# Contributing to the *digital commons* without the help we can't get
##  The help we can't get


::: columns
:::: column

- digitisation and maintaining digital artefacts is really **expensive**
- periodicals form an extremely **large corpus** of very short texts (and images)
- lacking technologies*
    - OCR for Arabic script
    - automated layout recognition
- no institutional funding for the digitisation of mundane bulk of the periodical press

::::
:::: column

- existing digitised periodicals are nigh unusable
    + lacking/faulty metadata
    + mainly facsimiles
    + unknown veracity of text layers
    + paywalls, geofencing
    + no APIs
    + no machine-actionable data layer

::::
:::


::: columns-3
:::: column

![*al-Muqtabas* 6 on [HathiTrust](http://hdl.handle.net/2027/njp.32101073250910) with geo-fencing](../assets/hathi_muqtabas-1.png)

::::
:::: column

![*al-Bashīr* 9 Jan. 1880 (#487), p.1 on [GPA](https://gpa.eastview.com/crl/mena/newspapers/bshr18800109-01.1.1), state of OCR](../assets/gpa_bashir-i_487-p_1_ocr.png)

::::
:::: column

![*al-Muqtabas* on [*al-Maktaba al-Shāmila*](http://shamela.ws/browse.php/book-26523#page-4046)](../assets/shamela_muqtabas-annotated.png)

::::
:::

## Contributing to the *digital commons* <br/> without the help we can't get

::: columns
:::: column

### ideas

- unite **existing** gray transcriptions with digital facsimiles
- learn from free and open-source software development
<!-- - model everything to make components citable
- harvest, generate, validate and share open metadata -->


### minimal computing principles

- build what **we need** with what **we have** at hand
- as **few** as possible, **open** and **established** formats and tools
- running on **our** hardware
- with **our** skills and knowledge
- **free-to-use** platforms without lock-in of data

::::
:::: column

### aims

<!-- + **validate** and **improve** the transcription with the facsimiles
- **train** text and layout recognition algorithms to make the textual heritage accessible to digitisation efforts
- **citable** for scholars, **linkable** for machines to facilitate use and adoption of the resources
- **open licences** to facilitate re-use -->

- make Arabic periodicals **accessible** on a shoestring budget
- **validate** and improve utilization of transcriptions
    + reliablity: content and citations
    + accessibility: for readers and computational analysis
    + ground truth for ML-based OCR/HTR
- establish an open, sustainable **infrastructure** of workflows, models, authority files
<!-- - With the affordances of the Global South -->

::::
:::

::: notes

- minimal computing
- meaningful connectivity: focus on practicability instead of principled stance
- result: bootstrapped scholarly editions

:::

# Resulting workflow of OpenArabicPE
## 1. get the data

::: columns
:::: column

- facsimiles
    + link to existing facsimiles from [British Library's "Endangered Archives Programme" (EAP)](http://eap.bl.uk/), <!-- [HathiTrust](http://hathitrust.org/), --> [Translatio Bonn](https://digitale-sammlungen.ulb.uni-bonn.de/topic/view/3085779), [*Arshīf al-majallāt [...] al-ʿarabiyya*](http://archive.alsharekh.org/) etc., preferably through [IIIF](https://iiif.io/)
    + scan/ photograph your physical artefacts (at the lowest sustainable resolution)
- text
    + scrape existing transcriptions from [*shamela.ws*](http://shamela.ws/index.php/book/26523), et al.
    + use [Transkribus](https://transkribus.eu/), [eScripta](https://escripta.hypotheses.org)/[eScriptorium](https://www.https://escriptorium.fr/) for HTR (with our model trained on 1000+ pages from the OpenArabicPE corpus)


::::
:::: column

EPub (HTML) for *al-Zuhūr* 2(4) from shamela.ws

```html
<div dir="rtl" id="book-container">
    <hr/>
    <a id='C232'></a>
    <span class="title">صحافة سورية ولبنان</span><br /><span class="red">3 - </span>المجلات<br />هذه مقالتي الثالثة عن صحافة سورية ولبنان. . . ولا يخفى أن للانقلاب العثماني الأخير فضلاً عظيماً على هذه المجلات التي أنا ذاكر. فمل يكن منها قبل إعلان الدستور إلا مجلة المشرق ومجلة المقتبس.<br />أما بقية المجلات فقد صدرت في العامين الأخيرين كما يظهر لك في هذا المقال.<br />وقد اجتهدت، في هذا القسم، أن أذكر تاريخ صدور لهذه المجلات متخيراً أوثق المصادر في ذلك فأقول:<br />
</div>
```

OCR output from Transkribus for *al-Ḥasnāʾ* (PAGE XML)

```xml
<TextLine id="r1l5" custom="readingOrder {index:4;}">
    <Coords points="470,548 2191,527 1648,462 470,464"/>
    <Baseline points="480,542 565,540 650,537 735,534 820,533 905,531 990,530 1075,528 1160,528 1245,527 1330,527 1415,527 1500,527 1585,527 1670,528 1755,528 1840,530 1925,531 2010,531 2095,534 2180,536"/>
    <TextEquiv>
        <Unicode>من عسر سنوات مجلة بسائة في الاستارة اعتمد في تحريرها على أقلامهن فزيئها</Unicode>
    </TextEquiv>
</TextLine>
```
::::
:::

::: notes

- IIIF allows to set a very low quality to reduce bandwidth and traffic
- what do you need to know
    - HTML
    - XML
    - JSON: for IIIF
    - wget, cURL: for scraping

:::

## 2. model the data

Structure the text string into issues, sections, articles with bylines ...

::: columns
:::: column

- widely accepted standard for textual editions: [Text Encoding Initiative](https://tei-c.org/) (TEI XML)
    - active community
    - pre-requisite for grant funding
    - easy to archive (XML = plain text)
- re-use / adapt domain specific encoding schemas within the TEI
- try to script basic modelling using patterns in your source text:
    + regular expressions
    + XSLT, Python, R, whatever you are most comfortable with
- automatically model derivative bibliographic data: MODS, METS, BibTeX, ...

::::
:::: column

The same section of *al-Zuhūr* 2(4) modelled in TEI

```xml
<body xml:lang="ar">
<pb corresp="../epub/shamela_36534/OEBPS/xhtml/P744.xhtml" ed="shamela" n="n2-p184"/>
<pb ed="print" edRef="#edition_1" facs="#facs_184" n="184"/>
    <div prev="oclc_1034545644-i_13.TEIP5.xml#div_1.d2e2766" subtype="article" type="item" xml:id="div_1.d2e634">
        <head>صحافة <placeName>سورية</placeName> و<placeName>لبنان</placeName></head>
        <div type="section" xml:id="div_3.d2e1200">
            <head> ٣ - المجلات</head>
            <p>هذه مقالتي الثالثة عن صحافة سورية ولبنان. . . ولا يخفى أن للانقلاب العثماني الأخير فضلاً عظيماً على هذه المجلات التي أنا ذاكر. فلم يكن منها قبل إعلان الدستور إلا <bibl>مجلة <title level="j">المشرق</title></bibl>  و<bibl>مجلة <title level="j">المقتبس</title></bibl> .</p>
            <p>أما بقية المجلات فقد صدرت في العامين الأخيرين كما يظهر لك في هذا المقال.</p>
            <p>وقد اجتهدت، في هذا القسم، أن أذكر تاريخ صدور لهذه المجلات متخيراً أوثق المصادر في ذلك فأقول:</p>
        </div>
    </div>
</body>
```

::::
:::

::: notes

- why TEI?
    + I knew it already
    + widely adopted standard in the digital editing world
    + necessary for grant-funding in the Global North
- why not TEI
    + steep learning curve
    + not particularly well-suited to Arabic texts?

:::

## 3. edit the data

::: columns
:::: column

- make use of version control <!-- and stable IDs (e.g. [ORCID](https://orcid.org)) --> for **transparent authorship attribution** and **damage control**:
    + [.git](https://git-scm.com/) is open source and available for all OSs
- plain-text (including XML) editors
    + should be **syntax aware**
    - **RTL**: support in text editors is a mixed bag

![The TEI XML file for *al-Zuhūr* 2(4) in [Visual Studio Code](https://code.visualstudio.com/)](../assets/vscode_zuhur.png){#fig:zuhur-vscode}

<!-- ![The TEI XML file for *al-Zuhūr* 2(4) in [Sublime Text](https://www.sublimetext.com/)](../assets/sublime_zuhur.png) -->

<!-- ![The TEI XML file for *al-Zuhūr* 2(4) in [TextMate](https://macromates.com/)](../assets/textmate_zuhur.png) -->

::::
:::: column

- XML editors proper
    + should be **schema aware** to validate the encoding
    - **RTL**:
        1. [oXygen XML editor](https://www.oxygenxml.com/) (99 USD) allows to separate content and tags<!-- : [TextGrid Lab](https://textgrid.de/index) -->
        2. [Visual Studio Code](https://code.visualstudio.com/) (free) with the right extensions is a viable second

![The TEI XML file for *al-Zuhūr* 2(4) in [oXygen](https://www.oxygenxml.com/)'s  author mode. Styling relies on CSS.](../assets/oxygen_zuhur-author.png){#fig:zuhur-oxygen}

::::
:::

::: notes

- editing tools depend on modelling decisions and file formats

:::

## 4. save and share the data

::: columns
:::: column

- facsimiles: [Internet Archive](https://archive.org) (supports [IIIF](https://iiif.io/))
- working copy of everything else: distributed version control platforms ([GitHub](https://github.com/), [GitLab](https://about.gitlab.com/))
- longterm preservation: publicly-funded, open repository ([Zenodo](https://zenodo.org/))
    + make sure to add [ORCID](https://orcid.org)s for all contributors
- authority data (people, titles, etc.): [Wikidata](https://wikidata.org/)
- provide suitable open licenses for re-use: [Creative Commons](https://creativecommons.org/), [MIT](), Public Domain (CC0)

::::
:::: column

![Archived release of *al-Zuhūr* on [Zenono](https://doi.org/10.5281/zenodo.3580606)](../assets/zenodo_zuhur.png){#fig:zuhur-zenodo}

::::
:::

## 5. present the data
<!-- ### presentation layers and access for human readers -->

::: columns
:::: column

- Hosting: [GitHub Pages](https://pages.github.com/) can expose your data repository to the web
- Generate static webviews
    + removes need for backend and minimises traffic
    + easy to archive
    - on the fly: XSLT1 ([TEI Boilerplate](http://dcl.slis.indiana.edu/teibp/)) or JS ([CETEICEan](https://github.com/TEIC/CETEIcean)) to render XML files in the client's web browser
    - pre-computed: [GitHub actions](https://github.com/features/actions) give access to virtual machines
- bibliographic database: [Zotero group](https://www.zotero.org/groups/openarabicpe/items/)
    + mitigates against the absent backend
    + **browse** and **search** independent of file structure
- full-text search across the entire corpus: [Google's programmable search engine](https://cse.google.com/cse?cx=012251040084107011117:jof1v_ejndo)

::::
:::: column


![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": details in mobile view](../assets/zotero-group_openarabicpe-mobile-details_small.png){#fig:zuhur-zotero}

![[Webview of *al-Zuhūr* 2(4)](https://openarabicpe.github.io/journal_al-zuhur/tei/oclc_1034545644-i_15.TEIP5.xml#div_1.d2e634)](../assets/boilerplate_zuhur-v_2-i_4_small.png){#fig:zuhur-webview}

<!-- ![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": search in mobile view](../assets/zotero-group_openarabicpe-mobile-search.png) -->

::::
:::

# Conclusion
## All dependencies will eventually break / need repair

::: columns
:::: column

- Reliance on external data providers: link rot
    - links to facsimiles broke twice in four years
- Reliance on free tools and services: link rot
    + URLs to our editions had to be changed once
- XSLT1 in web browsers: will fall victim to JSON and security features
    + over the last 5 years support has markedly decreased
<!-- - Full-text search across issues and periodicals without a backend
    + [Google's programmable search engines](https://cse.google.com/cse?cx=012251040084107011117:jof1v_ejndo): requires internet connection (and Google account!) -->

::::
:::: column

![The main components of OpenArabicPE](../assets/OpenArabicPE_components-layer-1-4.png)

::::
:::


::: notes

Bootstrapping relies on the work of others


:::

## Thank you!

- Contributors to [OpenArabicPE][openarabicpe_website]: Jasper Bernhofer, Dimitar Dragnev, Patrick Funk, Talha Güzel, Hans Magne Jaatun, Daniel Kolland, Jakob Koppermann, Xaver Kretzschmar, Daniel Lloyd, Klara Mayer, Tobias Sick, Manzi Tanna-Händel, and Layla Youssef
- Contributors to [Project Jarāʾid][jaraid_website]: Hala Auji, Philippe Chevrant, Marina Demetriadou, Lamia Eid, Stacy Fahrenthold, Ulrike Freitag, Till Grallert, Rana Issa, Nicole Khayat, Peter Magierski, Leyla von Mende, Adam Mestyan, Christian Meier, Daniel Newman, Geoffrey Roper, Sinai Rusinek, Philip Sadgrove, Ola Seif, and Rogier Visser
- Links:
    + Slides: [https://tinyurl.com/dighis23-grallert](https://tillgrallert.github.io/slides/dh/2023-regensburg/index.html)
    + Project blog: [https://openarabicpe.github.io](https://openarabicpe.github.io)
    + Papers: <http://digitalhumanities.org/dhq/vol/16/2/000593/000593.html>, <https://doi.org/10/gkhrjr>
    + Mastodon: [\@tillgrallert\@digitalcourage.social](https://digitalcourage.social/@tillgrallert)
    + Email: <till.grallert@fu-berlin.de>, <till.grallert@hu-berlin.de>
- Licence: slides and images are licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)

## References {#refs}