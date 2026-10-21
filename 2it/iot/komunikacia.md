---
source: "iot.pdf"
tags: [iot, komunikacia, osi, 2_it]
date_transcribed: "2026-04-25"
legibility: "high"
---

# Komunikácia

- 2-smerný proces so snahou výmeny informácií
- aby mohla komunikácia prebehnúť, sú potrebné tieto prvky:
    - odosielateľ, prijímateľ [sic — v texte „prijemca"], informácia, správa, médium, kódovanie, dekódovanie
- v komunikácii sa objavuje, ale nie je nevyhnutné:
    - odpoveď, spätná väzba, šum
- účelom kom. je výmena info.

## Informácia v komunikácii

- informácia je názov pre obsah toho, čo sa vymieňa s vonkajším svetom, keď sa mu prispôsobujeme a ovplyvňujeme ho
- info. môžu byť zakódované za účelom:
    - efektivity
    - zabezpečenia
- každé zar. môže poskytovať alebo spracovávať dáta
- existuje niekoľko typov info — pre jeho optimálne spracovanie sa môžu vyžadovať odlišné systémy
- mnoho systémov využíva **API** (Application Programming Interface) — rozhrania, ktoré zabezpečujú, aby systémy dostali aktuálne dáta

## Metadáta

- pri prenose dát sa stretávame s konceptom metadát — info. o info.
- slúžia na opis, organizáciu, vyhľadávanie, správu dát
- metadáta poskytujú info o vlastnostiach al. obsahu dát

### Typy metadát

- **popisné** — obsah al. charakteristiky — autor, dátum, názov
- **technické** — info o technických vlastnostiach — formát, veľkosť, rozlíšenie
- **administratívne** — info o správe dát — prístupové práva, dátum úpravy, licencie
- **štrukturálne** — umožňujú organizáciu a navigáciu v rámci dát — poradie stránok v dokumente

## Príkazy

- inštrukcie, pokyny, ktoré prijímateľ vykoná
- príkaz obsahuje jasne definovanú akciu, ktorú treba vykonať
- skriptovací / terminálový jazyk — inštrukcia PC na vykonanie úlohy

## Prevádzkové info

- info na riadenie, monitorovanie, optimalizáciu

### Charakteristiky

- **aktuálnosť**
- **praktická využiteľnosť** — konkrétne akcie, ktoré zlepšujú al. udržiavajú prevádzku
- **jednoduchá interpretácia** — priamo použiteľné bez analýzy
- **presnosť, spoľahlivosť**

## Spracovanie dát

- dáta sú spracované al. uchované pomocou operácií:
    - **transformácia**: prevod dát do iného formátu, napr. napätie → teplotu
    - **agregácia**: kombináciou dát možno aplikovať štatistickú analýzu — napr. filtrácia chybných údajov
    - **obohatenie**: kombinácia údajov z rôznych zariadení alebo s inými súbormi
    - **presúvanie**: získanie na 1. mieste, spracovávanie na 2., ukladanie na 3.

# Komunikačný model OSI

- pre pochopenie konceptu bol vytvorený model OSI ako jeden z mnohých
- je len teoretický

## Vrstvy stroja a médií

- vrstvy stroja: aplikačná, prezentačná, relačná, transportová
- médiá: sieťová, spojová, fyzická

## Účel modelu

- pomáha zlepšovaniu rozvoja technológií — zmena v 1 vrstve neovplyvňuje komunikáciu v iných vrstvách
- pomáha navrhovať nové komunikačné štandardy — protokoly
- podporuje konkurenciu podnikov

## Vrstvy podrobne

### Fyzická

- popisuje fyzickú časť siete
- definuje logickú 0 a 1
- popisuje konektory, vodiče, parametre vodičov

### Spojová

- popisuje komunikáciu medzi 2 spojenými zariadeniami
- je v nej špecifikované, ako sú definované adresy jednotlivých zariadení

### Sieťová

- rieši výber cesty na komunikáciu zo susednej siete (čo najrýchlejšie, bez straty)

### Transportná

- úlohou je overiť správne doručenie medzi cieľom a odosielateľom

### Relačná

- úlohou je udržiavať spojenie medzi aplikáciami na koncových zariadeniach
- zabezpečuje potrebnú výmenu dát bez prerušenia

### Prezentačná

- úloha je prezentovať dané dáta
- šifrovanie
- pripojenie headera a footera

### Aplikačná

- rozhrania medzi používateľom a sieťou

## Súvisiace

- [[zettelkasten/30 - permanent/school/transcribed/2_it/iot/spojenia]]
- existujúca poznámka vo vaulte: [[school/2it/iot/protokoly]]

## Poznámky k prepisu

- Originál pri vrstvách OSI píše „aplikačná, prezentačná, relačná, transportová {stroj}; sieťová, spojová, fyzická {médiá}". Toto rozdelenie odráža logiku TCP/IP vs. fyzické médiá, prepísané verne.
- „prijemca" → ponechané ako „prijímateľ" pre konzistenciu (vyžadované definíciou komunikácie).
