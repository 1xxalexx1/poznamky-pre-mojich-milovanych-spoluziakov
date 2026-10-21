# Protokoly — ELE-IST 2. ročník

---

## Laboratórne cvičenie č. 14

**Názov cvičenia:** Overenie činnosti špeciálnych diód

### Úlohy

1. Vyhľadajte v katalógu obmedzujúce veličiny predložených diód. *(Iz = 35 mA)*
2. Zapojte prístroje a súčiastky podľa daných schém.
3. Pri rôznych napätiach U_R zistite veľkosť prúdu I_R a nakreslite namerané charakteristiky Zenerovej diódy v závernom smere I_R = f(U_R). Vymedzte na nich dovolenú pracovnú oblasť určenú na stabilizáciu napätia.
4. Zistite kapacitu varikapu pomocou mostíka RLCG pri rôznych hodnotách záverného napätia U_R. Nakreslite namerané charakteristiky C = f(U_R) a na nich určte zmenu kapacity ΔC vplyvom zmeny napätia ΔU minimálne v troch rôznych pracovných bodoch.
5. Nakreslite schému a tabuľku pre meranie VACH LED diódy a overte ju v priepustnom smere, zostroj VACH, vyznačte prahové napätie.
6. Namerané údaje vyhodnoťte a porovnajte s katalógovými.

### Schémy zapojenia

- schéma zap. pre Zenerovu diódu *(voltmeter + mA merač + dióda v závernom smere)*
- schéma zap. pre varikap *(voltmeter + RLCG mostík MER)*

### Tabuľka nameraných hodnôt

**Zenerova dióda:**

| Typ Diódy | U_R (V) | I_R (mA) |
|-----------|---------|---------|
| ZENEROVA  | 5,4     | 0,5     |
| ZENEROVA  | 11,6    | 1       |
| ZENEROVA  | 12      | 10      |
| ZENEROVA  | 12,27   | 20      |
| ZENEROVA  | 12,8    | 40      |
| ZENEROVA  | 13,8    | 80      |

**LED / VARIKAP:**

| Typ Diódy | U_R (V) | C(pF) I_F (mA) |
|-----------|---------|----------------|
| LED VARIKAP | 1,71  | 0,5            |
| LED VARIKAP | 1,74  | 1              |
| LED VARIKAP | 1,78  | 2              |
| LED VARIKAP | 1,84  | 5              |
| LED VARIKAP | 1,87  | 7              |
| LED VARIKAP | 1,91  | 10             |

### Grafy

- **Zenerova dióda:** U_R (V) na osi y, I_R (mA) na osi x — krivka v závernom smere, stabilizačná oblasť ~12–13 V
- **LED dióda:** U_R (V) na osi y, I_F (mA) na osi x — priepustná charakteristika, prah ~1,7 V

### Záver

Pri meraní Zenerovej diódy v závernom smere sme zistili, že so zvyšujúcim sa záverným prúdom sa napätie mení len nepatrne a pohybuje sa približne v rozsahu 12 až 13 V. Táto oblasť zodpovredá stabilizačnej oblasti Zenerovej diódy a je v súlade s katalógovými údajmi.

Pri meraní LED diódy v priepustnom smere sme zistili, že dióda začína vodivo viesť pri napätí 1,7 V a pri prúde 10 mA dosahuje priepustné napätie približne 1,9 V. Namerané hodnoty zodpovedajú katalógovým charakteristikám LED diódy.

Cieľ merania bol splnený a potvrdzujú teoretické predpoklady.

---

## Laboratórne cvičenie č. 15

**Názov cvičenia:** Nelineárne súčiastky elektronických obvodov – bipolárne tranzistory. Grafické zostrojovanie prevodových VACH bipolárneho tranzistora a výpočet „h"-parametrov.

### Úlohy

1. Oboznámte sa so základnými katalógovými hodnotami daného bipolárneho tranzistora KF 508.
2. Z predložených výstupných VACH bipolárneho tranzistora KF 508 graficky zostrojte prevodové VACH pre U_ce = 10 V a U_ce = 20 V.
3. Daný pracovný bod P so súradnicami U_ce = 10 V, I_c = 20 mA, I_b = 120 μA, preneste do II. a III. kvadrantu.
4. Navrhnite kolektorový odpor R_c tak, aby zaťažovacia priamka išla cez daný pracovný bod P, ak je dané napájacie napätie U_cc = 20 V.
5. V okolí pracovného bodu vyznačte pracovnú oblasť ΔU_ce = 12 V, tomu zodpovedajúce ΔI_c a preneste do II. a III. kvadrantu.
6. Vypočítajte parametre:
   - h22 = ΔI_c / ΔU_ce pri podmienke I_b = 120 μA
   - h21 = ΔI_c / ΔI_b pri podmienke U_ce = 10 V
   - h11 = ΔU_be / ΔI_b pri podmienke U_ce = 10 V
