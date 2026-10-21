# Elektronika — Logické obvody

---

## Logické obvody

- je to hnodný systém realizujúci prostredníctvom logických signálov rôzne logické funkcie
- **logická funkcia F** — konečného počtu nezávislých logických premenných je akékoľvek jednoznačné priradenie pravdivostnej hodnoty závislej logickej premennej `y` pravdivostným hodnotám nezávislých logických `x`

$$\Rightarrow y = F(x)$$

- **logická funkcia F** — zobrazenie z množiny výrokov do množiny pravdivostných hodnôt (1 = true a 0 = false)
- **pravdivý výrok** je logická 1 — áno, `y = 1`
- **nepravdivý výrok** je logická 0, `y = 0`
- **pravdivostná tabuľka** — tabuľka v kt. sú uvedené všetky možné kombinácie hodnôt nezávislých premenných a im odpovedajúce hodnoty závislých logických premenných
  - táto tabuľka má toľko stĺpcov koľko je uvažovaných logických premenných a toľko riadkov koľko existuje kombinácií pravdivostných hodnôt nezávislých premenných

### Logický výraz

- popisuje logické vzťahy medzi logickými operátormi pomocou logických operátorov a vyžíva symboliku analogickú klasickej algebre
- pre súbor n-logických premenných kde `xᵢ => i = 1, 2, ..., n` existuje:
  - `2ⁿ` rôznych vstupných kombinácií týchto premenných, teda `2ⁿ` rôznych logických funkcií `y` (pretože každá z n nezávislých premenných môže nadobudnúť 2 hodnoty `(0, 1)`, pre `j = 1, 2, 3, ..., 2²ⁿ`)
  - s rastúcim počtom logických premenných n, teda počet navzájom rôznych funkcií kt. možno týmto premenným priradiť prudko narastá

### Štandardný súčtový tvar

- získame tak, že v každom riadku pravdivostnej tabuľky kde má závislá premenná `y` pravdivostnú hodnotu 1, vynásobíme priamo alebo vynegovanú pravdivostnú hodnotu každej nezávislej premennej `x` podľa toho, či má tá premenná pravdivostnú hodnotu 1 alebo 0
- príslušnými premennými získame súčiny, vynásobíme a takto získané súčiny sčítame

### Štandardný súčinový tvar

- získame tak, že v každom riadku pravdivostnej tabuľky kde má závislá premenná `y` pravdivostnú hodnotu 0, vynásobíme priamo alebo negovanú pravdivostnú hodnotu každej nezávislej premennej `x` podľa toho, či má tá premenná pravdivostnú hodnotu 0 alebo 1
- príslušnou premennou získané súčiny sčítame a takto získané súčty vynásobíme

- **súčtová normálová forma-1:**

$$\Rightarrow y = (A \cdot B \cdot C) + (A \cdot B \cdot \bar{C}) + (A \cdot \bar{B} \cdot C) + (\bar{A} \cdot B \cdot C) + (A \cdot B \cdot C)$$

- **súčinová normálová forma-0:**

$$\Rightarrow y = (A + B + C) \cdot (A + B + \bar{C})$$

**Príklad — pravdivostná tabuľka** (`y = A => (B <= C)`):

| A | B | C | y |
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

## Kombinačné logické obvody

- **KLO** (kombinačné log. obvody) sú obvody kde výstupná hodnota `y` závisí od okamžitej hodnoty vstupných signálov a od ich vzájomnej kombinácie

### Negácia

- obvod je **invertor — NOT**
- funkcia je **inverzia**
- NOT — MH7404
- `y = Ā` (A negované)

| A | y |
|---|---|
| 0 | 1 |
| 1 | 0 |

- logická 0 = 0V, GND, Zem, nízka, Low
- logická 1 = 5V, High

*(diagram: TTL — 5V = HIGH, 0V = LOW; MH7404, MH7408; AND aj OR aj NAND)*

