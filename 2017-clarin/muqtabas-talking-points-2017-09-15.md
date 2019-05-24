---
title: "OpenArabicPE: Muqtabas at Clarin-D"
author: Till Grallert
date: 2017-04-24 15:24:23 +0200
bibliography: openarabicpe-clarin.bib
links-as-notes: true
---

# Description of the data

## What is Muqtabas

Digital Muqtabas comprises the TEI edition of all 96 issues of Muhammad Kurd Ali's monthly journal *al-Muqtabas* (The Digest / Acquired Learning) between 1906 and 1917/18 totalling some 3,8 million words. Muhammad Kurd Ali (1876–1953) was the best known and, after the Young Turk Revolution of 1908, the most influential journalist and intellectual in Damascus. Before establishing his own journal *al-Muqtabas* in Cairo in 1906 and the first daily newspaper to be published in Damascus in 1908 (also confusingly called *al-Muqtabas*), he had held minor government offices and worked at various public and private presses and periodicals in Damascus and Cairo. He was well-acquainted with leading figures of the Islamic reform movement in Egypt and Greater Syria, like Tahir al-Jaza'iri, Rashid Rida and Muhammad Abduh "senior circle" in the early 1890s in Damascus and later moved and worked in Rashīd Riḍā's and Muhammad ʿAbduh's circles in Cairo. After the Young Turk Revolution, Kurd Ali returned to his hometown and publication of *al-Muqtabas* moved from Cairo to Damascus in the journal's third year. In Damascus, *al-Muqtabas* soon became "the boldest, most coherent, consistent and committed proponent of reform and modernity [...] prior to World War I".[^6] Due to conflicts with the authorities over the reprint of a poem, Kurd Ali again fled Damascus for Cairo and Europe in 1912. Consequently, *al-Muqtabas* was published from Cairo for a couple of months before Kurd Ali was allowed to return once again. During World War I and Cemal Pasha's infamous term as commander-in-chief of the 4th Army and governor general of Syria, Kurd Ali was able to win his support. He thus escaped the fate of Shukri al-Asali, Abd al-Ghani al-Uraysi and other journalists from Beirut and Damascus, who were publicly executed on charges of treason. Similarly to their editor, the journal and the newspaper *al-Muqtabas* survived and continued publication until the final days of the war---albeit in shorter and less frequent editions due to material shortages. After the end of the war and the disintegration of the Ottoman Empire, Kurd Ali abandoned the monthly and left the editorship of the revived daily newspaper *al-Muqtabas* to his brother Ahmad.[^7] He founded the Arab Scientific Academy whose president he became in 1919 and served twice as Minister of Education (1920–22, 1928–32) during the French Mandate over Syria.

## general state of affairs

Early Arabic periodicals from the late nineteenth and early twentieth centuries, among them *al-Muqtabas* , such as {--Butrus al-Bustānī's--} *al-Jinān* (Beirut, 1876–86), {--Yaʿqūb Ṣarrūf, Fāris Nimr, and Shāhīn Makāriyūs'--} *al-Muqtaṭaf* (Beirut and Cairo, 1876–1952), {--Muhammad Kurd Ali's--} *al-Muqtabas* (Cairo and Damascus, 1906–18/19) or {--Rashīd Riḍā's--} *al-Manār* (Cairo, 1898–1941) are at the core of formative discourses that still reverberate through the Arabic-speaking Middle East: the Arabic renaissance (*al-nahda*), Arab nationalism, and the Islamic reform movement. The better known and---at the time---widely popular journals do not face the ultimate danger of their last copy being destroyed in the current onslaught from iconoclasts, institutional neglect, and wars raging through Syria, Libya, Yemen, and Iraq. Yet, copies are distributed throughout libraries and institutions worldwide. This makes it almost impossible to trace discourses across journals and with the demolition and closure of libraries in the Middle East, they are increasingly accessible to the affluent Western researcher only.

*al-Muqtabas* is one of the more readily available early Arabic periodicals and its importance to regional audiences as well as the scholarly community is underlined by a 1992 facsimile reprint from Dar Sadir in Beirut. But despite this reprint and an original print run of c. 1000 copies per issue[^8], we were able to trace only about 40 copies globally through library catalogues and inquiries---and most of these are either incomplete collections or microfiche copies from one of two master fiches (produced in Chicago and Zurich). Consequently, systematic analysis of *al-Muqtabas* is all but absent from scholarly literature.

