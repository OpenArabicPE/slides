---
title: "IDH conference: OpenArabicPE normalize_whitespace"
author: Till Grallert
date: 2020-04-26
ORCID: orcid.org/0000-0002-5739-8094
---

# to do

the core network could be plotted with a larger font for the nodes

# ideosphere

- I use ideosphere as a spatial metaphor to refer to the realm of human ideas in its entirety, only some of which becomes manifest and thus traceable in concrete intellectual production. As such it is different from Roland Barthes’ ideosphere and Arjun Appadurai’s ideosphere, which are both concerned with questions of ideology.

# network of referenced periodicals
## 1. only a small number of nodes is of relative importance

- common to all social networks
    + nodes cluster into communities with
    + core nodes for each cluster and
    + nodes connecting communities (in-betweenness centrality)
- centrality measured in in-degree (number of edges connecting to a node) and weight of the edges connecting nodes
- Out of a total of 465 different periodical titles, 421 or c. 90% were referred to by only a single journal. 344 periodicals are only mentioned in a single issue and 335 in a single article.
- 44 core nodes: periodicals referenced in more than one journal

## 2. *al-Muqtabas* accounts for the vast majority of references

- by some orders of magnitude and
- even after we weight the number of references by the number of issues
- should we deduct that *al-Muqtabas* was more outward-looking and more involved in larger discourses of the day?

## 3. all periodicals are primarly self-referential

# network of referenced periodicals: the core
## 1. the inner core confirms the bias on Cairo and Beirut

- Only 9 (2,13%) were referenced by three journals in our corpus. They are: *al-Manār*, *al-Muqtaṭaf*, *al-Hilāl* and *al-Ḍiyā* from Cairo, *al-Muqtabas* itself, *al-Mufīd*, *al-Waṭan* and *al-Ḥaqīqa* from Beirut and *al-Ḥuqūq* from Mt. Lebanon
    + comment: this fits the standard narrative of important journals, with the exception of *al-Mufīd*
    + these would be the ones to be digitised
- The centrality of the three Cairene periodicals, *al-Manār*, *al-Muqtaṭaf*, *al-Hilāl*, which were all published by Syrian immigrants, tentatively confirms the standard narratives of the Arabic press.

## 2. the network is highly centralised in terms of geographic distribution

- The 44 core nodes were published in only a handful of locations: Beirut (9), Cairo (7), Baghdad, Damascus, Paris (3), Alexandria,  London, Mt. Lebanon, Saida and Zahle (1).

## 3. surprising members of the core group

1. *al-Jinān* and *al-Ḍiyāʾ* were not longer published
2. Foreign titles:  *Le Temps*, *Revue des Revues* and *Revue du Monde Musulman* from Paris and *The Times* from London

# Bibliometrics: the network of authors
## 1. only a small number of nodes is of relative importance

- 14 of 319
- one author published in all journals

Maʿrūf al-Ruṣāfī was a famous poet from Baghdad who mostly authored *qaṣāʾid* on current political affairs. He moved to Istanbul after the Young Turk Revolution, where he worked as an Arabic teacher at the Royal College and at the newspaper *Sabīl al-Rashad*. He was elected MP for al-Muthanna (Iraq) in 1912 and 1914. After WWI he became a member of the Arab Scientific Academy, established by Muḥammad Kurd ʿAlī in Damascus.[^45] al-Ruṣāfī's close ties to *al-Muqtabas* and Kurd ʿAlī are further evident in the announcement in 1910 for the publication of a first collection of his poems, in which *al-Muqtabas* claimed that he was known among some people as "the poet of *al-Muqtabas*" and---wrongly---that "more than three quarters [of the *qaṣāʾid* therein] had been published in this journal".[^46] The publication of al-Ruṣāfī's *qaṣīda*s in so many different periodicals---in addition to the journals in our corpus, I came across his *qaṣīda*s in many other journals and newspapers---raises an important question regarding the production of newspapers: did he send his *qaṣīda*s to the editors of sometimes far away periodicals {==just like that==}{>>better wording<<}? Was he invited to contribute? Did editors take his texts from other sources?

## 2. limited overlap between journals from the same city
## 3. nodes are connected by various other social networks (education, imperial service, family relations etc.)

# network of authors: the core
## 1. Iraqis, poets, not covered by scholarly literature

- 14 of 319
- Only 8 can be found in international authority files
- 11 identifiable authors
    + 6 Iraqis: Maʿrūf al-Ruṣāfī, Kāẓim al-Dujaylī, Ibrahīm Ḥilmī al-ʿAmr, Anastās Mārī al-Karmalī (often writing under the pen name Sātisnā), the two al-Shabībī brothers, Muḥammad Riḍā and Muḥammad Bāqir;
    + 3 Egyptians: Muṣṭafā Ṣādiq al-Rāfiʿī, Aḥmad Muḥarram and Walī al-Dīn Yakan;
    + only 2 Syrians ʿĪsā Iskandar al-Maʿlūf and Muḥammad Rāghib Ṭabbākh
    + only 2 Christians
        * challenges the dominant *nahḍa* narrative
    + only one (al-Maʿlūf) mentioned in standard account of Arabic press
    + 7 poets
    + 7 journalists (editors, owners of periodicals)

# stylometry: computational authorship attribution
## computational authorship attribution: stylometry

- this has not yet been applied to Arabic
- method: **compare** stylistic features to gain a numerical measure of difference
    + distance measure is sensitive to composition of corpus
- stylistic features: most frequent words (MFWs)
    + have been shown to be extremely effective for authorship attribution
- chunking/sampling impacts results
    + features: run multiple iterations and have them vote
    + texts: minimum length of 4000-5000 words

## stylometry: 5000 words

- it works! correctly identified signal of
    + authorship
    + editorship
    + translation
- additional (sub)-signal: genre
- Contradicts the hypothesis insofar as there is at least one additional author beyond Muḥammad Kurd ʿAlī for articles in *al-Muqtabas*

## stylometry: how to deal with the minimal length requirement?

- compare anonymous sections and articles of >= 5000 words with articles of known authors
- result: the lower half of the plot cannot be considered authors of the anonymous articles.
