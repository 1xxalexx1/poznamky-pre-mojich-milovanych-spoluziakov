# Logické obvody — Tahák na skúšku

---

## 1. Logické obvody — základy

**Logický obvod** je hardvérový systém, ktorý pomocou logických signálov realizuje logické funkcie.

**Logická funkcia F** priradí každej kombinácii hodnôt nezávislých premenných (vstupy) jednu hodnotu závislej premennej (výstup).
- Zapisujeme: `y = F(x)`
- Výrok s hodnotou 1 = pravdivý (true)
- Výrok s hodnotou 0 = nepravdivý (false)

**Pravdivostná tabuľka** — tabuľka všetkých možných kombinácií vstupov a im zodpovedajúcich výstupov.
- Počet stĺpcov = počet premenných (vstupov)
- Počet riadkov = 2ⁿ (kde n = počet vstupných premenných)

**Logický výraz** — opisuje logické vzťahy medzi premennými pomocou logických operátorov (AND, OR, NOT…).

---

## 2. Normálové tvary logickej funkcie

### Štandardný súčtový tvar (SNF-1 / DNF)
- Zoberieme len tie riadky pravdivostnej tabuľky, kde **y = 1**
- V každom takom riadku napíšeme súčin (AND) všetkých premenných:
  - premennú s hodnotou 1 píšeme priamo (napr. A)
  - premennú s hodnotou 0 negujeme (napr. Ā)
- Všetky tieto súčiny sčítame (OR)

**Príklad:** `y = (A·B·C) + (A·B̄·C) + (Ā·B·C)`

### Štandardný súčinový tvar (SNF-0 / KNF)
- Zoberieme len tie riadky, kde **y = 0**
- V každom takom riadku napíšeme súčet (OR) všetkých premenných:
  - premennú s hodnotou 0 píšeme priamo
  - premennú s hodnotou 1 negujeme
- Všetky tieto súčty vynásobíme (AND)

**Príklad:** `y = (A+B+C) · (A+B̄+C)`

---

## 3. Základné logické členy (hradlá)

### NOT — negácia (invertor)
- Funkcia: `y = Ā`
- Výstup je vždy opak vstupu
- IC: **MH7404**

| A | y |
|---|---|
| 0 | 1 |
| 1 | 0 |

---

### AND — konjunkcia (logický súčin)
- Funkcia: `y = A · B`
- Výstup je 1 **len ak sú oba vstupy 1**
- IC: **MH7408**

| A | B | y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

---

### OR — disjunkcia (logický súčet)
- Funkcia: `y = A + B`
- Výstup je 1 ak **aspoň jeden vstup je 1**
- IC: **MH7432**

| A | B | y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

---

### NAND — negovaný logický súčin
- Funkcia: `y = Ā·B` (negácia AND)
- Výstup je 0 **len ak sú oba vstupy 1**, inak 1
- IC: **MH7400, MH7403, MH7410, MH7420, MH7430**
  - (2-vstupový, 3-vstupový, 4-vstupový, 8-vstupový varianty)

| A | B | y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

---

### NOR — negovaný logický súčet
- Funkcia: `y = Ā+B` (negácia OR)
- Výstup je 1 **len ak sú oba vstupy 0**
- IC: **MH7402**

| A | B | y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

---

### XOR — exkluzívny logický súčet (EX-OR)
- Funkcia: `y = A ⊕ B`
- Výstup je 1 ak sú vstupy **rozdielne**
- IC: **MH7486**

| A | B | y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

---

### XNOR — exkluzívny negovaný logický súčet (EX-NOR)
- Funkcia: `y = A⊕B` (negácia XOR) — koncovka **66**
- Výstup je 1 ak sú vstupy **rovnaké**

| A | B | y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

---

> **Logická 0** = 0V, GND, zem, nízka, LOW
> **Logická 1** = 5V, HIGH

---

## 4. Kombinačné logické obvody (KLO)

KLO sú obvody kde výstupná hodnota závisí **len od aktuálnej kombinácie vstupov** (nemajú pamäť).

---

### Polovičná sčítačka (1/2 ADD)
- Sčítava 2 jednobitové čísla
- **Vstupy:** A, B
- **Výstupy:** S (súčet), P (prenos do vyššieho rádu)
- **Nevýhoda:** nedokáže spracovať prenos z nižšieho rádu
- Realizácia: hradlo **XOR** (pre S) + hradlo **AND** (pre P)
- Funkcie: `S = A ⊕ B`, `P = A · B`

---

### Úplná sčítačka (Full ADD)
- Sčítava 2 bity + **prenos z nižšieho rádu (P₁)**
- **Vstupy:** A, B, P₁
- **Výstupy:** S (súčet), P₂ (prenos)
- Realizácia: 2× XOR + 2× AND + 1× OR (alebo iné ekvivalentné zapojenie)
- Vznikne spojením dvoch polovičných sčítačiek

