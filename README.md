# Flanders: law history in git

The law of the Flemish Region and Community (Vlaanderen, Belgium) as a git history: one file per article, one commit per amending act on the day it took effect, and the amending act as the commit's author. `git blame` names the act behind every paragraph; `git log` lists every change to an article; checking out a date gives the text in force that day.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `be-vlg/`. The federal law is in [lexifina/belgium-law](https://github.com/lexifina/belgium-law).

The text is in Dutch, the official language of the Flemish institutions, exactly as the Vlaamse Codex publishes it.

## What this repository holds

45 acts with 161 versions so far: the special decree of 7 July 2006 on the Flemish institutions first, then the other special decrees and the decrees (codified decrees first), added in parts of about 25. Orders of the Flemish Government (besluiten), ministerial orders and federal texts the Codex also holds are not included yet.

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `decr-1992-12-18-1001310/` | Decreet van 18 december 1992 houdende bepalingen tot begeleiding van de begroting 1993 | 7 | oldest version available, then each consolidated version: 30 November 2006 to 23 July 2026 |
| `decr-1994-12-21-1001602/` | Decreet van 21 december 1994 houdende bekrachtiging van het besluit van de Vlaamse regering van 16 november 1994 betreffende de definitieve aanwijzing van de be | 1 | oldest version available, 1 August 2007 |
| `decr-1991-04-29-1001605/` | Decreet van 29 april 1991 tot vaststelling van de algemene regelen inzake de erkenning en subsidiëring van [de milieu-, natuur-, en ruimteverenigingen] | 4 | oldest version available, then each consolidated version: 1 June 2009 to 1 July 2024 |
| `decr-1991-04-29-1001607/` | Decreet van 29 april 1991 betreffende het Vlaams Provinciefonds | 7 | oldest version available, then each consolidated version: 1 January 2007 to 1 January 2016 |
| `decr-1984-03-20-1001609/` | Decreet van 20 maart 1984 houdende het statuut van de logiesverstrekkende bedrijven | 2 | oldest version available, then each consolidated version: 31 January 2008 to 1 January 2010 |
| `decr-1990-12-21-1001610/` | Decreet van 21 december 1990 houdende begrotingstechnische bepalingen alsmede de bepalingen tot begeleiding van de begroting 1991 | 18 | oldest version available, then each consolidated version: 1 June 2006 to 1 January 2028 |
| `decr-1994-12-21-1001611/` | Decreet van 21 december 1994 houdende bepalingen tot begeleiding van de begroting 1995 | 5 | oldest version available, then each consolidated version: 1 January 2012 to 1 January 2022 |
| `decr-1990-07-31-1001627/` | Decreet van 31 juli 1990 [betreffende het publiekrechtelijk vormgegeven extern verzelfstandigd agentschap Vlaamse Vervoermaatschappij - De Lijn] | 13 | oldest version available, then each consolidated version: 1 June 2006 to 15 March 2024 |
| `decr-1976-03-03-1001628/` | Decreet van 3 maart 1976 tot bescherming van monumenten en stads- en dorpsgezichten | 7 | oldest version available, then each consolidated version: 1 June 2006 to 1 January 2015 |
| `decr-1991-01-23-1001876/` | Decreet van 23 januari 1991 betreffende de Vlaamse Instelling voor Technologisch Onderzoek | 3 | oldest version available, then each consolidated version: 30 November 2006 to 1 January 2010 |
| `decr-1986-12-23-1001879/` | Decreet van 23 december 1986 houdende uitroeping van het Ijzermonument en het omringende domein te Diksmuide tot memoriaal van de Vlaamse ontvoogding | 2 | oldest version available, then each consolidated version: 1 January 2010 to 20 August 2011 |
| `decr-1976-12-21-1001935/` | Decreet van 21 december 1976 houdende organisatie van de Vlaamse interuniversitaire samenwerking | 3 | oldest version available, then each consolidated version: 15 August 2006 to 1 October 2013 |
| `decr-1995-02-22-1001974/` | Decreet van 22 februari 1995 tot regeling van het administratief toezicht op de provincies in het Vlaamse Gewest | 2 | oldest version available, then each consolidated version: 1 June 2006 to 1 January 2014 |
| `decr-1990-07-12-1002022/` | Decreet van 12 juli 1990 houdende de regeling van de basiseducatie voor laaggeschoolde volwassenen | 6 | oldest version available, then each consolidated version: 1 June 2006 to 1 September 2010 |
| `decr-1994-12-21-1002023/` | Decreet van 21 december 1994 betreffende het onderwijs VI | 3 | oldest version available, then each consolidated version: 1 June 2006 to 1 January 2017 |
| `decr-1994-12-21-1002212/` | Decreet van 21 december 1994 houdende vaststelling van het wapen en de vlag van de provincies en gemeenten | 2 | oldest version available, then each consolidated version: 1 July 2006 to 1 January 2007 |
| `decr-1995-02-22-1002341/` | Decreet van 22 februari 1995 betreffende de bodemsanering | 5 | oldest version available, then each consolidated version: 1 July 2006 to 1 June 2008 |
| `decr-1991-07-24-1002550/` | Decreet van 24 juli 1991 jachtdecreet | 15 | oldest version available, then each consolidated version: 1 June 2006 to 20 August 2026 |
| `decr-1991-06-26-1002607/` | Decreet van 26 juni 1991 betreffende de erkenning en subsidiëring van het maatschappelijk opbouwwerk | 4 | oldest version available, then each consolidated version: 1 June 2006 to 1 January 2018 |
| `decr-1995-02-22-1002719/` | Decreet van 22 februari 1995 tot regeling van de invordering van niet-fiscale schuldvorderingen voor de Vlaamse Gemeenschap en de instellingen die eronder resso | 5 | oldest version available, then each consolidated version: 1 June 2006 to 8 December 2024 |
| `bijz-decr-2006-07-07-1015039/` | Bijzonder Decreet van 7 juli 2006 over de Vlaamse instellingen | 2 | as enacted, then each consolidated version: 27 October 2006 to 22 August 2008 |
| `bijz-decr-1988-12-19-1000612/` | Bijzonder Decreet van 19 december 1988 [betreffende de Vlaamse Autonome Hogescholen (verv. Bijz. Decr. 14 juli 1998, art. 69)] | 3 | oldest version available, then each consolidated version: 1 January 2009 to 1 October 2013 |
| `bijz-decr-1991-06-26-1002753/` | Bijzonder Decreet van 26 juni 1991 betreffende de Universiteit Gent [...] | 10 | oldest version available, then each consolidated version: 1 January 2013 to 1 September 2023 |
| `bijz-decr-1998-07-14-1006342/` | Bijzonder Decreet van 14 juli 1998 betreffende het gemeenschapsonderwijs | 2 | oldest version available, then each consolidated version: 1 September 2015 to 1 September 2026 |
| `bijz-decr-2002-07-19-1009703/` | Bijzonder Decreet van 19 juli 2002 houdende de controle op de mededelingen van de voorzitter van het Vlaamse Parlement | 1 | oldest version available, 30 November 2006 |
| `bijz-decr-2003-04-04-1011464/` | Bijzonder Decreet van 4 april 2003 houdende de deelname van gemeenschapsinstellingen aan de associaties in het hoger onderwijs | 1 | oldest version available, 1 October 2013 |
| `bijz-decr-2008-06-20-1016950/` | Bijzonder Decreet van 20 juni 2008 houdende vervanging van artikel 10 van het bijzonder decreet van 7 juli 2006 over de Vlaamse instellingen | 1 | as enacted, 22 August 2008 |
| `bijz-decr-2009-02-20-1017846/` | Bijzonder Decreet van 20 februari 2009 [betreffende de Hogere Zeevaartschool (verv. Bijz. Decr. 13 juli 2012, art. 45, I: 1 oktober 2013)] | 3 | as enacted, then each consolidated version: 1 January 2009 to 1 October 2013 |
| `bijz-decr-2011-07-08-1020563/` | Bijzonder Decreet van 8 juli 2011 tot aanvulling van het decreet houdende de organisatie van de lokale en provinciale verkiezingen en houdende wijziging van het | 2 | as enacted, then each consolidated version: 4 September 2011 to 3 December 2012 |
| `bijz-decr-2012-07-13-1022064/` | Bijzonder Decreet van 13 juli 2012 houdende wijziging van het bijzonder decreet van 4 april 2003 houdende de deelname van gemeenschapsinstellingen aan de associ | 1 | as enacted, 1 October 2013 |
| `bijz-decr-2012-07-13-1022097/` | Bijzonder Decreet van 13 juli 2012 houdende wijziging van het bijzonder decreet van 26 juni 1991 betreffende de Universiteit Gent en het Universitair Centrum An | 2 | as enacted, then each consolidated version: 1 January 2013 to 1 October 2013 |
| `bijz-decr-2012-07-13-1022262/` | Bijzonder Decreet van 13 juli 2012 houdende regeling van de bestuurlijke organisatie en werking van twee fusiehogescholen | 2 | as enacted, then each consolidated version: 14 September 2012 to 1 October 2013 |
| `bijz-decr-2012-07-13-1022267/` | Bijzonder Decreet van 13 juli 2012 houdende regeling van de bestuurlijke organisatie en werking van sommige publiekrechtelijke hogescholen | 3 | as enacted, then each consolidated version: 17 September 2012 to 1 October 2013 |
| `bijz-decr-2014-04-04-1024192/` | Bijzonder Decreet van 4 april 2014 houdende wijziging van het bijzonder decreet van 14 juli 1998 betreffende het gemeenschapsonderwijs, wat betreft de schoolraa | 1 | as enacted, 1 September 2015 |
| `bijz-decr-2014-04-25-1024202/` | Bijzonder Decreet van 25 april 2014 houdende wijziging van de regeling met betrekking tot de commissies van beroep in de publiekrechtelijke hogescholen en van d | 2 | as enacted, then each consolidated version: 1 October 2013 to 1 April 2014 |
| `bijz-decr-2017-02-03-1028015/` | Bijzonder Decreet van 3 februari 2017 tot wijziging van diverse bepalingen van het bijzonder decreet van 26 juni 1991 betreffende de Universiteit Gent en het Un | 2 | as enacted, then each consolidated version: 1 February 2017 to 1 January 2018 |
| `bijz-decr-2017-06-30-1028410/` | Bijzonder Decreet van 30 juni 2017 houdende wijziging van het Provinciedecreet van 9 december 2005 en van het Lokaal en Provinciaal Kiesdecreet van 8 juli 2011 | 1 | as enacted, 22 July 2017 |
| `bijz-decr-2018-06-15-1029538/` | Bijzonder Decreet van 15 juni 2018 tot wijziging van het decreet van 28 november 2008 betreffende de intergemeentelijke onderwijsvereniging en het bijzonder dec | 1 | as enacted, 23 July 2018 |
| `bijz-decr-2019-03-01-1030453/` | Bijzonder Decreet van 1 maart 2019 tot wijziging van het bijzonder decreet van 26 juni 1991 betreffende de Universiteit Gent en het Universitair Centrum Antwerp | 1 | as enacted, 1 September 2019 |
| `bijz-decr-2020-05-08-1032991/` | Bijzonder Decreet van 8 mei 2020 tot dringende, tijdelijke afwijking van het bijzonder decreet van 14 juli 1998 betreffende het gemeenschapsonderwijs naar aanle | 1 | as enacted, 9 May 2020 |
| `bijz-decr-2020-06-19-1033385/` | Bijzonder Decreet van 19 juni 2020 tot wijziging van artikel 5 en 22 van het bijzonder decreet van 26 juni 1991 betreffende de Universiteit Gent en het Universi | 1 | as enacted, 20 July 2020 |
| `bijz-decr-2022-07-15-1037324/` | Bijzonder Decreet van 15 juli 2022 tot wijziging van artikel 40sexies van het bijzonder decreet van 26 juni 1991 betreffende de Universiteit Gent en het Univers | 1 | as enacted, 19 August 2022 |
| `bijz-decr-2023-11-17-1039018/` | Bijzonder Decreet van 17 november 2023 tot wijziging van het bijzonder decreet van 26 juni 1991 betreffende de Universiteit Gent en het Universitair Centrum Ant | 1 | as enacted, 1 September 2023 |
| `bijz-decr-2024-05-17-1039770/` | Bijzonder Decreet van 17 mei 2024 tot wijziging van het bijzonder decreet van 14 juli 1998 betreffende het gemeenschapsonderwijs, wat betreft het onderwijs in d | 1 | as enacted, 1 September 2026 |
| `bijz-decr-2025-07-18-1041117/` | Bijzonder Decreet van 18 juli 2025 tot wijziging van de inwerkingtreding van het bijzonder decreet van 17 mei 2024 tot wijziging van het bijzonder decreet van 1 | 1 | as enacted, 31 August 2025 |

