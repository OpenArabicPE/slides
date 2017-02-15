---
title: "Digital *Muqtabas*"
author: Till Grallert
date: December 17, 2015
cover-image: images/digital-muqtabas-screenshot.png
---

<!-- Mention Bassel Khartabil / Bāsil Kharṭabīl
    + OA, CC in Syria
    + detained by the regime since 2012
    + moved to an unknown site and probably killed since Oct 2015 -->

# The journal *al-Muqtabas* between Shamela.ws, HathiTrust, and GitHub: producing open, collaborative, and fully-referencable digital editions of early Arabic periodicals—with almost no funds.

Project URL: [https://www.github.com/tillgrallert/digital-muqtabas](https://www.github.com/tillgrallert/digital-muqtabas)

Slides: [http://tillgrallert.github.io/Slides/DHLeipzig2015](http://tillgrallert.github.io/Slides/DHLeipzig2015)

Twitter: @tillgrallert

Email: <grallert@orient-institut.org>

# 1.1 Importance of mundane texts / periodicals

- They are at the core of various discourses
    + Modernity / -ism at the end of empire
    + Arabic renaissance
    + Arab nationalism
    + Islamic reform movement
- They form large corpora with an equal distribution along a temporal axis
    + linguistic analysis
    + historical semantics
    + data sets for social history

# 1.2 A two-fold problem

- Preservation: 
    + Active destruction of cultural artifacts: iconoclasm, neoliberalism
    + fragile materiality
- Access:
    + Absence / destruction of infrastructure / channels of knowledge transmission: lack of access to institutions, hardware, software, internet connections
    + widely-dispersed collections
    + technologies: absence of reliable OCR
    + technical skills: lack of basic scripting skills
- Consequences: focus on "high" culture and canonical texts

# 1.3 State of digitisation

1. gray online libraries / "crowd"-sourced transcriptions, e.g. [shamela.ws](http://shamela.ws/index.php/book/26523)
    + lack of metadata
    + unknown editing principles
    + unknown quality
    + cannot be reliably cited 
2. Digital imagery, e.g. [HathiTrust](http://catalog.hathitrust.org/Record/100658549)
    + lack of metadata
    + limited licences, paywalls
    + no text layer

# 2. Suggested solution: unite the two

- improve and validate the transcription with the facsimiles
- make it citable for scholars, linkable for machines
- re-purpose available tools, technologies, and material
    - preference for open and simple formats and tools
- provide the new edition with the broadest possible licence to facilitate access and re-use 


# Test case: digital *Muqtabas*

1. Basis: Generate and share a TEI edition of all 96 issues (c. 7000 pages) of Muḥammad Kurd ʿAlī's *Majallat al-Muqtabas* with a CC BY-SA 4.0 licence
2. Core feature: gradually improve the digital edition (text and mark-up)
3. Sugar on top: Static web-view (doesn't require a permanent internet connection)


# 1. Basis: Generate the TEI edition

- crawl the [digital text from *shamela.ws*](http://shamela.ws/index.php/book/26523)
- automatically transform it into [TEI XML](http://www.tei-c.org)
    + documented URI design to reference all elements
- link to digital facsimiles from the [British Library's "Endangered Archives Programme" (EAP)](http://eap.bl.uk/database/overview_item.a4d?catId=809;r=12316) and [HathiTrust](http://catalog.hathitrust.org/Record/100658549) or produce your own imagery
- host everything but images on [GitHub](https://www.github.com)
    + distributed version control
    + attribution of authorship
    + provide a [CC BY-SA 4.0 licence](http://creativecommons.org/licenses/by-sa/4.0/) for all files: edition, tools, webview

# 2. Core feature: Continuous improvement

- correct the transcription
- provide reliable bibliographic metadata based on the facsimile
- add structural mark-up
- add semantic mark-up

# 3. Sugar on top: web-view

[https://rawgit.com/tillgrallert/digital-muqtabas/master/xml/oclc_4770057679-i_60.TEIP5.xml](https://rawgit.com/tillgrallert/digital-muqtabas/master/xml/oclc_4770057679-i_60.TEIP5.xml)

- Adaptation of [TEI Boilerplate XSLT stylesheets](http://dcl.slis.indiana.edu/teibp/)
- human-readable and static web-view (either rawgit or gh-pages)
    + can be run without a continuous internet connection and with local facsimiles
- parallel display of text and facsimile
    + simple changes to display different facsimiles
- link to metadata on the article level (BibTeX)

# To do, ongoing work

- Schema design
    + mark-up of some text features has not yet been decided
- mark-up of page breaks
- Web-view needs some polishing

# Experiences

- Simple technologies and relatively little coding needed: Initial set-up took less than four weeks of after-hour labour
- Hosting with GitHub is free
- Core (but simple) features cannot be automated: page breaks must be manually tagged
- Code that can be re-purposed for---inter alia---Muḥammad Rashīd Riḍā's journal *al-Manār* 
    + [full text from shamela](http://shamela.ws/index.php/book/6947): 8605 views
    + [imagery from HathiTrust](http://catalog.hathitrust.org/Record/008882663),[imagery / PDFs from the Internet Archive](https://archive.org/details/almanaralmanar), which are linked from [*al-Maktaba al-Waqfiyya*](http://waqfeya.com/book.php?bid=7374)

# Summary

- open scholarly digital edition of *Majallat al-Muqtabas* providing
    + TEI XML files (transcription and links to facsimiles)
    + plain text files
    + BibTeX files for every article
    + customised version of TEI Boilerplate (XSLT and CSS) with stable URLs for every element
- within a framework (git and GitHub) that allows for
    + collaborative, open, version-controlled improvements of the edition
    + re-use of the text
