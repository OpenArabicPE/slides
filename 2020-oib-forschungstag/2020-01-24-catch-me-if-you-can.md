---
title: "Catch me if you can!"
author: Till Grallert
date: 24 January 2020
duration: 30
tags:
- presentation
- OpenArabicPE
---

# Introduction: me
## academic profile

- academic background: social historian of the late Ottoman Eastern Mediterranean
- PhD: history of the streets as public places and public space in late Ottoman Damascus
- main areas of research:
    + social history
    + intellectual history
    + urban studies
    + periodical studies
    + gender studies
    + digital humanities
- projects:
    + genealogy food riots
    + periodical studies
    + OpenArabicPE
    + Project Jarāʾid

# Introduction: project
## Problems

1. periodicals are commonly perceived as a **source** but not a **subject** in its own right
2. the history of the periodical press
    + remains largely unexplored
    + is full of untested hypotheses
    + is heavily biased by national(ist) narratives
    + focusses on a few "core" publications from Cairo and Beirut

## One of the many reasons

![Map: geographic distribution of library holdings of *al-Muqtabas*](../assets/map-oclc_4770057679-holdings-vol_1-9.png)

## Open questions: micro level

- how were individual periodicals produced?
- who authored the vast majority of anonymous articles?
- how to conceptualise "authorship"?

## Open questions: meso level

- What are the core nodes (authors, periodicals, other works) in the ideosphere of the late Ottoman Eastern Mediterranean?

## Open question: macro level

- How do we have to revise the *nahḍa* narrative / late Ottoman intellectual history if we include the full ideosphere of the press beyond Cairo and Beirut?

# Methodology
## Methodology: computational approaches

1. Corpus building for the purpose of
2. *distant reading*
    - bibliometrics
    - social network analysis
    - stylometric authorship attribution

## OpenArabicPE's corpus

| title               | volumes | issues | articles | words   | words.per.article |
| --------            | ----:   | ----:  | ----:    | ----:   | ----:             |
| **al-Ḥaqāʾiq**      | 3       | 35     | 389      | 298090  | 832.66            |
| **al-Ḥasnāʾ**       | 1       | 12     | 201      | NA      | NA                |
| al-Manār            | 35      | 537    | 4300     | 6144593 | 1437.73           |
| **al-Muqtabas**     | 9       | 96     | 2964     | 1981081 | 873.34            |
| al-Ustādh           | 1       | 42     | 435      | 221447  | 582.21            |
| al-Zuhūr            | 4       | 39     | 436      | 292333  | 695.09            |
| **Lughat al-ʿArab** | 3       | 34     | 939      | 373832  | 485.21            |
| **total**           | 56      | 795    |          |         |                   |

## OpenArabicPE's corpus

| title               | articles.with.author.per.cent | author.count | author.birth.avg | author.death.avg |
| -------             | ----:                         | ----:        | ----:            | ----:            |
| **al-Ḥaqāʾiq**      | 41.90                         | 104          | 1837.53          | 1905.93          |
| **al-Ḥasnāʾ**       | 37.31                         | 50           | 1883.14          | 1947.17          |
| al-Manār            | 87.14                         | 356          | 1870.96          | 1913.5           |
| **al-Muqtabas**     | 12.72                         | 140          | 1855.94          | 1929.48          |
| al-Ustādh           | 5.52                          | 8            | NA               | NA               |
| al-Zuhūr            | 41.51                         | 112          | 1872.96          | 1939.52          |
| **Lughat al-ʿArab** | 16.19                         | 53           | 1875.8           | 1942.1           |
| **total**           |                               |              |                  |                  |

# First attempts to computationally map the ideosphere of the late Ottoman Arabic-speaking press
# Evaluating the corpus: network of referenced periodicals
## network of referenced periodicals: data sources
## network of referenced periodicals

![Figure: Network of periodicals mentioned *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab* and *al-Muqtabas*; weights per issue](../assets/network_oape-p3a6afa20_referenced-periodicals-per-issue_ar.png)

## network of referenced periodicals

![Figure: Core nodes in the network of periodicals mentioned *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab* and *al-Muqtabas*; weights per issue](../assets/network_oape-p3a6afa20_referenced-periodicals-per-issue-core_ar.png)

## network of referenced periodicals

1. only a small number of nodes is of relative importance
2. the inner core confirms the bias on Cairo and Beirut
3. the network is highly centralised in terms of geographic distribution
4. *al-Muqtabas* accounts for the vast majority of references
5. all periodicals are primarly self-referential
6. surprising members of the core group

## 1. only a small number of nodes is of relative importance

- common to all social networks
- centrality measured in in-degree (number of edges connecting to a node) and weight of the edges connecting nodes
- Out of a total of 465 different periodical titles, 421 or c. 90% were referred to by only a single journal. 344 periodicals are only mentioned in a single issue and 335 in a single article.
- 44 core nodes: periodicals referenced in more than one journal

## 2. the inner core confirms the bias on Cairo and Beirut

- Only 9 (2,13%) were referenced by three journals in our corpus. {==They are: *al-Manār*, *al-Muqtaṭaf*, *al-Hilāl* and *al-Ḍiyā* from Cairo, *al-Muqtabas* itself, *al-Mufīd*, *al-Waṭan* and *al-Ḥaqīqa* from Beirut and *al-Ḥuqūq* from Mt. Lebanon ==}{>>comment: this fits the standard narrative of important journals, with the exception of *al-Mufīd* <<} 
    + these would be the ones to be digitised
- The centrality of the {==three==} Cairene periodicals, *al-Manār*, *al-Muqtaṭaf*, *al-Hilāl*, which were all published by Syrian immigrants, tentatively confirms the standard narratives of the Arabic press.

## 3. the network is highly centralised in terms of geographic distribution

- The 44 core nodes were published in only a handful of locations: Beirut (9), Cairo (7), Baghdad, Damascus, Paris (3), Alexandria,  London, Mt. Lebanon, Saida and Zahle (1).

## 4. *al-Muqtabas* accounts for the vast majority of references

- by some orders of magnitude and
- even after we weight the number of references by the number of issues
- should we deduct that *al-Muqtabas* was more outward-looking and more involved in larger discourses of the day?

## 5. all periodicals are primarly self-referential

## 6. surprising members of the core group

1. *al-Jinān* and *al-Ḍiyāʾ* were not longer published
2. Foreign titles:  *Le Temps*, *Revue des Revues* and *Revue du Monde Musulman* from Paris and *The Times* from London

# Bibliometrics: the network of authors
## network of authors: data sources