7. Vypočítané parametre porovnajte s katalógovými.

### Výstupné VACH bipolárneho tranzistora KF508

*(graf s krivkami I_c [mA] v závislosti od U_CE [V] pre rôzne I_B [μA], hodnoty I_B od 20 do 220 μA)*

### Výpočty

$$\Delta I_c = \frac{33\,\text{mm}}{14\,\text{mm}} \cdot 10 = 23{,}6\,\text{mA}$$

$$\Delta I_B = \frac{27\,\text{mm}}{17\,\text{mm}} \cdot 100 = 159\,\mu\text{A}$$

$$\Delta U_{BE} = \frac{5}{7} \cdot 100 = 71\,\text{mV}$$

$$\Delta U_{ce} = 12\,\text{V}$$

$$h_{22} = \frac{23{,}6\,\text{mA}}{12\,\text{V}} = \frac{23{,}6\,\text{mA}}{12\,000\,\text{mV}} = 1{,}96\,\text{mS}$$

$$h_{21} = \frac{23{,}6\,\text{mA}}{159\,\mu\text{A}} = \frac{23600}{159} = 148{,}4$$

$$h_{11} = \frac{71\,\text{mV}}{159\,\mu\text{A}} = \frac{71000}{159} = 446\,\Omega$$

$$R_C = \frac{U_{cc}}{I_{c\max}} = \frac{20}{40\,\text{mA}} = 0{,}5 \cdot 10^3 = 500\,\Omega$$

### Záver

*(záver nie je napísaný — chýba)*

---

## Laboratórne cvičenie č. 16

**Názov cvičenia:** Nelineárne súčiastky elektronických obvodov – bipolárne tranzistory. Overenie vlastností bipolárnych tranzistorov v zapojení so spoločným emitorom (BT - SE).

### Úlohy

1. Vyhľadajte v katalógu obmedzujúce veličiny predložených BT (I_cmax, U_cemax, P_cdov.)
2. Zapojte meracie prístroje podľa predloženej schémy.
3. Zmerajte 2 vstupné a 3 výstupné VACH a zostroj ich.
4. Pre zvolené konštantné výstupné napätie (U_ce = k) graficky zostrojte prevodovú charakteristiku.
5. Pre zvolený pracovný bod a pracovnú oblasť vypočítajte parametre h11, h21, h22. Pripravte si vzťahy na výpočet parametrov!
6. Vyhodnotenie merania.

### Funkčné vzťahy pre jednotlivé VACH

- VSTUPNÉ VACH: U_be = f(I_b) / U_ce = k
- VÝSTUPNÉ VACH: I_c = f(U_ce) / I_b = k
- PREVODOVÉ VACH: I_c = f(I_b) / U_ce = k

### Schéma zapojenia

*(zapojenie: U1, R1, R2, meradlá A a V na vstupe, tranzistor K v strede, meradlá A a V na výstupe, R3, U2)*

### Tabuľky nameraných hodnôt

**Výstupné VACH** (I_b = konštantné):

| U_ce (V) | I_c (A) Ib= | I_c (A) Ib= | I_c (A) Ib= |
|---------|------------|------------|------------|
| 1       | 13         | 22         | 25,4       |
| 2       | 15,15      | 22,4       | 27,1       |
| 3       | 15,3       | 22,7       | 27,3       |
| 4       | 15,32      | 23,4       | 28,6       |
| 5       | 15,6       | 24         | 29,3       |
| 10      | 17         | 26,2       | 31,5       |
| 15      | 18,4       | 28,7       | 34,3       |
| 20      | 19,5       | 34,5       | 38,7       |
| 25      | 21,7       | 37,5       | 43,2       |
| 30      | 23         | 41,2       | 48,1       |

**Vstupné VACH:**

| I_b (A) | U_be (V) Uce= (V) | U_be (V) Uce= (V) |
|---------|-------------------|-------------------|
| *(prázdna tabuľka)* | | |

### Záver

*(záver nie je napísaný — chýba)*

---

## Laboratórne cvičenie č. 17

**Názov cvičenia:** Nelineárne súčiastky elektronických obvodov – unipolárne tranzistory. Overenie vlastností unipolárnych tranzistorov v zapojení so spoločným emitorom (UT - SE).

### Úlohy

