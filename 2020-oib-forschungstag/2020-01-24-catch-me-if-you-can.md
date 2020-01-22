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

# Introduction: project
## Problems

1. periodicals are commonly perceived as a *source* but not a *subject* in its own right
2. the history of the periodical press
    + remains largely unexplored
    + is full of untested hypotheses
    + is heavily biased by national(ist) narratives
    + focusses on a few "core" publications from Cairo and Beirut

## One of the many reasons

![Map: geographic distribution of library holdings of *al-Muqtabas*](../assets/map-oclc_4770057679-holdings-vol_1-9.png)

## Open questions: mirco level

- how were individual periodicals produced?
- who authored the vast majority of periodicals?
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

| title           | volumes | issues | articles | words   | words.per.article |
| --------        | ----:   | ----:  | ----:    | ----:   | ----:             |
| al-Ḥaqāʾiq      | 3       | 35     | 389      | 298090  | 832.66            |
| al-Ḥasnāʾ       | 1       | 12     | 201      | NA      | NA                |
| al-Manār        | 35      | 537    | 4300     | 6144593 | 1437.73           |
| al-Muqtabas     | 9       | 96     | 2964     | 1981081 | 873.34            |
| al-Ustādh       | 1       | 42     | 435      | 221447  | 582.21            |
| al-Zuhūr        | 4       | 39     | 436      | 292333  | 695.09            |
| Lughat al-ʿArab | 3       | 34     | 939      | 373832  | 485.21            |
| **total**       | 56      | 795    |          |         |                   |

## OpenArabicPE's corpus

| title           | articles.with.author.per.cent | author.count | author.birth.avg | author.death.avg |
| -------         | ----:                         | ----:        | ----:            | ----:            |
| al-Ḥaqāʾiq      | 41.90                         | 104          | 1837.53          | 1905.93          |
| al-Ḥasnāʾ       | 37.31                         | 50           | 1883.14          | 1947.17          |
| al-Manār        | 87.14                         | 356          | 1870.96          | 1913.5           |
| al-Muqtabas     | 12.72                         | 140          | 1855.94          | 1929.48          |
| al-Ustādh       | 5.52                          | 8            | NA               | NA               |
| al-Zuhūr        | 41.51                         | 112          | 1872.96          | 1939.52          |
| Lughat al-ʿArab | 16.19                         | 53           | 1875.8           | 1942.1           |
| **total**       |                               |              |                  |                  |

# First attempts to computationally map the ideosphere of the late Ottoman Arabic-speaking press



