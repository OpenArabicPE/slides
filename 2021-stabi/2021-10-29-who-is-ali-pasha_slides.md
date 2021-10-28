---
title: "Who is *ʿAlī Pasha*?"
subtitle: "Modelling personal names from the late Ottoman Eastern Mediterranean (c.1850--1920)"
author: Till Grallert
date: 2021-10-25 
ORCID: orcid.org/0000-0002-5739-8094
bibliography: /BachUni/research-projects/OpenArabicPE/assets/bibliography/openarabicpe.csl.json
---

## Who is *ʿAlī Pasha*? <br /> Modelling personal names from the late Ottoman Eastern Mediterranean (c.1850--1920)

Till Grallert,  @[tillgrallert](https://twitter.com/tillgrallert)

Workshop "`<Author><Title><Place>`", Berlin, 27--29 October 2021

Slides: [https://OpenArabicPE.github.io/slides/2021-stabi/](https://OpenArabicPE.github.io/slides/2018-turkologentag/index.html)


<!-- ## Background
### Building infrastructures we need without the help we can't get

:::{.c_width-50}

[Project Jarāʾid](https://projectjaraid.github.io/): crowd-sourced union list of all Arabic periodicals before 1930 (with Adam Mestyan)

![Number of Arabic periodical titles until 1930, showing known holdings and (partial) digitised collections](../assets/maps/map-jaraid_sf_mena_en-status_scatterpie.png){#fig:jaraid-holdings}

:::
:::{.c_width-50}

[Open Arabic Periodical Editions](https://openarabicpe.github.io): a framework for bootstrapped digital scholarly editions of Arabic periodicals

![[Webview of *al-Muqtabas* 6(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png){#fig:webview-muqtabas}

::: -->

# Background: <br/>Building infrastructures we need without the help we can't get

## [Project Jarāʾid](https://projectjaraid.github.io/) (2012--) <br/>Closing the knowledge `<gap/>`

:::{.c_width-50}

- Collaboration with Adam Mestyan (Duke)
- Crowd-sourced union list of all Arabic periodicals before 1930
    + website and open data sets ([TEI XML](https://tei-c.org/))
    + authority files for c.2700 persons, 220 places, 180 libraries etc.

:::
:::{.c_width-50}

![Global distribution of new Arabic periodical titles](../assets/maps/map-periodicals_World_1855-1929_temp-dist-status-y_5.gif){#fig:map-jaraid}

:::

## Open Arabic Periodical Editions ([OpenArabicPE](https://openarabicpe.github.io), 2015--) <br/>Closing the infrastructural `<gap/>`

Digital editions based on shadow libraries and digital facsimiles (TEI XML), authority files (TEI XML), Bibliographic metadata (TEI, MODS, RDF, Zotero)


:::{.c_width-60}

| title                                                                         | DOI                                                              | vol.s | issues | articles | words  |
| :--------                                                                     | :--                                                              | ----: | ----:    | ----:   | ----:   |
| [al-Ḥaqāʾiq](https://www.github.com/openarabicpe/digital-haqaiq)              | [10.5281/zenodo.1232016](https://doi.org/10.5281/zenodo.1232016) | 3     | 35       | 389     | 298090  |
| [al-Ḥasnāʾ](https://www.github.com/openarabicpe/journal_al-hasna)             | [10.5281/zenodo.3556246](https://doi.org/10.5281/zenodo.3556246) | 1     | 12       | 201     | NA      |
| [al-Manār](https://www.github.com/openarabicpe/journal_al-manar)              |                                                                  | 35    | 537      | 4300    | 6144593 |
| [al-Muqtabas](https://www.github.com/tillgrallert/digital-muqtabas)           | [10.5281/zenodo.597319](https://doi.org/10.5281/zenodo.597319)   | 9     | 96       | 2964    | 1981081 |
| [al-Ustādh](https://www.github.com/openarabicpe/journal_al-ustadh)            | [10.5281/zenodo.3581028](https://doi.org/10.5281/zenodo.3581028) | 1     | 42       | 435     | 221447  |
| [al-Zuhūr](https://www.github.com/openarabicpe/journal_al-zuhur)              | [10.5281/zenodo.3580606](https://doi.org/10.5281/zenodo.3580606) | 4     | 39       | 436     | 292333  |
| [Lughat al-ʿArab](https://www.github.com/openarabicpe/journal_lughat-al-arab) | [10.5281/zenodo.3514384](https://doi.org/10.5281/zenodo.3514384) | 3     | 34       | 939     | 373832  |
| **total**                                                                     |                                                                  | 56    | 795      | 9664    | 9311376 |

Table: Übersicht über das Periodikakorpus {#tbl:openarabicpe-corpus}

:::
:::{.c_width-30}

![[Webview of *al-Muqtabas* 6(2)](https://openarabicpe.github.io/journal_al-muqtabas/tei/oclc_4770057679-i_61.TEIP5.xml)](../assets/boilerplate_muqtabas.png){#fig:webview-muqtabas}

:::

## Background
### Computational periodical studies

:::{.c_width-50}

![Directed network of periodicals referenced  in *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab*, and *al-Muqtabas*, weighted by number of issues. Size and colour of nodes: in-degree.](../assets/networks/network_oape-p3a6afa20_referenced-periodicals-per-issue_circular-n-size_in-degree.png){#fig:network-periodicals}

:::
:::{.c_width-50}

![Undirected network of authors in *al-Ḥaqāʾiq*, *al-Ḥasnāʾ*, *Lughat al-ʿArab*, and *al-Muqtabas*. Colour of nodes: betweenness centrality; size of nodes: number of periodicals; width of edges: number of articles.](../../assets/OpenArabicPE/networks/network_oape-p3a6afa20_authors_unimodal-n-size_out-degree-n-colour_betweenness-e-colour_grey.png){#fig:network-authors}

:::

## Aim: identification and disambiguation of named entities

:::{.c_width-50}

- problem 1: historical diversity
	+ multilingual and multiscriptoral societies
	+ multiple cultural practices
	+ use of a name is context dependent
	+ change over a person's life time

:::
:::{.c_width-50}

- problem 2: Western conceptual hegemony over the tool chain
	+ limited support for Arabic script
	+ various Latinizations
	+ hegemonial concepts of "entity names"

:::

## Example: *Nāṣīf Mishāqa*

American consular agent and chancellor-cum-dragoman of the British consulate in Damascus. Eldest son of the famous Mikhāʾīl Mishāqa.

<!-- - حضرة صاحب الدولة المشير عبد الله باشا
- جناب رفعتلو فريد افندي كركبي
- حضرة سعادتلو احمد برهان الدين بك افندي
- جناب عزتلو صبحي بك ابو النصر
- جزائري زاده الامير علي باشا ابن عبد القادر افندي الحسني -->

:::{.c_width-50}

### Periodicals

+ ناصيف افندي مشاقة
+ حضرج المفاضل ناصيف بك مشاقة

:::
:::{.c_width-50}

### Consular archives

<!-- - TNA (UK):  -->
+ Nassif Effendi Meshaka
+ M. Nasif Bey Mishaka
+ Michaka
<!-- - NACP (US) -->
+ Nasif Meshaka (his own signature)

:::

## Example: *Anastās Mārī al-Karmilī*

Famous Iraqi priest and philologist of Lebanese descent. Prolific user of pen names and pseudonyms. Disambiguation is solely provided by Arabic bibliobiographic dictionaries (Ziriklī etc.).

:::{.c_width-30}
### Periodicals

- <persName xml:lang="ar"><roleName type="pseudonym">ساتسنا</roleName></persName>
- <persName xml:lang="ar"><roleName type="pseudonym">صاحب مجلة لغة العرب</roleName></persName>

:::
:::{.c_width-30}
### Authority files


- <persName xml:lang="ar"><roleName type="rank">الأب</roleName> <forename>أنستاس</forename> <forename>ماري</forename> <surname><addName type="nisbah">الكرملي</addName></surname></persName>
- <persName xml:lang="ar"><forename>بطرس</forename> <addName type="nasab">بن <forename>جبرائيل</forename></addName> <forename>يوسف</forename> <surname>عواد</surname></persName>
- <persName xml:lang="fr">Père Anastase-Marie de Saint-Elie</persName>

:::
:::{.c_width-30}
### Scholarly literature

-  (Father) Anastās al-Karmalī
-  Anastase-Marie de Saint-Elie

:::


# Modelling Names in TEI
## Why TEI

- limited/no institutional support
- no database
- well-established standard with mature tools

## What is the TEI

- a community of practice around a shared goal: interchangable formats, tools etc. for digital editing
- a hermeneutic tool and data model: based in the Western tradition
- a technical implementation and serialisation in a specific data format: currently XML with the much hated pointy brackets.

## Soualah and Hassoun's proposal for classical Arabic names

[@Soualah+2012] propose to use available elements `<surname>`, `<forename>`, and `<addName>` with a controlled vocabulary of `@type` and `@subtype` attributes.

- `<surname>`: to encode the *laqab* evoking a real or assigned quality
- `<forename>`: for the *ism*
- `<addName>` with `@type`
    + "nasab": patronym introduced by "ibn" or "ibnat"
    + "kunyah": teknonym or a mark of distinction applied to prominent figures to honor them. For example, "Abū Yūsuf" is often used for someone called Yaʿqūb
    + "khitab": an honorific name, which is usually ended by the suffix al-Dīn
    + "nisbah": an adjective formed by using the suffix ī in order to indicate the person origin, his birth place, or his residence. It represents the relationship name, which can be a genealogical, political or ideological affiliation of a person.

## My extended proposal for late Ottoman contexts

I suggest to add the following mark-up for late-Ottoman names

- `<roleName type="title">`: covering the wide range of Ottoman titles, e.g. Pasha, Bey, Efendi that do not necessarily denote a post in an administrative hierarchy
- `<roleName type="rank">`: denoting ranks with a formal, administrative hierarchy
- `<addName type="honorific">`: for the highly regularised honorific addresses and salutations, e.g. *rif'etli*, *saadetli*, *utufetli*, *lizetli*, *devletli*

## Example: ʿAlī Pasha

```xml
<persName xml:lang="ar">دولتلو جزائري زاده الامير علي باشا ابن عبد القادر افندي الحسني</persName>
```

Could be marked up as:

```xml
<persName xml:lang="ar">
	<addName type="honorific">دولتلو</addName>
    <addName type="nisbah">جزائري</addName>
    <addName type="honorific" xml:lang="ota">زاده</addName>
    <roleName type="title">الامير</roleName>
    <forename>علي</forename>
    <roleName type="title" xml:lang="ota">باشا</roleName>
    <addName type="nasab">ابن
        <forename><addName type="theophoric">عبد القادر</addName></forename>
        <roleName type="title" xml:lang="ota">افندي</addName>
    </addName>
    <surname type="laqab">الحسني</surname>
</persName>
```

# Automating the mark-up
## 1. check against authority list of Ottoman components

Allows to identify all titles, ranks, honorific addresses

:::{.c_width-50}
input:

```xml
<persName xml:lang="ar">دولتلو جزائري زاده الامير علي باشا ابن عبد القادر افندي الحسني</persName>
```

:::
:::{.c_width-50}
output:

```xml
<persName xml:lang="ar">
	<addName type="honorific" xml:lang="ota">دولتلو</addName>
	جزائري 
    <addName type="honorific" xml:lang="ota">زاده</addName>
    <roleName type="title">الامير</roleName>
    علي 
    <roleName type="title" xml:lang="ota">باشا</roleName>
    ابن عبد القادر
    <roleName type="title" xml:lang="ota">افندي</addName>
    الحسني
</persName>
```

:::

## 2. rule-based mark-up of Arabic components

1. *laqab* / surname: final **word** beginning with ال but not ending in ي
2. *nisba*: final **word** beginning with ال and ending in ي
3. *nasab*: **sequence** of words beginning with ابن, بن, بنت etc.
4. *kunya*:  **sequence** of words beginning with `اب(و|ي|ا)` etc.
5. *khiṭāb*: **sequence** of **two** words ending with الدين
6. theophoric: can be *ism* or *laqab*
	- **sequence** of **two** words beginning with عبد
	- **sequence** of **two** words ending with الله

## 2. rule-based mark-up of Arabic components

:::{.c_width-50}
input:

```xml
جزائري
علي
ابن عبد القادر
الحسني
```

:::
:::{.c_width-50}
output:

```xml
جزائري
علي
<addName type="nasab"><nameLink>ابن</nameLink> <addName type="theophoric">عبد القادر</addName>
<addName type="nisbah">الحسني</addName>
```

:::

## 3. combined results

:::{.c_width-50}
automated mark-up:

```xml
<persName xml:lang="ar">
	<addName type="honorific" cert="high" xml:lang="ota">دولتلو</addName>
	جزائري 
	<addName type="honorific" cert="high" xml:lang="ota">زاده</addName> 
	<roleName type="honorific" cert="high">الامير</roleName>  
	علي 
	<roleName type="title" cert="high">باشا</roleName>
	<addName type="nasab" cert="medium">
		<nameLink cert="high">ابن</nameLink> 
		<addName type="theophoric" cert="high">عبد القادر</addName> 
		<roleName type="title" cert="high">افندي</roleName> </addName> 
	<addName type="nisbah" cert="high">الحسني</addName>
</persName>
```

:::
:::{.c_width-50}
aim: 

```xml
<persName xml:lang="ar">
	<addName type="honorific">دولتلو</addName>
    <addName type="nisbah">جزائري</addName>
    <addName type="honorific" xml:lang="ota">زاده</addName>
    <roleName type="title">الامير</roleName>
    <forename>علي</forename>
    <roleName type="title" xml:lang="ota">باشا</roleName>
    <addName type="nasab">ابن
        <forename><addName type="theophoric">عبد القادر</addName></forename>
        <roleName type="title" xml:lang="ota">افندي</addName>
    </addName>
    <surname type="laqab">الحسني</surname>
</persName>
```

:::

# Latinization
## approaches

1. rule-based
2. look up: precomputed authority file

## TEI `<listNym>` for multiple word forms

The TEI provides `<nym>` for enconding multiple forms of a string.

:::{.c_width-50}

```xml
<nym xml:id="nym-T-4">
   <form xml:lang="ar">باشا</form>
   <form xml:lang="ar-Latn-x-ijmes">Bāshā</form>
   <form xml:lang="ar-Latn-x-dmg">Bāšā</form>
   <form xml:lang="de">Pascha</form>
   <form xml:lang="en">Pasha</form>
   <form xml:lang="fr">Pacha</form>
   <form xml:lang="tr">Paşa</form>
</nym>
```

<!-- <nym xml:id="nym-T-1">
	<form xml:lang="ota">بك</form>
	<form xml:lang="ar-Latn-x-ijmes">Bik</form>
	<form xml:lang="en">Bek</form>
	<form xml:lang="ota-Latn-DE">Beg</form>
	<form xml:lang="tr">Bey</form>
</nym> -->

:::
:::{.c_width-50}

```xml
<nym xml:id="nym-F-23">
   <form xml:lang="ar">علي</form>
   <form xml:lang="ar-Latn-x-ijmes">ʿAlī</form>
   <form xml:lang="ar-Latn-x-dmg">ʿAlī</form>
   <form xml:lang="und-Latn">Ali</form>
   <form xml:lang="und_Latn">Aly</form>
</nym>
```

## link name components to nyms

Linking name components allows for script-agnostic identification

:::{.c_width-50}
input: 

```xml
<persName xml:lang="ar">
	<addName type="honorific">دولتلو</addName>
    <addName type="nisbah">جزائري</addName>
    <addName type="honorific" xml:lang="ota">زاده</addName>
    <roleName nymRef="#nym-H-1" type="title">الامير</roleName>
    <forename nymRef="#nym-F-23">علي</forename>
    <roleName nymRef="#nym-T-4" type="title" xml:lang="ota">باشا</roleName>
    <addName type="nasab">
    	<nameLink nymRef="#nym-P-2">ابن</nameLink> 
        <forename><addName type="theophoric">عبد القادر</addName></forename>
        <roleName nymRef="#nym-T-2" type="title" xml:lang="ota">افندي</addName>
    </addName>
    <surname type="laqab">الحسني</surname>
</persName>
```

:::
:::{.c_width-50}
outputs:

- Arabic: دولتلو جزائري زاده الامير علي باشا ابن عبد القادر افندي الحسني
- IJMES: develtli Jazāʾirī zāde al-Amīr ʿAlī Pasha Ibn ʿAbd al-Qādir Efendi al-Ḥusnī

:::

# Link to authority files
## normalize the name

:::{.c_width-50}
resort name components to generate a stable sequence of `@nymRef` codes

<!-- - حافظ أفندي إبراهيم
- حافظ بك إبراهيم  -->

- `addName[@type = 'honorific']`
- `forename`
- `roleName[@type = 'title']`
- `roleName[@type = 'rank']`
- `addName[@type = 'khitab']`
- `addName[@type = 'kunyah']`
- `addName[@type = 'nasab']`
- `surname`
- `addName[@type = 'nisbah']`

:::
:::{.c_width-50}
compute minimal versions likely to be found in authority files

- `forename`
- `surname` or `addName[@type = 'nisbah']`
- e.g. 
	+ علي الحسني
	+ علي الجزائري
	+ ʿAlī al-Ḥusnī
	+ ʿAlī al-Jazāʾirī

:::

## Thank you!

- Contributors to Project Jarāʾid: Hala Auji, Philippe Chevrant, Marina Demetriadou, Lamia Eid, Stacy Fahrenthold, Ulrike Freitag, <!-- Till Grallert,  -->Rana Issa, Nicole Khayat, Peter Magierski, Leyla von Mende, Adam Mestyan, Christian Meier, Daniel Newman, Geoffrey Roper, Sinai Rusinek, Philip Sadgrove, Ola Seif, and Rogier Visser
- Contributors to OpenArabicPE: Jasper Bernhofer, Dimitar Dragnev, Patrick Funk, Talha Güzel, Hans Magne Jaatun, Xaver Kretzschmar, Daniel Lloyd, Klara Mayer, Tobias Sick, Manzi Tanna-Händel, and Layla Youssef