---

### Konjunkcia

- logický súčin
- obvod je **AND**
- funkcia: `Y = A · B`
- MH7408 — integrovaný obvod

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

---

### Disjunkcia

- logický súčet
- obvod je **OR**
- funkcia: `Y = A + B`
- MH7432 — IC

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 1 |

*(diagram: 1 svieti; 0 nesvieti; LED)*

---

### Negovaný logický súčin

- obvod je **NAND**
- `Y = Ā·B`
- MH7400, MH7403, MH7410, MH7420, MH7430

|         | vstupy | výstupy |
|---------|--------|---------|
| MH7400  | 2 vst., 1 výs. | |
| MH7410  | 3 vst., 1 výs. | |
| MH7420  | 4 vst., 1 výs. | |
| MH7430  | 8 vst., 1 výs. | |

| A | B | Y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

---

### Negovaný logický súčet

- **NOR**
- MH7402
- `Y = Ā+B`

| A | B | Y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

---

### Exkluzívny logický súčet

- EX-OR alebo X-OR
- MH7486
- `Y = A ⊕ B`
  - exkluzívny súčet = znamenené exkluzívne

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

---

### Exkluzívne negovaný logický súčet

- EX-NOR / X-NOR
- koncovka 66
- `Y = A ⊙ B`

| A | B | Y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

---

## Súčiastky / zariadenia KLO

### Polovičná sčítačka

- používa sa: EX-OR
- len v prípade že obidva vstupy sú 1 dokáže síce vypočítať súčet `1+1=0` ale nedokáže vygenerovať tzv. prenos `P` do vyššieho rádu
- túto funkciu docielime pridaním členu AND na vstup obvodu EX-OR — dostaneme tak zapojenie ktoré sa nazýva **polovičná sčítačka**
- na obr. sú A a B sčítance, S je súčet a P je prenos
- rovnakú funkciu vzniku prenosu získame pripojením invertora na výstup prvého člena NAND v obrade EX-OR

*(diagram: bloková schéma pre 1/2 ADD — vstup A, B; výstupy P→, S→)*

---

### Úplná sčítačka

- získame spojením 2 polovičných
- sčíta 2 vstupné bity
- dokáže pripočítať k tomuto súčtu binárny prenos z nižšieho rádu
- zaistuje ďalší bit prenosu do ďalšieho rádu

*(diagram: bloková schéma úplnej sčítačky: P vstup, A, B → [EX-OR] → [AND] → P výstup, S výstup)*

---

### Generátor parity — G.P.

- je kombinačný logický obvod kt. identifikuje vznik chyby v binárnom slove (1 alebo 0)
- G.P. si prehliadne binárne slovo a generuje jednoduchý výstupný tzv. **paritný bit** kt. je prenášaný alebo uchovávaný a použije sa v kontrole prenášaného/uchovávaného slova
- ak je v binárnom slove párny počet logických hodnôt 1, bude paritný bit rovný 0 ⇒ `PB = 0`
- ak je v bin. slove nepárny počet log. hodnôt 1, bude paritný bit rovný 1

---

### Kóder

- sú prevodníky kt. slúžia k prevodu čísel v inom kóde do iného kódu
- kódery sú kombinačné log. obvody kt. z 1 alebo viac vstupov zodpovedajúcich 10-sústave prevádzajú to číslo do 2 sústavy
- zapojenie kódera zostrojíme pomocou kódovacej tabuľky kt. k tomu použijeme členy NAND, lebo vieme, čo privedením log. 0 na aspoň 1 vstup, čo sa realizuje uzemnením tohto vstupu, dostaneme na jeho výstupe log. 1

**Kódovacia tabuľka:**

| vstup "10" | výstup B | A |
|-----------|---------|---|
| 0         | 0       | 0 |
| 1         | 0       | 1 |
| 2         | 1       | 0 |
| 3         | 1       | 1 |

