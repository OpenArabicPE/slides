---
title: "Digital Muqtabas CTS Integration in CLARIN"
author: Till Grallert
date: 2017-09-15 16:17:48 +0300
duration: 6
---

# The journal of *al-Muqtabas*

*al-Muqtabas* / المقتبس

- "monthly" journal published by Muḥammad Kurd ʿAlī between 1906 and 1918/19 in Cairo and, from 1908 onwards, in Damascus.
    + 9 volumes, 96 issues <!-- (at least 2 double issues),  -->, c. 7000 pages
    + 3.851.614 tokens (words), 5042 articles, [136 named authors](../assets/muqtabas_word-cloud.html)
- Muḥammad Kurd ʿAlī (1876-1952): Ottoman bureaucrat, journalist, president of the Syrian Academy of Sciences, minister of education.
- available at c. 30 libraries (North America, Europe, Middle East):
    + original prints (mostly incomplete)
    + some copies of a "gray" reprint
    + a number of microfiche copies from a single source

# Importance of mundane texts / periodicals

- They are at the core of various discourses
    + Modernity / -ism at the end of empire
    + Arabic renaissance
    + Arab nationalism
    + Islamic reform movement
- They form large corpora with an equal distribution along a temporal axis (*al-Muqtabas*: 12 yrs, *al-Manār*: 43 yrs, *al-Muqtaṭaf*: 76 yrs)
    + linguistic analysis
    + historical semantics
    + rich data sets for social history

# Digitisation

- promises:
    + access
    + preservation
- challenges:
    - no reliable Arabic OCR
    - lack of funding

# State of digitisation

1. Text: "crowd"-sourced transcriptions / gray online libraries, e.g. [*al-Maktaba al-Shāmila*](http://shamela.ws/index.php/book/26523), [*Mishkāt*](http://almeshkat.net/), [*Ṣayd al-Fawāʾid*](http://saaid.net/), [*al-Waraq*](http://www.alwaraq.net/) etc.
    + lack of / faulty metadata
    + unknown editing principles
    + unknown quality
    + very limited structural mark-up
    + cannot be reliably cited
2. Digital imagery, e.g. [Endangered Archives Programme (EAP)](http://eap.bl.uk/database/overview_project.a4d?projID=EAP119;r=63), [HathiTrust](http://catalog.hathitrust.org/Record/100658549), [Institut du Monde Arabe](http://ima.bibalex.org/IMA/presentation/periodic/list.jsf?pid=9C82C139F9785E99D30089727B40A269).
    + lack of metadata
    + limited licences, paywalls
    + no or very bad text layers
3. Metadata search within and across periodicals: **inexistent**

# [Digital *Muqtabas* (2015-)](https://www.github.com/tillgrallert/digital-muqtabas): unite transcription and facsimiles

1. aims
    + **validate** the transcription against the facsimiles
    - **improve** the transcription with the help of the "crowd"
    - make everything **citable** for scholars, **linkable** for machines
    - provide the new edition with the broadest possible licence to facilitate access and re-use
2. principles
    - re-purpose **available** and **established** tools, technologies, and material
    - preference for **open** and **simple** formats and tools

# [Digital *Muqtabas* (2015-)](https://www.github.com/tillgrallert/digital-muqtabas): deliverables

- open scholarly digital editions of *[Majallat] al-Muqtabas* <!-- and *al-Ḥaqāʾiq* --> providing
    + TEI XML files (transcription and links to facsimiles)
    + plain text files (markdown)
    + MODS and BibTeX files for every article
    + [customised version of TEI Boilerplate](https://github.com/tillgrallert/tei-boilerplate-arabic-editions) (XSLT and CSS) with stable URLs for every element ([example](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml))
    + access to bibliographic metadata through a public [Zotero group (OpenArabicPE/digital-muqtabas)](https://www.zotero.org/groups/904125/openarabicpe/items/collectionKey/8SINFUW9)
- within a framework (git, [GitHub](https://github.com/openarabicpe/journal_al-muqtabas), [Zenodo](https://zenodo.org)) that allows for / provides
    + collaborative, open, version-controlled improvements of the edition
    + re-use through open licences:[CC0](https://creativecommons.org/publicdomain/zero/1.0/) (text, metadata), [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/) (edition), and [MIT licence](https://en.wikipedia.org/wiki/MIT_License) (tools)
    + long-term preservation and DOIs ([10.5281/zenodo.597319](https://doi.org/10.5281/zenodo.597319))

# [Digital *Muqtabas* (2015-)](https://www.github.com/tillgrallert/digital-muqtabas): current state

- Project evolved into "Open Arabic Periodical Editions" ([OpenArabicPE](https://openarabicpe.github.io))
- Editorial decisions: modelling / TEI schema design
    <!-- + mark-up of some text features has not yet been decided -->
- Editorial work:
    + mark-up of page breaks (1-2 h per issue)
    + add parts missing from transcription (all foreign words and footnotes, entire pages)
    + correct transcription
    + correct publication dates for all issues.
- Web-display:
    + needs some polishing
    + search functions beyond the Zotero group and individual issues