---

### Generátor parity (G.P.)
- Identifikuje vznik chyby v binárnom slove
- Prehliada binárne slovo a generuje **paritný bit**
- Ak je počet jedničiek v slove **párny** → paritný bit = **0**
- Ak je počet jedničiek v slove **nepárny** → paritný bit = **1**

---

### Kóder
- Prevodník — prevádza čísla z jedného kódu do iného
- Je to KLO: z 1 alebo viacerých vstupov zodpovedajúcich 10-sústave generuje výstup v 2-sústave
- Zapojenie pomocou NAND členov (privedenie log. 0 na aspoň 1 vstup → na výstupe log. 1)

---

### Dekóder
- **Opak kódera**
- Zaistí prítomnosť určitého binárneho čísla alebo zistí stav binárneho čísla
- Každá kombinácia vstupov aktivuje **práve jeden výstup**
- Pre 2 vstupné premenné (A, B) → 4 výstupy (0–3):
  - 0: `Ā·B̄`, 1: `Ā·B`, 2: `A·B̄`, 3: `A·B`

---

### Multiplexor (MUX)
- Prepínacie KLO: z **niekoľkých vstupov** vyberá 1 výstup podľa riadiacich signálov
- Použitie: prepínanie signálov, prevod paralelných dát na sériové, generátor sériového binárneho slova, realizácia booleovských funkcií
- Riadiace signály môžu byť výstupy z dekódera

### Demultiplexor (DEMUX)
- Opak multiplexora
- 1 vstup prepína na **niekoľko výstupov** podľa riadiaceho signálu
- Je to obrátený multiplexor

---

### Binárny komparátor
- Porovnáva 2 paralelné binárne slová
- Generuje 1 ak sú obe slová **rovnaké**
- Využíva vlastnosť hradla **XNOR** (generuje 0 pri zhode vstupov → negáciou dostaneme 1 pri zhode)

---

## 5. Karnaughova mapa (KM)

Karnaughova mapa je grafická metóda **minimalizácie** logickej funkcie.

### Pravidlá:
- Pre **2 premenné** (A, B): mapa 2×2 = 4 políčka
- Pre **3 premenné** (A, B, C): mapa 2×4 = 8 políčok
- Pre **4 premenné** (A, B, C, D): mapa 4×4 = 16 políčok
- Stĺpce/riadky sú zoradené v **Grayovom kóde** (susedné políčka sa líšia len v 1 bite): `00, 01, 11, 10`

### Ako vyplniť KM:
- Do políčok dávame hodnoty **y** z pravdivostnej tabuľky
- Políčko kde premenná platí (=1) patrí do stĺpca/riadku **bez čiarky** (napr. A)
- Políčko kde premenná neplatí (=0) patrí do stĺpca/riadku **s čiarkou** (napr. Ā)
- Kde je **1 → disjunktná A** (ide do skupín pre SNF-1)
- Kde je **0 → konjunktná A** (ide do skupín pre SNF-0)
- Kde premenná v rámci skupiny **mení hodnotu → vynecháme ju** z výsledného člena

### Postup minimalizácie:
1. Vyplníme KM hodnotami z pravdivostnej tabuľky
2. Skupujeme (ohraničujeme) **jednotky** do skupín veľkosti 1, 2, 4, 8, 16... (mocniny 2)
3. Skupiny musia byť čo najväčšie a čo najmenej početné
4. Skupiny sa môžu prekrývať
5. Každá skupina dáva 1 súčinový člen výslednej funkcie — vynecháme premenné, ktoré sa v rámci skupiny menia
6. Výsledok = súčet všetkých skupinových členov (SNF-1)

### Konkrétny príklad — F(A,B,C), disjunktná D(3,4,6,8) — teda y=1 pre minitermy 3,4,6,8:

Pravdivostná tabuľka (y=1 pre riadky 3,4,6,8 — číslujeme od 0):

| # | A | B | C | y |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 0 |
| 2 | 0 | 1 | 0 | 0 |
| 3 | 0 | 1 | 1 | 1 |
| 4 | 1 | 0 | 0 | 1 |
| 5 | 1 | 0 | 1 | 0 |
| 6 | 1 | 1 | 0 | 1 |
| 7 | 1 | 1 | 1 | 0 |

Karnaughova mapa (riadky = A, stĺpce = BC v Grayovom kóde):

```
        B̄C̄  B̄C  BC  BC̄
   Ā  |  0 |  0 |  1 |  0 |
   A  |  1 |  0 |  0 |  1 |
```