1. Vyhľadajte v katalógu obmedzujúce veličiny predložených UT (I_cmax, U_cemax, P_cdov.) *(KF 520)*
2. Zapojte meracie prístroje podľa predloženej schémy.
3. Zmerajte výstupné VACH UT s vodivým kanálom v obohatenom aj ochudobnenom režime a zostroj ich. *(„10V")*
4. Pre zvolené konštantné výstupné napätie (U_ce = k) graficky zostrojte prevodovú charakteristiku (alebo ju odmerajte a potom zostroj).
5. Pre zvolený pracovný bod a pracovnú oblasť vypočítajte parametre y21, y22. Pripravte si vzťahy na výpočet parametrov! *(bez parametrov)*
6. Vyhodnotenie merania.

### Funkčné vzťahy pre jednotlivé VACH

- VÝSTUPNÉ VACH: I_c = f(U_ce) / U_ge = k
- PREVODOVÉ VACH: I_c = f(U_ge) / U_ce = k

### Schéma zapojenia

*(tranzistor KF 520, R1, voltmeter V na vstupe, ampérmeter A a voltmeter V na výstupe, R2, R3)*

### Tabuľka nameraných hodnôt — výstupné VACH

| U_ce (V) | I_c (A)mA U_ge=0V | I_c (A)mA U_ge=2V | I_c (A) U_ge=4V | I_c (A) U_ge=-2V | I_c (A) U_ge=-4V |
|---------|-------------------|-------------------|-----------------|-----------------|-----------------|
| 1       | 0,9               | 1                 | 1,17            | 0,7             | 0,56            |
| 2       | 1,5               | 1,76              | 2               | 1,2             | 0,83            |
| 3       | 1,9               | 2,3               | 2,7             | 1,5             | 1,07            |
| 4       | 2,2               | 2,7               | 3,3             | 1,66            | 1,14            |
| 5       | 2,38              | 3                 | 3,67            | 1,75            | 1,17            |
| 6       | 2,5               | 3,2               | 4               | 1,76            | 1,18            |
| 8       | 2,55              | 3,36              | 4,3             | 1,8             | 1,2             |
| 10      | 2,58              | 3,42              | 4,45            | 1,83            | 1,22            |
| 16      | 2,63              | 3,5               | 4,57            | 1,86            | 1,24            |
| 20      | 2,67              | 3,56              | 4,6             | 1,9             | 1,3             |

### Graf — výstupné VACH KF520

*(graf: I_c [mA] vs U_CE [V] pre 5 hodnôt U_GE: +4V, +2V, 0V, -2V, -4V; pracovný bod P vyznačený)*

### Záver

V cvičení sme merali VACH charakteristiky unipolárneho tranzistora KF 520 pri rôznych hodnotách V_GE. Namerané hodnoty potvrdili, že pri kladnom U_GE (obohatený stav) prúd I_C narastá, a pri zápornom U_GE (ochudobnený stav) klesá. Charakteristiky majú typický priebeh — strmý nárast I_C v odporovej oblasti a stabilizáciu v aktívnej oblasti.

Správanie tranzistora potvrdzuje teoretické poznatky o unipolárnych tranzistoroch.

---

## Laboratórne cvičenie č. 18–19

**Názov cvičenia:** Optoelektronické súčiastky. Overenie vlastností fotoprvkov.

### Úlohy

1. Vyhľadajte v katalógu obmedzujúce veličiny predložených fotoprvkov.
2. Zapojte meracie prístroje podľa predložených schém.
3. Overte ako sa mení odpor fotorezistora v závislosti od zmeny intenzity osvetlenia, ktorú určíme pomocou luxmetra.
4. Pri fototranzistorze odmerajte výstupné VACH pri dvoch rôznych intenzitách osvetlenia.
5. Pri fotodióde určte vplyv zmeny intenzity osvetlenia na veľkosť jej anódového prúdu v odporovom režime (VACH v závernom smere).
6. V hradlovom režime fotodiódy určte ako sa zmení napätie naprázdno U_o a prúd nakrátko I_k, keď sa zmení intenzita osvetlenia.
7. Zistené údaje vyneste graficky. *(I_cmax = 20 mA, U_cmax = 30 V)*
8. Vyhodnotenie merania.

### Schémy zapojenia

*(a) fotorezistor — Ω merač*
*(b) fototranzistor — A merač + V merač*
*(c) fotodióda — odporový režim — A merač + V merač*
*(d) fotodióda — hradlový režim — A merač / V merač)*

### Tabuľky nameraných hodnôt

**a) Fotoodpor:**

| E (lx) | R (Ω)  |
|--------|--------|
| 100    | 1480   |
| 200    | 1420   |
| 300    | 950    |
| 400    | 800    |
| 500    | 710    |
| 600    | 640    |
| 700    | 588    |
| 800    | 550    |
| 900    | 515    |
| 1000   | 488    |

**b) Fototranzistor:**

