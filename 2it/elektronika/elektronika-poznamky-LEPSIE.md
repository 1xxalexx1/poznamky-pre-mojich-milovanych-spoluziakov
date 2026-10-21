# elektronika – poznámky

> **poznámka k prepisu (negácia):** negácia premennej je v zošite značená pruhom
> nad písmenom. v tomto prepise ju zapisujem ako `a̅`, `b̅`, `c̅`, `d̅` (prípadne
> `¬a`). na niektorých miestach (vyznačené ďalej) pruhy nad jednotlivými
> premennými na fotografii **nie sú čitateľné** – tam je to výslovne upozornené.

---

## logické obvody

- je hmotný systém realizujúci prostredníctvom logických signálov niektorú logickú funkciu
- logická funkcia **f** – konečného počtu nezávislých logických premenných je akékoľvek jednoznačné priradenie pravdivostnej hodnoty závislej logickej premennej **y** pravdivostným hodnotám nezávislých logických **x**
  - ⟹ **y = f(x)**

- logická funkcia **f** – zobrazenie z množiny výrokov do množiny pravdivostných hodnôt (1 – true a 0 – false)
- pravdivý výrok je logická 1-ka, **y = 1**
- nepravdivý výrok je logická 0, **y = 0**
- **pravdivostná tabuľka** – tabuľka, v kt. sú uvedené všetky možné kombinácie hodnôt nezávislých premenných a im odpovedajúce hodnoty závislých premenných
  - ⟹ táto tabuľka má toľko stĺpcov, koľko je vyšetrovaných logických premenných, a toľko riadkov, koľko existuje kombinácií pravdivostných hodnôt nezávislých premenných

- **logický výraz**
- popisuje logické vzťahy medzi logickými operandami pomocou logických operátorov a využíva symboliku analogickú klasickej algebre
- pre súbor **n** logických premenných, kde xᵢ ⟹ i = 1, 2, … n, existuje:
  - 2ⁿ rôznych vstupných kombinácií týchto premenných (dvojica)
  - 2^(2ⁿ) rôznych logických funkcií y (pretože každá z nezávislých premenných môže nadobudnúť 2 hodnoty (0, 1), teda j = 1, 2, 3; … 2^(2ⁿ))
  - s rastúcim počtom log. premenných n teda počet parciálne rôznych funkcií, kt. možno týmto premenným priradiť, prudko narastá

- **štandardný súčtový tvar**
  - ⟹ získame tak, že v každom riadku pravdivostnej tabuľky, kde má závislá premenná (y) pravdivostnú hodnotu 1, vynásobíme priamu al. vynegovanú pravdivostnú hodnotu každej nezávislej premennej xy podľa toho, či má táto premenná pravdivostnú hodnotu 1 al. 0
  - príslúchajúcou premennou získame súčiny, vynásobíme a takto získané súčiny sčítame
- **štandardný súčinový tvar**
  - ⟹ získame tak, že v každom riadku pravdivostnej tabuľky, kde má závislá premenná pravdivostnú hodnotu 0, vynásobíme priamu al. negovanú pravdivostnú hodnotu každej nezávislej premennej xy podľa toho, či má táto premenná prav. hod. 0 al. 1 príslúchajúcou premennou
  - získané súčiny sčítame a takto získané súčty vynásobíme

- **súčtová normálová forma – 1**
  - ⟹ y = (a·b·c) + (a·b·c) + (a·b·c) + (a·b·c) + (a·b·c)
- **súčinová normálová forma – 0**
  - ⟹ y = (a+b+c) · (a+b+c)

> ℹ️ **pozn.:** pri kontrole v plnom rozlíšení fotografie **nad premennými v
> týchto dvoch normálových formách nie sú napísané žiadne pruhy negácie** —
> nejde teda o nečitateľnosť, ale o to, že v zápise jednoducho chýbajú (zrejme
> všeobecný/ilustračný zápis bez vyznačenia, ktoré členy sú negované). štruktúra
> (počet členov, súčiny/súčty) je prepísaná verne.

**pravdivostná tabuľka k príkladu** &nbsp; y = a ⟹ (b ⟺ c)

| a | b | c | y |
|---|---|---|---|
| 1 | 1 | 1 | 1 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 |
| 1 | 0 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 0 | 0 | 1 |

