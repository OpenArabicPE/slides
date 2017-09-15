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
    + 3.851.614 tokens (words), 5042 articles, 136 named authors
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

# [Digital *Muqtabas*](https://www.github.com/tillgrallert/digital-muqtabas): unite transcription and facsimiles

1. aims
    + **validate** the transcription against the facsimiles
    - **improve** the transcription with the help of the "crowd"
    - make everything **citable** for scholars, **linkable** for machines
    - provide the new edition with the broadest possible licence to facilitate access and re-use 
2. principles
    - re-purpose **available** and **established** tools, technologies, and material
    - preference for **open** and **simple** formats and tools

# [Digital *Muqtabas*](https://www.github.com/tillgrallert/digital-muqtabas)

1. Basis: open-access digital scholarly edition
    - XML/TEI files of all 96 issues
    - links to digital facsimiles
    - licenced as [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)
2. Core feature: social edition
    - gradually improve text and mark-up: [GitHub](https://github.com/tillgrallert/digital-muqtabas)
    - releases are archived at [Zenodo](https://zenodo.org) and receive a DOI ([10.5281/zenodo.597319](https://doi.org/10.5281/zenodo.597319))
3. Sugar on top: 
    - Static web-view (doesn't require a permanent internet connection)
    - bibliographic metadata for all issues and articles (MODS, BibTeX)
    - access to bibliographic metadata through a public [Zotero group (OpenArabicPE/digital-muqtabas)](https://www.zotero.org/groups/904125/openarabicpe/items/collectionKey/8SINFUW9)