|         | E = 300 (lx) | E = 600 (lx) |
|---------|-------------|-------------|
| U_CE (V) | I_c (mA)    | I_c (mA)    |
| 2        | 2,6         | 4,3         |
| 4        | 2,7         | 4,5         |
| 6        | 2,9         | 4,7         |
| 8        | 2,8         | 4,9         |
| 10       | 2,8         | 5,2         |
| 12       | 3,2         | 5,4         |
| 14       | 3,34        | 5,7         |
| 16       | 3,4         | 6           |
| 18       | 3,4         | 6,3         |
| 20       | 3,46        | 6,7         |

**c) Fotodióda — odporový režim:**

|          | E = 300 (lx) | E = 600 (lx) |
|----------|-------------|-------------|
| U_KA (V) | I_A (mA)    | I_A (mA)    |
| 2         | 0,1         | 0,2         |
| 4         | 0,1         | 0,2         |
| 6         | 0,1         | 0,2         |
| 8         | 0,1         | 0,2         |
| 10        | 0,1         | 0,2         |
| 12        | 0,1         | 0,2         |
| 14        | 0,1         | 0,2         |
| 16        | 0,1         | 0,2         |
| 18        | 0,1         | 0,2         |
| 20        | 0,1         | 0,2         |

**d) Fotodióda — hradlový režim:**

| E (lx) | U_o (mV) | I_k (μA) |
|--------|---------|---------|
| 100    | 0,355   | 57      |
| 200    | 0,374   | 87      |
| 300    | 0,384   | 111     |
| 400    | 0,391   | 133     |
| 500    | 0,3956  | 153     |
| 600    | 0,400   | 170     |
| 700    | 0,4063  | 183     |
| 800    | 0,4086  | 204     |
| 900    | 0,4093  | 218     |
| 1000   | 0,4111  | 235     |

### Grafy

*(Fotoodpor: E (lx) vs R (Ω) — klesajúca nelineárna krivka)*
*(Fototranzistor: I_c (mA) vs U_CE (V) pre E=300lx a E=600lx — rastúce krivky)*
*(Fotodióda odporový: I (mA) vs U_KA (V) — vodorovné rovné čiary pre E=300 a E=600)*
*(Fotodióda hradlový Uo: E (lx) vs U_o (mV) — rastúca krivka)*
*(Fotodióda hradlový Ik: E (lx) vs I_k (μA) — rastúca krivka)*

### Záver

Meraním sme overili vlastnosti troch optoelektronických súčiastok.

Odpor fotorezistora klesal so zvyšujúcou sa intenzitou osvetlenia – z 1800 Ω pri 100 lx na 488 Ω pri 1000 lx. Grafom je klesajúca nelineárna krivka.

Výstupné VACH fototranzistora potvrdili, že vyššia intenzita osvetlenia spôsobuje väčší kolektorový prúd. Obe charakteristiky mierne stúpajú s rastom U_CE.

Fotodióda v odporovom režime vykazovala konštantný prúd nezávislý od záverného napätia.

V hradlovom režime napätie rastie nelineárne a prúd rastie približne lineárne s intenzitou osvetlenia.

Všetky namerané závislosti zodpovedajú teoretickým predpokladom.

---

## Laboratórne cvičenie č. 20–21

**Názov cvičenia:** Oboznámenie s unitestami. Základy číslicovej techniky – minimalizácia log. funkcií pomocou BA.

### Úlohy

1. Oboznámte sa s predloženými učebnými pomôckami – unitestami, s druhom používaného školského stabilizovaného zdroja, s potrebnými obvodmi a katalógmi.
2. Pri unitestoch treba zohľadňovať veľkosť napájacieho napätia, umiestňovanie obvodov, realizáciu kontroly zapojení, úroveň výstupných signálov overovať pomocou LED diód. Potrebné informácie si podľa inštrukcií vyučujúceho a pomocou konštrukčného katalógu zapíšte do cvičení.
3. Pre obvody TTL vypíšte z konštrukčného katalógu hodnoty:
   - napájacieho napätia
   - úrovne vstupných a výstupných signálov (log.1 a log.0)
   - označenie vývodov puzdra DIL
4. Zopakujte si zákony BA.
5. Na predložených príkladoch precvičte minimalizáciu log. funkcií pomocou zákonov BA.

### Úloha 3: Hodnoty z konštrukčného katalógu — obvod MH7400 (NAND)

| Parameter                        | Hodnota          |
|----------------------------------|------------------|
| Napájacie napätie VCC            | 4,75 V – 5,25 V  |
| Min. vstupné napätie log. 1 (U_IH min) | 2,0 V      |
| Max. vstupné napätie log. 0 (U_IL max) | 0,8 V      |
| Min. výstupné napätie log. 1 (U_OH min) | 2,4 V     |
| Max. výstupné napätie log. 0 (U_OL max) | 0,4 V     |
| Max. vstupný prúd log. 1 (I_IH max) | 40 μA          |
| Max. vstupný prúd log. 0 (I_IL max) | −1,6 mA        |