---

## kombinačné logické obvody

- **klo** (kombinačné log. obvody) sú obvody, kde výstupná hodnota **y** zavisí od okamžitej hodnoty vstupných signálov a od ich vzájomnej kombinácie

### negácia
- obvod je invertor – **not**
- funkcia je inverzia
- not – **mh 7404**
- y = a̅ (a negované)

| a | y |
|---|---|
| 0 | 1 |
| 1 | 0 |

- guľôčka (krúžok) = negácia
- logická 0 – 0 v, gnd, zem, nízka, low (⊖)
- log. 1 – 5 v, high – h (⊕)

> schéma: zobrazené značky pre invertor (trojuholník s krúžkom, resp. obdĺžnik
> s „1") a rozkreslené vývody puzdra io (5 v / high hore, gnd / 0 v / low dole),
> s popismi **mh7404** a **mh7408**.

### konjunkcia
- logický súčin
- obvod je **and**
- funkcia: **y = a·b**
- **mh7408** – integrovaný obvod

| a | b | y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

### disjunkcia
- logický súčet
- obvod je **or**
- funkcia: **y = a + b**
- **mh 7432** – ic

| a | b | y |
|---|---|---|
| 0 | 0 | 0 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 1 |

> schéma s led: „1 svieti, 0 nesvieti".

### negovaný logický súčin
- obvod je **nand**
- **y = a·b** (s pruhom nad celým súčinom: y = (a·b)̅ )
- **mh7400, mh7403, mh7410, mh7420, mh7430**
  - 2 vst. / 1 vys.
  - 3 vst. / 1 vys.
  - 4 vst. / 1 vys.
  - 8 vst. / 1 vys.

| a | b | y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

### negovaný logický súčet
- **nor**
- **mh7402**
- **y = (a+b)̅**

| a | b | y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

### exkluzívny logický súčet
- **ex-or** alebo **x-or**
- **mh7486**
- **y = a ⊕ b**
  - (exkluzívny súčet = znamená „exkluzívne")
- značka v schéme: **=1**

| a | b | y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

### exkluzívne negovaný logický súčet
- **ex-nor / x-nor**
- koncovka **66**
- **y = (a ⊕ b)̅**
- značka v schéme: **=1**

| a | b | y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

---

## súčiastky / zariadenia klo

### polovičná sčítačka
- používa sa: **ex-or**
  - ⟹ len v prípade, že obidva vstupy sú 1, dokáže síce vypočítať súčet 1 + 1 = 0, ale nedokáže vygenerovať tzv. prenos **p** do vyššieho rádu
  - túto funkciu docielime pridaním člena **and** na vstup obvodu ex-or; dostaneme tak zapojenie, ktoré sa nazýva **polovičná sčítačka**
- na obr. sú **a** a **b** sčítance, **s** je súčet a **p** je prenos
- rovnakú funkciu vzniku prenosu získame pripojením invertora na výstup prvého člena **nand** v obvode ex-or

> schémy: realizácia polovičnej sčítačky z hradiel (ex-or pre súčet s a and pre
> prenos p), aj alternatíva zostavená z nand hradiel.

### bloková schéma pre 1/2 add
> a, b → **=1 (xor)** → s &nbsp;&nbsp; a &nbsp;&nbsp; a, b → **& (and)** → p.
> blok označený **„1/2 add"** so vstupmi a, b a výstupmi p (prenos) a s (súčet).

### úplná sčítačka
- získame spojením 2 polovičných (sčítačiek)
- sčíta 2 vstupné bity
  - ⟹ dokáže pripočítať k tomuto súčtu binárny prenos z nižšieho rádu
  - zaisťuje ďalší bit prenosu do ďalšieho rádu

> schéma: vstupy a, b a prenos p₁; dve hradlá **=1 (xor)** → výstup s; hradlá
> **& (and)** a hradlo **≥1 (or)** → výstupný prenos p₂.

### generátor parity – g.p.
- je kombinačný logický obvod, kt. identifikuje vznik chyby v binárnom slove (1 al. 0)
- g.p. si prehliadne binárne slovo a generuje jednoduchý výstupný tzv. **paritný bit**, kt. je prenášaný alebo uchovávaný a použije sa v kontrole prenášaného (uchovávaného) slova
- ak je v binárnom slove **párny** počet logických hodnôt 1, bude paritný bit rovný 0 ⟹ pb = 0
- ak je v bin. slove **nepárny** počet log. hodnôt 1, bude paritný bit rovný 1

### kóder
- sú prevodníky, kt. slúžia k prevodu čísel v niektorom kóde do iného kódu
- kódery sú kombinačné log. obvody, kt. z 1 alebo viac vstupov odpovedajúcich 10-sústave prevádzajú 10. číslo do 2-sústavy
- zapojenie kódera zostrojíme pomocou kódovacej tabuľky; k tomu použijeme členy **nand**, kde vieme, že privedením log. 0 na aspoň 1 vstup (čo sa realizuje uzemnením tohto vstupu) dostaneme na jeho výstupe log. 1

| vstup („10") | výstup b a |
|:---:|:---:|
| 0 | 0 0 |
| 1 | 0 1 |
| 2 | 1 0 |
| 3 | 1 1 |

> schéma: zapojenie s nand hradlami, výstupy a a b, vstupy 0, 1, 2, 3
> (so znakmi + a − pre napájanie / zem).

> ⚠️ **neisté slovo:** v texte „prevodu čísel v ___ kóde" je rukopisné slovo
> ťažko čitateľné (vyzerá ako „niahom"); pravdepodobne malo byť „niektorom"
> / „nejakom".

### dekóder
- k.l.o., kt. zaisťuje buď prítomnosť určitého bin. čísla, al. zisťuje stav bin. čísla

| b | a | des. č. | y |
|---|---|:---:|:---:|
| 0 | 0 | 0 | b̅·a̅ |
| 0 | 1 | 1 | b̅·a |
| 1 | 0 | 2 | b·a̅ |
| 1 | 1 | 3 | b·a |

> schéma: vstupy a, b, dva invertory (a̅, b̅) a štyri hradlá **& (and)** s výstupmi:
> - 0: y = a̅·b̅
> - 1: y = a·b̅
> - 2: y = a̅·b
> - 3: y = a·b

---

## karnaughova mapa – km

### km pre 2 premenné &nbsp; (a, b – 2ⁿ = 4)

|     | a̅ | a |
|-----|----|----|
| **b̅** | a̅·b̅ | a·b̅ |
| **b**  | a̅·b  | a·b  |

> poznámka v zošite pri jednom políčku: „toto políčko nepatrí do pásu (a),
> patrí do (b)".

### km pre 3 premenné &nbsp; (2³ = 8 ⟹ n = 3)

|     | b̅·c̅ | b̅·c | b·c | b·c̅ |
|-----|------|------|-----|------|
| **a̅** | a̅·b̅·c̅ | a̅·b̅·c | a̅·b·c | a̅·b·c̅ |
| **a**  | a·b̅·c̅  | a·b̅·c  | a·b·c  | a·b·c̅  |

### km pre 4 premenné &nbsp; (2⁴ = 16)

|     | a̅·b̅ | a·b̅ | a·b | a̅·b |
|-----|------|-----|-----|------|
| **d̅·c̅** | a̅·b̅·c̅·d̅ | a·b̅·c̅·d̅ | a·b·c̅·d̅ | a̅·b·c̅·d̅ |
| **d̅·c**  | a̅·b̅·c·d̅  | a·b̅·c·d̅  | a·b·c·d̅  | a̅·b·c·d̅  |
| **d·c**   | a̅·b̅·c·d   | a·b̅·c·d   | a·b·c·d   | a̅·b·c·d   |
| **d·c̅**  | a̅·b̅·c̅·d  | a·b̅·c̅·d  | a·b·c̅·d  | a̅·b·c̅·d  |

> ⚠️ **upozornenie ku karnaughovým mapám:** je prepísaná štandardná štruktúra
> máp. presné umiestnenie jednotlivých pruhov negácie v každej bunke 3- a
> 4-premennej mapy je na fotografii len ťažko overiteľné políčko po políčku –
> odporúčam porovnať s originálom.

---

## karnaughova mapa – riešený príklad

**f = (a, b, c)**, &nbsp; 2³ = 8 &nbsp; — disjunktná (d) = log. 0 → štandardný log. súčet
&nbsp; **d(3, 4, 6, 8)** &nbsp; (čísla riadkov, kde y = 1)

**① pravdivostná tabuľka**

| a | b | c | y |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 |

- pravidlo: **1 = disjunktná**, **0 = konjunktná**
- 1 ide do tabuľky tam, kde je 1; tam, kde je 0, ide do tabuľky 0
- tam, kde je „x", sa nenachádza; „1" = x sa nachádza

**② karnaughova mapa a výsledok**

|     | b̅·c̅ | b·c̅ | b·c | b̅·c |
|-----|------|------|-----|------|
| **a̅** | 0 | 1 | 1 | 0 |
| **a**  | 0 | 0 | 1 | 1 |

zoskupenia (každý pár musí mať 2 písmená rovnaké):

> **f = (b·a̅) + (b·c) + (a·c)**

poznámky:
- „keby mám 1 na konci, tak sa to obráti"
- pre tie isté písmená: 1 → b a b, c a c; bc a bc (mohlo by byť aj b̅ a b̅)
- výstupné členy realizované cez **nand**

**③ realizácia v nand**

> - b, a̅ → **&** → (b·a̅)̅
> - b, c → **&** → (b·c)̅
> - a, c → **&** → (a·c)̅
> - výstupné nand: **y = ((b·a̅)̅ · (b·c)̅ · (a·c)̅)̅**  → čo sa rovná (b·a̅) + (b·c) + (a·c)

**④ zapojenie** — *(v zošite len nadpis „zapojenie", schéma nedokreslená)*

---

## Sekvenčné logické obvody – S.l.o.

- majú tú vlastnosť, že ich výstupné premenné sú určené nie len kombináciou vstupných premenných v danom okamihu, ale aj minulými hodnotami niektorých premenných
  - ⟹ z toho vyplýva, že si s.l.o. musí pamätať hodnoty z predchádzajúcich stavov, čo znamená, že musí obsahovať **pamäťové členy**
- základom s.l.o. sú **preklápacie obvody**, z kt. sa ďalej konštruujú čítače, registre a pamäťové obvody

---

## Klopný obvod typu RS – asynchrónny

- realizovaný z 2 obvodov **NAND** al. **NOR**
- **1.** rozoberieme si vstup, keď **R = 1 a S = 0**
  - ⟹ z pravdivostnej tabuľky členov NOR vieme, že má na výstupe log. 1 len v prípade oboch vstupov v log. 0
  - táto podmienka je splnená u horného člena NOR, pretože vstup R = 1, a preto výstup **Q = 0** → dióda nesvieti
  - táto log. 0 sa dostane spätnou väzbou na vstup dolného člena NOR a ten vytvorí na svojom výstupe **Q̅ = 1**
  - spätná väzba na horný člen NOR jeho výstup nezmení
  - tým je jednoznačne daný výstup klopného obvodu **Q = 0, Q̅ = 1**
  - ⟹ tomuto stavu hovoríme **reset** – vynulovanie obvodu – hlavný výstup Q = 0

- **2.** ak zmeníme R = 0 – vstup horného člena NOR na 0
  - ⟹ vplyvom spätnej väzby z dolného člena zostane jeho 2. vstup 1 a jeho výstup bude preto Q = 0
  - výstup dolného člena bude zo vstupov 0 a 0 ⟹ Q̅ = 1
  - oba výstupy sa po vynulovaní vstupov zo stavu reset nezmenili

- **3.** opačná situácia **R = 0; S = 1** oproti stavu reset
  - ⟹ výstup bude opačný → **Q = 1; Q̅ = 0**
  - tomuto stavu hovoríme **set** (nastavenie) – obvod má hlavný výstup Q = 1

- **4.** pri zmene **S = 1 na S = 0**
  - ⟹ sú opäť výstupy Q = 1; Q̅ = 0, nezmenia sa
  - teraz sú tieto výstupy pre S = 0 a R = 0 práve opačné oproti vynulovaniu obvodu zo stavu reset

- prechod z oboch stavov reset a set do stavu vynulovania vstupov vyjadruje pravdivostná tabuľka:

| | R | S | Q | Q̅ |
|---|---|---|---|---|
| **reset** | 1 | 0 | 0 | 1 |
| **set** | 0 | 1 | 1 | 0 |
| | 0 | 0 | 1 | 0 |
| | 0 | 0 | 0 | 1 |

> Posledné dva riadky (R = 0, S = 0) predstavujú držanie predchádzajúceho stavu
> (Q ostáva podľa toho, či predtým nastal set alebo reset).

- **komplikovaná situácia** nastane, ak **R = 1 a S = 1 (zároveň)** – set a reset naraz
  - ⟹ v tom prípade podľa pravdivostnej tabuľky NOR obidva výstupy **Q aj Q̅ sú v log. 0**
  - to by tak nevadilo, ale pri zmene R al. S na 1 al. 0 nastane labilná situácia, kedy všetky výstupy sú teraz v log. 0 a oba členy NOR sa snažia vytvoriť na výstupe log. 1 – ale kde ju vytvoria? Nie je to jednoznačne dané a obvod prejde náhodne do akéhokoľvek stavu

| R | S | Q | Q̅ |
|---|---|---|---|
| 0 | 0 | 0/1 | 1/0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 1 |
| 1 | 1 | X | X &nbsp; *(zakázaný stav)* |

> Riadok R = 0, S = 0 (Q = 0/1, Q̅ = 1/0) znamená držanie predchádzajúceho stavu.

---

## Klopný obvod RS – synchrónny

- ak doplníme klopný obvod RS asynchrónny ďalšími 2 členmi NAND (pred), dostaneme obvod s rovnakými vlastnosťami, ale jeho výstup bude možné meniť len v priebehu synchronizačného hodinového impulzu – je to **CLOCK**
- ak chýba hodinový impulz **C = 0**, je obvod pomocou prvých členov NAND zablokovaný, pretože ich výstup je trvale = 1 a akákoľvek zmena R al. S nemôže zmeniť výstup Q
- obvod sa otvorí až s príchodom hodinového impulzu **C = 1** a jedine v dobe jeho trvania je možné pomocou vstupov R a S meniť výstup Q
- výstupné členy NAND tu pôsobia ako invertory, a preto bude zakázaný stav opačný – to znamená **S = R = 1**
- z rovnakého dôvodu je nutné prehodiť vstupy R a S, aby platilo pre SET a RESET odpovedajúce nastavenie výstupného klopného obvodu

---

## Klopný obvod D

- odstraňuje zakázaný stav prepojením vstupu klopného obvodu RS invertorom (v obidvoch)
- obvod je riadený – synchronizovaný – hodinovým vstupom
- klopný obvod prehlopí len v priebehu hodinového impulzu, ináč je zavretý
- invertor zaisťuje, že vstupy do pôvodného klopného obvodu RS môžu byť len rozdielne

> Schéma: zapojenie z hradiel **& (NAND)** s hodinovým vstupom C a vstupom D
> cez invertor.

---

## Klopný obvod JK (Jack Kilby) – JK

- zdokonalený klopný obvod RS, ktorý nemá zakázaný stav vstupných premenných
- to je docielené pridaním súčinových členov **AND** do vstupov **S** a **R** a zavedením spätnej väzby z výstupu klopného obvodu na vstup tretieho člena AND
- zabráneniu vzniku zakázaného stavu je docielené takým spôsobom, že máme zaistením:
  1. nulového spätnoväzobného vstupu (ak je Q = 0) pre dolný súčinový člen AND, alebo
  2. nulového spätnoväzobného vstupu (ak je Q̅ = 0) pre horný súčinový člen AND

> Schéma: vstupy **J = 1, C = 0, K = 1**, súčinové členy **& (AND)** a hradlá
> **NAND** so spätnými väzbami, výstupy **Q = 0** a **Q̅ = 1**.

---

## Klopný obvod typu T

- klopný obvod tohto typu získame prepojením oboch (obidvoch) vstupov J a K klopného obv. typu JK; vznikne jediný vstup označený **T**
- pri tomto zapojení, ak je trvale **T = 1**, pracuje obvod tak, ako keby J a K boli = 1 v predchádzajúcom obvode
- ak je **T = 1**, stav na výstupe sa mení na opačný pri každom príchode synchronizačného hodinového impulzu **C**
- ak je **T = 0**, obvod zostáva v pôvodnom stave

> Schémy: blok JK (vstupy J, C, K → výstupy Q, Q̅) a blok T (vstupy T, C →
> výstupy Q, Q̅).
