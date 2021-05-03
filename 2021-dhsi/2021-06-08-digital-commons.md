---
title: "Open Arabic Periodical Editions"
subtitle: "Contributing to the *digital commons* without the help we cannot get"
author: Till Grallert
date: 2021-04-30
ORCID: orcid.org/0000-0002-5739-8094
duration: 10
---

## Open Arabic Periodical Editions
### Contributing to the *digital commons* without the help we cannot get

Till Grallert, @[tillgrallert](https://twitter.com/tillgrallert)

Third Right to Left (#RTL21) conference at #DHSI21

Slides: [https://OpenArabicPE.github.io/slides/2021-dhsi/](https://OpenArabicPE.github.io/slides/2021-dhsi/index.html)

## Open Arabic Periodical Editions ([OpenArabicPE](https://openarabicpe.github.io))

:::{.c_width-60 .c_left}

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
:::{.c_width-30 .c_right}

![[Webview of *al-Muqtabas* 3(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_26.TEIP5.xml)](../assets/boilerplate_muqtabas-v_3-i_2.png){#fig:webview-muqtabas}

![[Webview of *al-Zuhur* 1(1)](https://openarabicpe.github.io/journal_al-zuhur/tei/oclc_1034545644-i_1.TEIP5.xml)](../assets/boilerplate_zuhur-v_1-i_1.png){#fig:webview-zuhur}

:::

## Why spend the effort? Shouldn't others do it?

OpenArabicPE addresses a clear need, fundamental rights, and our scholarly duties:

1. Societies of the Global South have a **right** to unhampered access to their **own cultural record**---a cultural record that is frequently held by institutions of the Global North---and **on their own terms**
2. The general public and scholarly communities **need** access to an important local and quotidian source to tell and recover local stories
3. Scholarly communities have a duty of care and nobody else was doing it

## Neo-colonial invisibility of the Global South

:::{.c_width-50}

### Historical Arabic periodicals

- cultural heritage of 420 Mio Arabic-speakers
- 3269 journals and newspapers until 1929
- collection and cataloging bias:
    + 747 (< 1/4 ) can be localised
    + including partial collections
- digitisation bias:
    + 145 (< 1/20) titles have been (partially) digitised
- accessibility:
    + paywalls
    + geo-fencing
    + proprietary interfaces/formats, no APIs
    + non-Arabic interfaces and metadata


<!-- ![In Project Jarāʾid erfasste Periodika](../../assets/jaraid/jaraid_holdings_pie-3.png){#fig:jaraid-stats width="300"} -->

:::
:::{.c_width-50}

### Historical periodicals from a small German state

"[WWI as mirrored by Hessian regional papers](https://hwk1.hebis.de)"

- cultural heritage of 6.2 Mio inhabitants of Hesse
- 125 digitised titles with more than 1/2 Mio pages
    - facsimiles and full text
- accessibility
    + open access
    + standard compliant formats
    + APIs
    + German and English interfaces

:::

## Digitisation != online != accessible

<!-- outline problems -->

:::{.c_width-50}

### Facsimiles

+ lack of / faulty metadata
+ data silos
    + limited licences, paywalls
    + limited use of standards, APIs
+ UIs not suited to RTL and limited to English

:::{.c_height-50 .c_bottom}

![[*al-Muqtabas* 6 on HathiTrust without US IP](http://hdl.handle.net/2027/njp.32101073250910)](../assets/hathi_muqtabas-1.png)

:::
:::
:::{.c_width-50 .c_right}

### Text

- Automated transcriptions (OCR): [HathiTrust](https://www.hathitrust.org/), East View's [Global Press Archive (GPA)](https://www.eastview.com/resources/gpa/crl-mena/), [Cengage Gale](http://gale.cengage.co.uk/arabic.aspx)
    + unknown quality but commonly extremly bad
    + no structural mark-up
<!-- + data silos
    + limited licences, paywalls
    + limited use of standards, APIs
 -->

:::{.c_height-50 .c_bottom}

![*al-Bashīr* 9 Jan. 1880 (#487), p.1 on [GPA](https://gpa.eastview.com/crl/mena/newspapers/bshr18800109-01.1.1), state of OCR](../assets/gpa_bashir-i_487-p_1_ocr.png)

:::
:::

## Shadow libraries

<!-- outline problems -->

:::{.c_width-50}

### Fakesimiles

- Renderings of a digital text with a fake "original" layout
- served as image file

:::{.c_height-50 .c_bottom}

!["fakesimile" of *al-Muqtabas* 5(7) from [*arshīf al-majallāt [...] al-ʿarabiyya*](https://archive.alsharekh.org/MagazinePages/Magazine_JPG/AL_moqtabs/Al_moqtabs_1910/Issue_7/605.JPG). Large parts of text have been omitted. The original spans pp.[463](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_54.TEIP5.xml#pb_61.d1e2036)--[466](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_54.TEIP5.xml#pb_64.d1e2045).](../assets/sakhrit_muqtabas-v_5-i_7-p_605.jpg)
:::
:::
:::{.c_width-50 .c_right}

### Text

- anonymous transcriptions,  e.g. [*al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523), [*Mishkāt*](http://almeshkat.net/), [*Ṣayd al-Fawāʾid*](http://saaid.net/), [*al-Waraq*](http://www.alwaraq.net/) etc.
    + lack of / faulty metadata
    + unknown editing principles
    + unknown quality
    + very limited structural mark-up
    + cannot be reliably cited

:::{.c_height-50 .c_bottom}

![[*al-Muqtabas* on *al-Maktaba al-Shāmila*](http://shamela.ws/browse.php/book-26523#page-4046)](../assets/shamela_muqtabas-annotated.png)

:::
:::

# Contributing to the *digital commons* without the help we cannot get
##  Contributing to the *digital commons* without the help we cannot get <!-- Aims and principles --> <!-- move further down into the workflow section -->

::: {.c_width-30}

### ideas:

- unite **available** facsimiles and transcriptions
- harvest, generate, validate and share open metadata

:::
::: {.c_width-30}

### aims

<!-- + **validate** and **improve** the transcription with the facsimiles
- **train** text and layout recognition algorithms to make the textual heritage accessible to digitisation efforts
- **citable** for scholars, **linkable** for machines to facilitate use and adoption of the resources
- **open licences** to facilitate re-use -->

- **Validation** and utilization of transcriptions
- Establishing an open **infrastructure** of workflows, models, authority files
- With the affordances of the Global South

:::
::: {.c_width-30}

### principles

- **established** tools and technologies
- as **few** as possible **open** and "simple" formats and tools
- **free-to-use** platforms without lock-in of data

:::

## Affordances and constrains

::: {.c_width-60}

### General

- socio-technological hegemony of the Global North
    + hardware, software, formats ill-suited for the digitised cultural heritage of the Global South
- cultural hegemony of the English-speaking Global North
    + dominates the interfaces between humans and machines
    + decides how we can describe cultural artefacts in the digital domain
    + involves: language and script, metaphors, semantic models

:::
::: {.c_width-30}

### Project specific

- no institutional funding
- volatile electricity
- slow and expensive internet connection

:::

# Workflow / components of OpenArabicPE

## 1. get the data

:::{.c_width-50}

- text
    + scrape existing transcriptions from [*shamela.ws*](http://shamela.ws/index.php/book/26523), et al.
    + use [Transkribus](https://transkribus.eu/), [eScripta](https://escripta.hypotheses.org)/[eScriptorium](https://www.https://escriptorium.fr/) for HTR (with our model trained on 1000+ pages from the OpenArabicPE corpus)
- facsimiles
    + link to existing facsimiles from [British Library's "Endangered Archives Programme" (EAP)](http://eap.bl.uk/), [HathiTrust](http://hathitrust.org/), [Translatio Bonn](https://digitale-sammlungen.ulb.uni-bonn.de/topic/view/3085779), [*Arshīf al-majallāt [...] al-ʿarabiyya*](http://archive.alsharekh.org/) etc., preferably through [IIIF](https://iiif.io/)
    + scan/ photograph your physical artefacts (at the lowest sustainable resolution)

:::
:::{.c_width-50 .c_right}

EPub (HTML) for *al-Zuhūr* 2(4) from shamela.ws

```{.html}
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

:::

## 2. model the data
### This is a scholarly endeavour!

:::{.c_width-50}

- use open, plain-text file formats<!-- : proprietary formats will cause a lock-in -->
- widely accepted standard for textual editions: [Text Encoding Initiative](https://tei-c.org/) (TEI, serialised as XML)
    - active community
    - pre-requisite for grant funding
- re-use / adapt domain specific encoding schemas within the TEI
- try to script basic modelling using patterns in your source text:
    + regular expressions
    + XSLT, Python, R, whatever you are most comfortable with
- automatically model derivative bibliographic data: MODS, METS, BibTeX, ...

:::
:::{.c_width-50 .c_right}

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

:::

## 3. edit the data

:::{.c_width-50}

- editing tools depend on modelling decisions and file formats
- make use of version control <!-- and stable IDs (e.g. [ORCID](https://orcid.org)) --> for **transparent authorship attribution** and **damage control**: [.git](https://git-scm.com/) is open source and available for all OSs
- plain-text (including XML) editors
    + should be **syntax aware**
    - RTL: support in text editors is a mixed bag
- XML
    + should be **schema aware** to validate the encoding
    - RTL: There seems to be no way around [oXygen XML editor](https://www.oxygenxml.com/)<!-- : [TextGrid Lab](https://textgrid.de/index) -->

:::
:::{.c_width-50 .c_right}

![The TEI XML file for *al-Zuhūr* 2(4) in [Sublime Text](https://www.sublimetext.com/)](../assets/sublime_zuhur.png)

![The TEI XML file for *al-Zuhūr* 2(4) in [TextMate](https://macromates.com/)](../assets/textmate_zuhur.png)

:::

## 4. save and share the data

:::{.c_width-50}

- facsimiles: [Internet Archive](https://archive.org) (supports [IIIF](https://iiif.io/))
- working copy of everything else: distributed version control platforms ([GitHub](https://github.com/), [GitLab](https://about.gitlab.com/))
- longterm preservation: publicly-funded, open repository ([Zenodo](https://zenodo.org/))
    + make sure to add [ORCID](https://orcid.org)s for all contributors
- provide suitable open licenses for re-use: [Creative Commons](https://creativecommons.org/), [MIT]()

:::
:::{.c_width-50 .c_right}

![Archived release of *al-Zuhūr* on [Zenono](https://doi.org/10.5281/zenodo.3580606)](../assets/zenodo_zuhur.png)

:::

## 5. present the data <!-- change the title of this slide -->
<!-- ### presentation layers and access for human readers -->

:::{.c_width-50}

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
:::{.c_width-50 .c_right}

![[Webview of *al-Zuhūr* 2(4)](https://openarabicpe.github.io/journal_al-zuhur/tei/oclc_1034545644-i_15.TEIP5.xml#div_1.d2e634)](../assets/boilerplate_zuhur-v_2-i_4.png)

<!-- ![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": search in mobile view](../assets/zotero-group_openarabicpe-mobile-search.png) -->

:::

## 5. present the data
### Zotero group

:::{.c_width-50 .c_left}

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": search in mobile view](../assets/zotero-group_openarabicpe-mobile-search.png)

:::
:::{.c_width-50 .c_right}

![Zotero group "[OpenArabicPE](https://www.zotero.org/groups/openarabicpe/items/)": details in mobile view](../assets/zotero-group_openarabicpe-mobile-details.png)

:::

# Beware: character encoding != rendering
## Separate encoding and content during editing

... or learn how to navigate bi-directional XML and read Arabic from left to right.

:::{.c_width-50 .c_left}

![The TEI XML file for *al-Zuhūr* 2(4) in [Sublime Text](https://www.sublimetext.com/)](../assets/sublime_zuhur.png)

:::
:::{.c_width-50 .c_right}

![The TEI XML file for *al-Zuhūr* 2(4) in [oXygen](https://www.oxygenxml.com/)'s  author mode. Styling relies on CSS.](../assets/oxygen_zuhur-author.png)

:::

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


# Conclusion
## Thank you!

- Contributors to OpenArabicPE: Jasper Bernhofer, Dimitar Dragnev, Patrick Funk, Talha Güzel, Hans Magne Jaatun, Jakob Koppermann, Xaver Kretzschmar, Daniel Lloyd, Klara Mayer, Tobias Sick, Manzi Tanna-Händel, and Layla Youssef
- Links:
    + Slides: [https://OpenArabicPE.github.io/slides/2021-dhsi/](https://OpenArabicPE.github.io/slides/2021-dhsi/index.html)
    + Project URLs: [https://www.github.com/OpenArabicPE](https://www.github.com/OpenArabicPE)
    + Project blog: [https://openarabicpe.github.io](https://openarabicpe.github.io)
    + Twitter: @[tillgrallert](https://twitter.com/tillgrallert)
    + Email: <till.grallert@fu-berlin.de>
- Licence: slides and images are licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)