### Označenie vývodov puzdra DIL (MH7400):

| Pin | Signál                  | Pin | Signál                  |
|-----|-------------------------|-----|-------------------------|
| 1   | 1A – vstup A, hradlo 1  | 14  | VCC – napájacie napätie |
| 2   | 1B – vstup B, hradlo 1  | 13  | 4B – vstup B, hradlo 4  |
| 3   | 1Y – výstup, hradlo 1   | 12  | 4A – vstup A, hradlo 4  |
| 4   | 2A – vstup A, hradlo 2  | 11  | 4Y – výstup, hradlo 4   |
| 5   | 2B – vstup B, hradlo 2  | 10  | 3B – vstup B, hradlo 3  |
| 6   | 2Y – výstup, hradlo 2   | 9   | 3A – vstup A, hradlo 3  |
| 7   | GND – uzemnenie (zem)   | 8   | 3Y – výstup, hradlo 3   |

### Úloha 4: Zákony Booleovej algebry (BA)

| Zákon             | Forma AND (konjunktívna)  | Forma OR (disjunktívna)    |
|-------------------|--------------------------|---------------------------|
| Identita          | A · 1 = A                | A + 0 = A                 |
| Nulový element    | A · 0 = 0                | A + 1 = 1                 |
| Idempotentnosť    | A · A = A                | A + A = A                 |
| Komplementárnosť  | A · Ā = 0                | A + Ā = 1                 |
| Dvojitá negácia   | (Ā)' = A                 | (Ā)' = A                  |
| Komutatívnosť     | A · B = B · A            | A + B = B + A             |
| Asociatívnosť     | (A·B)·C = A·(B·C)        | (A+B)+C = A+(B+C)         |
| Distributívnosť   | A·(B+C) = A·B + A·C      | A+(B·C) = (A+B)·(A+C)    |
| Absorpcia         | A·(A+B) = A              | A + A·B = A               |
| De Morganove zákony | (A·B)' = Ā + B̄         | (A+B)' = Ā · B̄           |

### Záver

*(protokol je kompletný — záver je súčasťou tlačeného dokumentu s modrými tabuľkami)*

---

## Laboratórne cvičenie č. 22–23

**Názov cvičenia:** Vlastnosti logických obvodov. Overenie vlastností základných logických obvodov. Základné a odvodené logické funkcie – tabuľka.

### Úlohy

1. Zopakujte si vlastnosti základných log. obvodov, veľkosti napájacieho napätia, úrovne vstupných a výstupných signálov a označovanie vývodov puzdra DIL.
2. Overte logickú funkciu obvodov MH 7400, MH 7410, MH 7420, MH 7430, MH 7404. Pre všetky obvody nakreslite schématickú značku, zostavte pravdivostnú tabuľku a napíšte logickú rovnicu.
3. Charakterizujte správanie nepripojených vstupov obvodov NAND a NOR a navrhnite spôsoby ich ošetrenia. Pre obvody typu NAND zrealizujte aj kontrolu na zapojení obvodu MH 7400.
4. Zopakujte si jednotlivé typy základných a odvodených logických funkcií, charakterizujte ich a pre každú logickú funkciu definujte schematickú značku, rovnicu, KM, PT, principiálne zapojenie cez vypínače. (Tabuľka)

### Úloha 2: Overenie logickej funkcie obvodov — pravdivostné tabuľky

**MH7400 – dvojvstupový NAND (quad 2-input NAND)**
- Logická rovnica: Y = (A·B)'

| A | B | Y = (A·B)' |
|---|---|-----------|
| 0 | 0 | 1         |
| 0 | 1 | 1         |
| 1 | 0 | 1         |
| 1 | 1 | 0         |

**MH7410 – trojvstupový NAND (triple 3-input NAND)**
- Logická rovnica: Y = (A·B·C)'

| A | B | C | Y = (A·B·C)' |
|---|---|---|-------------|
| 0 | 0 | 0 | 1           |
| 0 | 0 | 1 | 1           |
| 0 | 1 | 0 | 1           |
| 0 | 1 | 1 | 1           |
| 1 | 0 | 0 | 1           |
| 1 | 0 | 1 | 1           |
| 1 | 1 | 0 | 1           |
| 1 | 1 | 1 | 0           |

**MH7420 – štvrvstupový NAND (dual 4-input NAND)**
- Logická rovnica: Y = (A·B·C·D)'

*(16-riadková tabuľka: Y = 0 len ak A=B=C=D=1, inak Y = 1)*