Skupiny jednotiek:
- Políčko (Ā,BC) = minterm 3: `Ā·B·C` — tvorí pár s...
- Políčka (A,B̄C̄) a (A,BC̄) = minterm 4 a 6 → BC̄ sa mení, A=1, C=0 → člen: `A·C̄`  — **toto je skupina 2**
- Políčka (Ā,BC) a (A,BC̄) → B je spoločné, ostatné sa menia → skúšame ďalej...

**Výsledok po minimalizácii:** `F = (B·Ā) + (B·C) + (A·C̄)`

> Každý pár susedných jednotiek (vrátane "wrap-around" cez okraje mapy) = 1 premenná sa vynechá.
> Každá štvorica = 2 premenné sa vynechajú. Čím väčšia skupina, tým jednoduchší člen.

---

## 6. Sekvenčné logické obvody (SLO)

SLO majú výstupy závislé **nielen od aktuálnych vstupov, ale aj od predchádzajúceho stavu** (majú pamäť).

→ Musia si pamätať hodnoty → obsahujú **pamäťové prvky**

Základom SLO sú **klopné obvody (flip-flopy)**, z ktorých sa ďalej konštruujú čítače, registre a pamäťové obvody.

---

## 7. Klopné obvody

### RS klopný obvod — asynchrónny (NOR / NAND verzia)
- Realizovaný z 2 hradiel **NOR** alebo **NAND**
- **Vstupy:** R (Reset), S (Set)
- **Výstupy:** Q, Q̄ (navzájom negované)

**NOR verzia — aktívna úroveň vstupu je log. 1:**

| R | S | Q | Q̄ | Stav |
|---|---|---|---|------|
| 0 | 0 | Q₀ | Q̄₀ | Pamäť (nezmenený stav) |
| 1 | 0 | 0 | 1 | Reset (Q=0) |
| 0 | 1 | 1 | 0 | Set (Q=1) |
| 1 | 1 | X | X | **Zakázaný stav!** |

**NAND verzia — aktívna úroveň vstupu je log. 0:**

| R | S | Q | Q̄ | Stav |
|---|---|---|---|------|
| 1 | 1 | Q₀ | Q̄₀ | Pamäť (nezmenený stav) |
| 0 | 1 | 0 | 1 | Reset (Q=0) |
| 1 | 0 | 1 | 0 | Set (Q=1) |
| 0 | 0 | X | X | **Zakázaný stav!** |

> Rozdiel: pri NAND verzii je obvod v pokoji pri vstupoch R=S=**1** (nie 0), a zakázaný stav nastane pri R=S=**0**.

- **Set:** S=1, R=0 → Q=1 (nastavenie)
- **Reset:** R=1, S=0 → Q=0 (vynulovanie)
- **Zakázaný stav (NOR):** R=1 a S=1 súčasne → Q aj Q̄ oba 0, neurčitý stav

---

### RS klopný obvod — synchrónny
- RS asynchrónny + 2 ďalšie NAND hradlá na vstupe
- Výstup možno meniť **len počas hodinového impulzu C=1** (CLOCK)
- Pri C=0 je obvod zablokovaný (výstupy sa nemenia)
- Zakázaný stav je stále S=R=1

---

### D klopný obvod
- Odstráni zakázaný stav prepojením vstupov RS cez invertor
- Vstupy D a C (hodinový vstup)
- Invertor zaistí, že S a R sú **vždy rozdielne** → zakázaný stav nemôže nastať
- Klopný obvod prehláspi len **počas hodinového impulzu**, inak je zavretý

---

### JK klopný obvod
- Zdokonalený RS klopný obvod **bez zakázaného stavu**
- Pridanie AND členov na vstupy S a R + spätná väzba z výstupu
- Keď J=1, K=1 → výstup sa **prehodí** (toggle)

| J | K | Q (ďalší stav) |
|---|---|----------------|
| 0 | 0 | Q₀ (pamäť) |
| 0 | 1 | 0 (reset) |
| 1 | 0 | 1 (set) |
| 1 | 1 | Q̄₀ (prehodenie) |

---

### T klopný obvod
- Vznikne prepojením oboch vstupov J a K JK klopného obvodu — vznikne jediný vstup **T**
- Pri T=1 sa stav výstupu **mení na opačný** pri každom hodinovom impulze C
- Pri T=0 obvod zostáva v pôvodnom stave

---

## 8. Rýchly prehľad IC čísel

| Obvod | IC |
|-------|----|
| NOT (invertor) | MH7404 |
| AND | MH7408 |
| OR | MH7432 |
| NAND (2-vstup) | MH7400 |
| NAND (3-vstup) | MH7410 |
| NAND (4-vstup) | MH7420 |
| NAND (8-vstup) | MH7430 |
| NOR | MH7402 |
| XOR | MH7486 |

---