Digitisation promises an "easy" solution to the problems of preservation and access. Large-scale scanning efforts such as [Hathitrust][hathitrust], the [British Library's "Endangered Archives Programme" (EAP)][bl], [MenaDoc][menadoc] or [Institut du Monde Arabe][bibalex] produced digital facsimiles of numerous Arabic periodicals. But they come with their own problems. Some, such as HathiTrust, restrict access even to material in the public domain due to fears of being sued in court. Interfaces are commonly not available in Arabic and some display Arabic material in the wrong sequence of pages. While this severely restricts accessibility for the communities these cultural artifacts arguably belong to, scholarly use is hampered by the absence of reliable bibliographic metadata, particularly on the issue level, stable URLs and a searchable text layer.

Due to the state of Arabic OCR and the particular difficulties of low-quality fonts, inks, and paper employed at the turn of the twentieth century, these texts can currently only be reliably digitised by human transcription.[^3] Funds for transcribing the tens to hundreds of thousands of pages of an average mundane periodical are simply not available, despite of their cultural significance and unlike for valuable manuscripts and high-brow literature. Consequently, we still have not a single digital scholarly edition of any of these journals. On the other hand, gray online-libraries of Arabic literature, namely [*al-Maktaba al-Shamila* (*shamela.ws*)][shamela], [*Mishkat*][almeshkat], [*Saydal-Fawa'id*][saaid] or [*al-Waraq*][alwaraq], provide access to a vast body of (mostly classical) Arabic texts including transcriptions of unknown provenance, editorial principals, and quality for some of the mentioned periodicals. These gray "editions" lack information linking the digital representation to material originals, namely bibliographic metadata and page breaks, which makes them almost impossible to employ for scholarly research.

## the digital edition

Within the framework of OpenArabicPE we propose to unite transcriptions from gray online libraries with the digital facsimiles as a means to verify the quality of the digital text. We then semi-automatically transform the text to XML following a custom [TEI schema][openarabicpe_schema] to model Arabic periodicals. At the bare minimum, we provide structural mark-up of sections and items (articles) with headings and bylines were applicable. Detailed bibliographic metadata on the issue level is provided in the TEI header. It contains all the information available on the journal's title pages and mastheads as well as information on publication dates from other sources (such as announcements in dated contemporaneous newspapers).

The text of our digital edition of *al-Muqtabas* was transcribed from either digital facsimiles or original copies by anonymous transcribers following undocumented editing principles and uploaded to [*shamela.ws*][shamela 2].[^1] Comparison with the original print edition allows us to discern common transcription errors, such as missing lines, which indicate that *shamela.ws*'s text was indeed transcribed by humans without quality control through double-keying usually required for scholarly transcriptions.[^5] The comparison also reveals that *shamela.ws* principally omitted mastheads, all words in Latin script (mainly technical terms and proper nouns) and all footnotes. The transcription has a number of substantial and unmarked gaps, ranging from a single paragraph to multiple pages.[^4] Some of these could be due to pages missing from the original from which the transcribers worked or page-turning errors. Others remain enigmatic and might have been driven by editorial choices.[^2] In terms of structural mark-up, *shamela.ws* did not provide but an eclectic selection of top-level headers. Bibliographic metadata is all but non-existing, since *shamela.ws* supplied faulty Gregorian publication dates and its own consecutive issue count that ignores the original collation into volumes.

## some statistics

The TEI edition comprises all 96 issues of *al-Muqtabas* with a total of some 7.000 pages and more than 3,8 million words. Issues comprise a collection of longer independent articles and sections with shorter articles such as brief reports on new discoveries and book announcements. In total *al-Muqtabas* printed slightly more than 5.000 articles, 3.400 of which were shorter articles in sections. Of the 1.633 independent articles, only one third explictly mentioned an author---including such bylines as "a reader from Baghdad". In total we can currently identify only 136 different named authors. All of them were men and only 52 published more than one article. Two of the three most prolific among them, Ma'ruf al-Rusafi (24 articles) and Satsuna (13), wrote from Baghdad<!-- , and the third, 'Isa Iskandar al-Ma'aluf, from Zahle (Lebanon) -->. The majority of the remaining authors contributed from the cities of Greater Syria and Egypt, but some wrote from cities in France and the US.


# Notes

[^1]: This text was then shared on [WikiSource][wikisource]. It was also used by [*arshif al-majallat al-adabiyya wa-l-thaqafiyya al-arabiyya* (archive.sakhrit.co)](archive.sakhrit.co) to produce a number of fake facsimiles by rendering the text as images adopting common layout principles for early Arabic periodicals.
[^2]: *shamela.ws*'s edition of *al-Manar* omitted Rashid Rida's *Tafsir* that accounted for one fifth of the journal's content; see [@Zemmin_2016, 232].
[^3]: c.f. [@Margner_2012]. For recent promising approaches using machine-learning and neural networks see [@Romanov_2016].
[^4]: See [no. 5(7), pp. 463--466][rawgit] and [no. 5(12), pp. 761--765][rawgit 2] for examples.
[^5]: See [no. 4(2), p.82][rawgit 3], [no. 4(3), p.158][rawgit 4], and [no. 6(12), pp.799--800][rawgit 5] for examples.
[^6]: [@Seikaly_1981, 128]
[^7]: [@Ayalon_1995, 84]
[^8]: [@Ayalon_1995, 148] with reference to [@Ilyas_1982, 180--181].

[almeshkat]: http://almeshkat.net/
[alwaraq]: http://www.alwaraq.net/
[bibalex]: http://ima.bibalex.org/IMA/presentation/home/list.jsf
[menadoc]: http://menadoc.bibliothek.uni-halle.de/
[bl]: http://eap.bl.uk/
[hathitrust]: http://catalog.hathitrust.org/
[openarabicpe_schema]: https://github.com/OpenArabicPE/OpenArabicPE_ODD
[rawgit]: https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_54.TEIP5.xml#pb_61.d1e2036
[rawgit 2]: https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_59.TEIP5.xml#pb_51.d1e2281
[rawgit 3]: https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_38.TEIP5.xml#p_60.d1e2238
[rawgit 4]: https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_39.TEIP5.xml#gap_1.d1e3111
[rawgit 5]: https://tillgrallert.github.io/digital-muqtabas/xml/oclc_4770057679-i_71.TEIP5.xml#pb_126.d1e4373
[saaid]: http://saaid.net/
[shamela]: http://www.shamela.ws/
[shamela 2]: http://shamela.ws/index.php/book/26523
[wikisource]: https://ar.wikisource.org/wiki/%D9%85%D8%AC%D9%84%D8%A9_%D8%A7%D9%84%D9%85%D9%82%D8%AA%D8%A8%D8%B3/%D8%A7%D9%84%D8%B9%D8%AF%D8%AF_1