**MH7430 – osmvstupový NAND (single 8-input NAND)**
- Logická rovnica: Y = (A·B·C·D·E·F·G·H)'
- Pravdivostná tabuľka má 2⁸ = 256 riadkov. Y = 0 iba keď sú všetky vstupy A–H = log. 1. V ostatných 255 prípadoch Y = 1.

**MH7404 – invertor / NOT (hex inverter)**
- Logická rovnica: Y = Ā

| A | Y = Ā |
|---|-------|
| 0 | 1     |
| 1 | 0     |

### Úloha 3: Správanie nepripojených vstupov obvodu

**NAND – nepripojený vstup:**
- Voľný vstup obvodu NAND sa správa ako log. 1. Funkcia hradla sa nemení – pracuje správne s pripojenými vstupmi.

**NOR – nepripojený vstup:**
- Voľný vstup NOR sa tiež správa ako log. 1.

**Spôsob ošetrenia nepripojených vstupov:**
- Pri NOR pripojiť na GND a pri NAND na VCC.

### Úloha 4: Tabuľka základných a odvodených logických funkcií

| Funkcia  | Schematická značka | Rovnica              | PT (pravdivostná tab.) | KM                      | Zapojenie cez vypínače |
|----------|-------------------|----------------------|------------------------|------------------------|------------------------|
| AND      | A, B → [&] → y    | Y = A·B              | 0,0→0; 0,1→0; 1,0→0; 1,1→1 | A\B: 0→0,0; 1→0,1  | Sériové vypínače       |
| OR       | A, B → [≥1] → y   | Y = A + B            | 0,0→0; 0,1→1; 1,0→1; 1,1→1 | A\B: 0→0,1; 1→1,1  | Paralelné vypínače     |
| NOT      | A → [1] → y       | Y = Ā                | 0→1; 1→0              | A: 0→1; 1→0            | Vypínač paralelne so záťažou |
| NAND     | A, B → [&]○ → y   | Y = (A·B)' = Ā + B̄  | 0,0→1; 0,1→1; 1,0→1; 1,1→0 | A\B: 0→1,1; 1→1,0  | Sériové + negácia      |
| NOR      | A, B → [≥1]○ → y  | Y = (A+B)' = Ā · B̄  | 0,0→1; 0,1→0; 1,0→0; 1,1→0 | A\B: 0→1,0; 1→0,0  | Paralelné + negácia    |
| EXOR (XOR) | A, B → [=1] → y | Y = A ⊕ B = ĀB + AB̄ | 0,0→0; 0,1→1; 1,0→1; 1,1→0 | A\B: 0→0,1; 1→1,0  | Krížové prepojenie     |
| EXNOR (XNOR) | A, B → [=1]○ → y | Y = A ⊙ B = AB + ĀB̄ | 0,0→1; 0,1→0; 1,0→0; 1,1→1 | A\B: 0→1,0; 1→0,1 | Krížové + negácia      |

### Záver

*(protokol je kompletný — záver je súčasťou tlačeného dokumentu s modrými tabuľkami)*

---

## Laboratórne cvičenie č. 24 — príklad

**Zadanie:** Máte schému zapojenia zostaveného zo základných hradiel. Označte hradlá H1 až H7 podľa zadania príslušnými symbolmi. Potom urobte nasledujúce úlohy, ktoré vyplývajú zo schémy zapojenia:
1. Napíšte logickú funkciu, ktorú obvod vykonáva.
2. Napíšte do pravdivostnej tabuľky funkciu Y, ktorú obvod vykonáva.
3. Na základe pravdivostnej tabuľky vyplňte Karnaughovu mapu.
4. Nakreslite do Karnaughovej mapy kontúry a vypíšte minimalizovanú logickú funkciu.
5. Napíšte LF vo forme, ktorá je realizovateľná hradlami NAND.
6. Nakreslite schému zapojenia obvodu zostaveného z hradiel NAND.
7. Realizujte obvod na stavebnici číslicovej techniky a overte jeho činnosť.

### Schéma — zadanie skupín

| Hradlo/Skupina | H1    | H2    | H3   | H4   | H5  | H6   | H7    |
|---------------|-------|-------|------|------|-----|------|-------|
| A             | EXNOR | AND   | NAND | EXOR | NOT | NOR  | OR    |
| B             | EXOR  | NAND  | AND  | NOR  | NOT | OR   | EXNOR |
| C             | NOR   | AND   | NAND | EXNOR| NOT | OR   | EXOR  |
| D             | EXOR  | EXNOR | AND  | NOR  | NOT | OR   | NAND  |
| E             | NAND  | EXOR  | NOR  | AND  | NOT | EXNOR| OR    |

### Zadanie – Skupina A: priradenie hradiel