## Source

The Vlaamse Codex, the Flemish Government's consolidated collection of Flemish legislation (<https://codex.vlaanderen.be/>), through its Open Data API (<https://codex.opendata.api.vlaanderen.be/>). For each article it gives every version with its start and end date and the article of the act that made the change.

## Dates

- Each commit is dated at **noon, Europe/Brussels, on the day the version took effect**, as the Codex gives it. The date of the amending act is the `Enacted:` trailer, its publication in the Belgisch Staatsblad the `Published:` trailer.
- The Codex keeps every version only for texts published in the Belgisch Staatsblad from 1 June 2006. An act published from that day starts with its text as enacted, credited to the act itself. For an older act the history starts with the oldest text the Codex holds, dated no earlier than 1 June 2006 and credited to the publisher as the "oldest version available".
- Versions that take effect after the retrieval day are on the `toekomst` branch, never merged into `main`. Article versions whose start date is still to be set are left out.
- `--before="YYYY-MM-DD"` alone uses your clock's time of day; use `T23:59:59Z` or `tools/on.py`.

## Files

`<act>/art-005.md` is Art. 5, `art-005-1.md` Art. 5/1, `art-005-bis.md` Art. 5bis; `bijlage-...md` an annex. The first line is the article number; then one paragraph per line. Annotations are left out.

## How it is checked

- Every version of every act is read back from git on the day it took effect and on the day before (`tools/check_repo.py`); both must match `corpus.json`.
- The letters and digits of every article in every version equal those of the Codex's own text of the article version in force that day, read by a separate HTML parser.
- Health checks: no merge commits, commit dates never go backwards, nothing dated in the future, and every commit's trailers parse.

## What "author" means

The author of a commit is the amending act (decree, special decree, order), with an e-mail address that cannot exist (`<act key>@codex.vlaanderen.be.invalid`). The committer is always Lexifina.

## Limits

This is not an official publication. The binding text is the one published in the Belgisch Staatsblad. Only the acts listed above are included, and for acts published before 1 June 2006 the history starts in 2006 at the earliest.