*(diagram: kóder so 4 vstupmi 0,1,2,3 a výstupmi A, B cez hradlá NAND)*

---

### Dekóder

- kt. zaistujú buď prítomnosť určitého bin. čísla al. zisťujú stav bin. čísla

**Tabuľka:**

| B | A | des.č. | y       |
|---|---|--------|---------|
| 0 | 0 | 0      | B̄·Ā    |
| 0 | 1 | 1      | B̄·A    |
| 1 | 0 | 2      | B·Ā    |
| 1 | 1 | 3      | B·A    |

*(diagram: dekóder s 2 vstupmi a 4 výstupmi cez hradlá AND)*

---

## Karnaughova mapa — KM

### KM pre 2 premenné, A,B — 2² = 4

```
    A  Ā
B | 1  0 |
B̄| 0  0 |
```

*(toto políčko nepatrí do pásu (A), patrí do pásu (B))*

### KM pre 3 premenné, 2³ = 8 ⇒ n = 3

```
        B̄C̄   B̄C   BC   BC̄
A  |  A·B̄·C̄ | A·B̄·C | A·B·C | A·B·C̄ |
Ā  | Ā·B̄·C̄ | Ā·B̄·C | Ā·B·C | Ā·B·C̄ |
```

### KM pre 4 premenné, 2⁴ = 16

```
         ĀB̄    AB̄    AB    ĀB
D̄C̄ | Ā·B̄·C̄·D̄ | A·B̄·C̄·D̄ | A·B·C̄·D̄ | Ā·B·C̄·D̄ |
D̄C  | Ā·B̄·C·D̄ | A·B̄·C·D̄ | A·B·C·D̄  | Ā·B·C·D̄  |
DC  | Ā·B̄·C·D  | A·B̄·C·D  | A·B·C·D   | Ā·B·C·D   |
DC̄  | Ā·B̄·C̄·D  | A·B̄·C̄·D  | A·B·C̄·D   | Ā·B·C̄·D  |
```

---

### Príklad — KM (strana 6)

`F = (A, B, C)` ≠ 2³ = 8

Disjunktná (D) = log. 0 — štandardný log. súčet: `D(3, 4, 6, 8)` → `(·) + (·) +`

*(diagram: KM 3 premenných s označenými políčkami)*

**① Pravdivostná tabuľka:**

| A | B | C | y |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 1 ← disjunktná |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 ← disjunktná |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 |