| H1    | H2  | H3   | H4   | H5  | H6  | H7 |
|-------|-----|------|------|-----|-----|----|
| EXNOR | AND | NAND | EXOR | NOT | NOR | OR |

### Úloha 1: Logická funkcia obvodu — odvodenie krok za krokom

```
H1 = EXNOR(A, B) = (A ⊕ B)' 
H2 = AND(B, C)   = B·C
H3 = NAND(B, C)  = (B·C)'
H4 = EXOR(H1, H2) = (A ⊕ B)' ⊕ (B·C)
H5 = NOT(H1)     = (A ⊕ B)''  = (A ⊕ B)
H6 = NOR(H3, H5) = ((A ⊕ B)' · (B·C)')'... = ((A⊕B)'' + (B·C)')'
Y = H7 = OR = [(A⊙B) ⊕ (B·C)] + [((A⊕B)'' + (B·C)')']
```

*(Pozn.: presné odvodenie závisí od konkrétneho zapojenia schémy z hodiny)*

### Úloha 2: Pravdivostná tabuľka

| A | B | C | H1 EXNOR | H2 AND | H3 NAND | H4 EXOR | H5 NOT | H6 NOR | Y=H7 OR |
|---|---|---|----------|--------|---------|---------|--------|--------|---------|
| 0 | 0 | 0 | 1        | 0      | 1       | 1       | 0      | 0      | 1       |
| 0 | 0 | 1 | 1        | 0      | 1       | 1       | 0      | 0      | 1       |
| 0 | 1 | 0 | 0        | 0      | 1       | 0       | 1      | 0      | 0       |
| 0 | 1 | 1 | 0        | 1      | 0       | 1       | 1      | 0      | 1       |
| 1 | 0 | 0 | 0        | 0      | 1       | 0       | 1      | 0      | 0       |
| 1 | 0 | 1 | 0        | 0      | 1       | 0       | 1      | 0      | 0       |
| 1 | 1 | 0 | 1        | 0      | 1       | 1       | 0      | 0      | 1       |
| 1 | 1 | 1 | 1        | 1      | 0       | 0       | 0      | 1      | 1       |

### Úloha 3: Karnaughova mapa

```
        B̄C̄   B̄C   BC   BC̄
Ā  | (1) | (1) | (1) |  0  |
A  |  0  |  0  | (1) | (1) |
```

### Úloha 4: Minimalizovaná logická funkcia

$$Y = \bar{A} \cdot \bar{B} + A \cdot B + B \cdot C$$

### Úloha 5: Logická funkcia vo forme NAND

$$Y = \overline{A}B + AB + BC$$

1. Y = NOT[NOT(Ā·B̄ + A·B + B·C)]
2. Y = NOT[NOT(Ā·B̄) · NOT(A·B) · NOT(B·C)]
3. **Y = NAND[NAND(Ā, B̄), NAND(A, B), NAND(B, C)]**

$$\text{NAND}(A, A) = \text{NOT}(A \cdot A) = \text{NOT}(A) = \bar{A}$$

$$\text{NAND}(B, B) = \text{NOT}(B \cdot B) = \text{NOT}(B) = \bar{B}$$

### Úloha 6: Popis schémy zapojenia z hradiel NAND

| Hr. | IC     | Vstupy             | Výstup            | Popis                      |
|-----|--------|--------------------|-------------------|----------------------------|
| H1  | MH7400 | A, A (oba vstupy = A) | Ā – inverzia vstupu A | NOT realizovaný pomocou NAND |
| H2  | MH7400 | B, B (oba vstupy = B) | B̄ – inverzia vstupu B | NOT realizovaný pomocou NAND |
| H3  | MH7400 | Ā (z H1), B̄ (z H2) | NOT(Ā·B̄)          | |
| H4  | MH7400 | A, B               | NOT(AB)           | |
| H5  | MH7400 | B, C               | NOT(BC)           | |
| H6  | MH7410 | H3, H4, H5 (tri vstupy) | Y – výstup obvodu | 3-vstupový NAND; výsledná funkcia |

*(schéma zapojenia z hradiel NAND v zošite)*

### Záver

*(protokol je kompletný — záver je súčasťou tlačeného dokumentu s modrými tabuľkami)*

---

## Laboratórne cvičenie č. 26

**Názov cvičenia:** Sčítačka

### Úlohy

1. Navrhnite polovičnú 1-bitovú sčítačku a overte jej činnosť. Na realizáciu využite hradlá typu NAND (MH 74 00).
2. Navrhnite úplnú 1-bitovú sčítačku a overte jej činnosť. Na realizáciu využite hradlá typu EXL-OR a NAND (MH 74 86, MH 74 00).
3. Vyhľadajte v katalógu, nakreslite značku, definujte vlastnosti a overte činnosť 4-bitovej úplnej sčítačky (MH 74 83) pri sčítaní 3 dvojíc ľubovoľných 4-bitových čísel. Ošetrite nevyužitý vstup C₀.
4. Zistite aký bude stav výstupov 4-bitovej úplnej sčítačky (MH 74 83) pre súčet dvoch maximálnych 4-bitových čísel? (uvažujte dva prípady ak C₀ = 0 a C₀ = 1)

### Úloha 1: Polovičná 1-bitová sčítačka z hradiel NAND (MH7400)

**Logické rovnice:**

$$S \text{ (Súčet)} = A \oplus B = \bar{A}B + A\bar{B}$$

$$P \text{ (Prenos)} = A \cdot B$$

**Pravdivostná tabuľka:**

| A | B | S = A⊕B | P = A·B |
|---|---|---------|---------|
| 0 | 0 | 0       | 0       |
| 0 | 1 | 1       | 0       |
| 1 | 0 | 1       | 0       |
| 1 | 1 | 0       | 1       |

**Realizácia pomocou hradiel NAND (MH7400):**

- Stredný výraz (potrebný pre S aj P): W = NAND(A, B) = (A·B)'
- S = NAND(NAND(A, W), NAND(B, W)) ← realizácia EXOR cez NAND
- P = NAND(W, W) = NOT(W) = NOT(NOT(A·B)) = A·B
- Obvod celkovo: 5 × 2-vstupový NAND → 2× MH7400

---

### Úloha 2: Úplná 1-bitová sčítačka z hradiel MH7486 (EXOR) a MH7400 (NAND)

**Logické rovnice:**

$$S = A \oplus B \oplus C$$

$$P = A \cdot B + B \cdot C + A \cdot C$$

**Pravdivostná tabuľka:**

| A | B | C | S = A⊕B⊕C | P |
|---|---|---|-----------|---|
| 0 | 0 | 0 | 0         | 0 |
| 0 | 0 | 1 | 1         | 0 |
| 0 | 1 | 0 | 1         | 0 |
| 0 | 1 | 1 | 0         | 1 |
| 1 | 0 | 0 | 1         | 0 |
| 1 | 0 | 1 | 0         | 1 |
| 1 | 1 | 0 | 0         | 1 |
| 1 | 1 | 1 | 1         | 1 |

**Realizácia (MH7486 + MH7400):**

1. XOR: X = A ⊕ B
2. XOR: S = X ⊕ C
3. P = NAND(NAND(A, B), NAND(X, C))

Obvod celkovo: 2× 2-vstupový XOR + 3× 2-vstupový NAND → 1× MH7486 + 1× MH7400

---

### Úloha 3: 4-bitová úplná sčítačka MH7483

**Popis obvodu MH7483:**

MH7483 je 4-bitová úplná sčítačka.
- Vstupy: A1–A4, B1–B4, C0 (vstupný prenos)
- Výstupy: S1–S4 (súčet), C4 (výstupný prenos)
- Nevyužitý vstup C0 musí byť pripojený na GND (log. 0).

**Overenie funkcie (C0 = 0):**

| A (4-bit)  | B (4-bit)  | C0 | S (výsledok) | C4 | Overenie           |
|-----------|-----------|----|--------------|----|-------------------|
| 0110 (6)  | 0011 (3)  | 0  | 1001 (9)     | 0  | 6 + 3 = 9         |
| 1010 (10) | 0101 (5)  | 0  | 1111 (15)    | 0  | 10 + 5 = 15       |
| 1100 (12) | 0101 (5)  | 0  | 0001 (1)     | 1  | 12 + 5 = 17; C4=1, S=0001 |

Nevyužité bity vstupov A, B alebo C0 sa pripájajú na GND (log. 0). C4 indikuje preplnenie (overflow).

---

### Úloha 4: Maximálny možný súčet 4-bitových čísel

Najväčšie 4-bitové číslo: 1111₂ = 15₁₀

**Pre C0 = 0:**

| A        | B        | C0 | S (4-bit) | C4 |
|----------|----------|----|-----------|-----|
| 1111 (15)| 1111 (15)| 0  | 1110 (14) | 1   |

Výsledok: C4=1, S=1110₂ → 2⁴ + 14 = 30₁₀

**Pre C0 = 1:**

| A        | B        | C0 | S (4-bit) | C4 |
|----------|----------|----|-----------|-----|
| 1111 (15)| 1111 (15)| 1  | 1111 (15) | 1   |

Výsledok: C4=1, S=1111₂ → 2⁴ + 15 = 31₁₀

Maximálny súčet na MH7483 je **31** (C0=1), resp. **30** (C0=0).

### Záver

*(protokol je kompletný — záver je súčasťou tlačeného dokumentu s modrými tabuľkami)*