*(kde je 1 = disjunktná A; kde je 0 = konjunktná A; Y ide sem: tam kde je 0 ide do tabuľky 0; tam kde je X sa nenachádza — // X sa nachádza)*

**② KM:**

```
        B̄·C̄   BC̄   BC   B̄C
Ā  | 0 | (1) | (1) | 0 |
A  | 0 |  0  | (1) | 1 |
```

*(každý pár musí mať 2 písmená rovnaké: napr. C 1 B a B; C a C; BC a BC; (možno by byt aj BaB))*

**Výsledok ②:**

$$F = (B \cdot \bar{A}) + (B \cdot C) + (A \cdot C)$$

*(NAND)*

**③ Zapojenie cez NAND:**

- vstupy: B, Ā → AND → B·Ā
- vstupy: B, C → AND → B·C
- vstupy: A, C → AND → A·C
- výstupy všetkých AND do AND:

$$y = \overline{B \cdot \bar{A}} \cdot \overline{B \cdot C} \cdot \overline{A \cdot C}$$

④ Zapojenie *(diagram v zošite)*

---

### Multiplexor

- sú prepinacie k.l.o. kt. z niekoľkých vstupných premenných prepínajú na 1 výstup podľa hodnôt riadiacich signálov
- riadiacimi signálmi môžu byť výstupné signály z dekódera

**Použitie multiplexora:**
- prepínanie signálov
- prevod paralelných dát na sériové
- generátor sériového binárneho slova
- al. vytváranie booleovských funkcií

**Princíp multiplexora s dekóderom:**
- do multiplexora prichádzajú 4 samostatné vstupy — každý na jeden obvod NAND + 4 samostatné vstupné NAND obvody
- dekóder má log. 1 len na 1 zo svojich výstupov a tento otvorí príslušný člen NAND v multiplexore

---

### Demultiplexor

- je prepínací k.l.o. kt. jeden vstup prepína na niekoľko výstupov podľa riadiacich signálov z dekódera
- je to obrátený multiplexor

---

### Binárny komparátor

- je to k.l.o. kt. porovnáva 2 paralelné binárne slová a generuje hodnotu 1 ak sú obidve slová rovné
- ak je prvé binárne slovo `A₃, A₂, A₁, A₀` a druhé binárne slovo `B₃, B₂, B₁, B₀`, musí platiť pre ich rovnosť: `A₃ = B₃; A₂ = B₂; A₁ = B₁; A₀ = B₀`
- komparátor využíva vlastnosti členov XOR kt. generuje 0 pri zhode vstupov

---

## Sekvenčné logické obvody — S.l.o.

- majú tú vlastnosť, že ich výstupné premenné sú určené nie len kombináciou vstupných premenných v danom okamihu ale aj minulými hodnotami niektorých premenných
- z toho vyplýva, že si s.l.o. musí **pamätať** hodnoty z predchádzajúceho stavu, čo znamená, že musí obsahovať **pamäťové členy**
- základom s.l.o. sú prelápacie obvody z kt. sa ďalej konštruujú čítače, registre a pamäťové obvody

---

## Klopný obvod typu RS asynchrónny

- realizovaný z 2 obvodov NAND al. NOR
- 1. rozoberieme si vstup keď `R = 1` a `S = 0`
- z pravdivostnej tabuľky členov NOR vieme, že má na výstupe log. 1 len v prípade oboch vstupov v log. 0
  - táto podmienka je splnená u horného člena NOR pretože vstup `R = 1` a preto výstup `Q = 0` → dióda nesvieti
  - táto log. 0 sa dostane spätnou väzbou na vstup dolného člena NOR a ten vytvorí na svojom výstupe `Q̄ = 1`
  - spätná väzba na horný člen NOR jeho výstup nezmení
  - tým je jednoznačne daný výstup klopného obvodu `Q = 0`, `Q̄ = 1`
- tomuto stavu hovoríme **reset** — vynulovanie obvodu — hlavný výstup `Q = 0`

### Krok 2 — keď zmeníme R=0 (vstup horného člena NOR na 0)

- vplyvom spätnej väzby z dolného člena zostane jeho 2. vstup 1 a jeho výstup bude, preto `Q = 0`
  - výstup dolného člena bude, zo vstupov 0 a 0 ⇒ `Q̄ = 1`
  - oba výstupy sa po vynulovaní vstupu zo stavu reset nezmenili

### Krok 3 — opačná situácia R=0; S=1 oproti stavu reset

- výstup bude opačný → `Q = 1; Q̄ = 0`
- tomuto stavu hovoríme **set** nastavenie — obvod má hlavný výstup `Q = 1`

### Krok 4 — pri zmene S=1 na S=0

- sú opäť výstupy `Q = 1; Q̄ = 0` — nemenia sa
- teraz sú tieto výstupy pre `S = 0` a `R = 0` práve opačné oproti vynulovaniu obvodu zo stavu reset

---

### Prechod z oboch stavov reset a set do stavu vynulovania vstupov

- vyjadruje pravdivostná tabuľka:

| R | S | Q | Q̄ |
|---|---|---|---|
| 1 | 0 | 0 | 1 | ← reset |
| 0 | 1 | 1 | 0 | ← set |
| 0 | 0 | 1 | 0 | |
|   |   | 0 | 1 | |

*(zakázaný stav naznačený šedou)*

### Komplikovaná situácia — R=1 zároveň S=1 (set a reset naraz)

- v tom prípade podľa pravdivostnej tabuľky NOR obidva výstupy Q aj Q̄ sú v log. 0
- to by tak nevadilo, ale pri zmene R al. S na 1 al. 0 nastane labilná situácia kedy všetky výstupy sú teraz v log. 0 a oba členy NOR sa snažia vytvoriť na výstupe log. 1, ale kde ju vytvoria? nie je to jednoznačne dané a obvod prejde náhodne do ľubovoľného stavu

**Pravdivostná tabuľka RS klopného obvodu:**

| R | S | Q  | Q̄  |
|---|---|----|-----|
| 0 | 0 | Q* | Q̄* | ← pamäť |
| 0 | 1 | 1  | 0   | ← set |
| 1 | 0 | 0  | 1   | ← reset |
| 1 | 1 | X  | X   | ← **zakázaný stav** |

*(kde Q* = predchádzajúca hodnota Q)*

---

## Klopný obvod RS — synchrónny

- ak doplníme klopný obvod RS asynchrónny ďalšími 2 členmi NAND (pred) dostaneme obvod s rovnakými vlastnosťami ale jeho výstup bude možné meniť len v priebehu synchronizačného hodinového impulzu — je to **CLOCK**
- ak chýba hodinový impulz `C = 0`, je obvod pomocou prvých členov NAND zablokovaný, pretože ich výstup je trvalo = 1 a akákoľvek zmena R al. S nemôže zmeniť výstup Q
- obvod sa otvorí až s príchodom hodinového impulzu `C = 1` a jedine v dobe jeho trvania je možné pomocou vstupov R a S meniť výstup Q
- výstupné členy NAND tu pôsobia ako invertory a preto bude zakázaný stav opačný — to znamená `S = R = 1`
- z rovnakého dôvodu je nutné prechádzať vstupy R a S aby platilo pre SET a RESET odpovedajúce nastavenie výstupného klopného obvodu

---

## Klopný obvod D

- odstraňuje zakázaný stav prepojením vstupu klopného obvodu RS invertrom
- obvod je riadený, synchronizovaný — hodinovým vstupom
- klopný obvod prelípa len v priebehu hodinového impulzu, inak je zavretý
- invertor zaistí, že vstupy do pôvodného klopného obvodu RS môžu byť len rozdielne

*(diagram: D KO — vstup D, C → [NAND] → [NAND] → Q, Q̄)*

### Klopný obvod Jack Knilby — JK

- zdokonalený klopný obvod RS ktorý nemá zakázaný stav vstupných premenných
- to je docielené pridaním súčinových členov AND do vstupov S a R a zavedením spätnej väzby z výstupov klopného obvodu na vstup troch členov AND
- zabránenie vzniku zakázaného stavu je docielené takým spôsobom: máme zaistením 1 nulového spätnoväzobného vstupu (ak je Q=0) pre dolný súčinový člen AND alebo 2 nulového spätnoväzobného vstupu (ak je Q̄=0) pre horný súčinový člen AND — prehlásiteľný obvod

*(diagram: JK KO — vstupy J, C, K; výstupy Q, Q̄)*

**Príklad stavu:** `D=1; C=0; L=1` →

*(diagram v zošite: cez NAND obvody)*

---

## Klopný obvod typu T

- klopný obvod tohto typu získame prepojením obidvoch vstupov J a K klopného obvodu JK — vznikne jediný vstup označený T
- pri tomto zapojení ak je trvalo `T = 1`, pracuje obvod ticho ako keď J a K sú = 1 v predchádzajúcom obvode
- ak je `T = 1`, stav na výstupe sa mení na opačný pri každom príchode synchronizačného hodinového impulzu C
- ak je `T = 0`, obvod zostáva v pôvodnom stave

*(diagram: T KO — vstup T, C; výstupy Q, Q̄)*
