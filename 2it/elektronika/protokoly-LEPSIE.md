# Elektronika – laboratórne protokoly

> **Poznámky k prepisu:**
> - Negácia premennej (pruh nad písmenom) je zapísaná ako `A̅`, `B̅`, `C̅`, `D̅`,
>   prípadne apostrofom `( )'` tam, kde to tak bolo v origináli.
> - Pri každom cvičení je rozlíšené, čo bolo **vytlačené** (zadanie, šablóny,
>   počítačovo vysádzané tabuľky a grafy) a čo je **rukou písané** (namerané
>   hodnoty, výpočty, závery, dokreslené značky a schémy).
> - Grafy na milimetrovom papieri a počítačové grafy sú opísané slovne; samotné
>   namerané body zodpovedajú tabuľkám pri danom cvičení.
> - Miesta, kde si nie som istý prečítaním, sú výslovne označené ⚠️.

---

# Laboratórne cvičenie č. 14 — Overenie činnosti špeciálnych diód

*(ELE – IST 2.ročník)*

## Zadanie (vytlačené)

**Názov cvičenia:** Overenie činnosti špeciálnych diód

**Úlohy:**
1. Vyhľadajte v katalógu obmedzujúce veličiny predložených diód. *(rukou dopísané: I_Z = 85 mA)*
2. Zapojte prístroje a súčiastky podľa daných schém.
3. Pri rôznych napätiach U_R zistite veľkosť prúdu I_R a nakreslite namerané charakteristiky Zenerovej diódy v závernom smere I_R = f(U_R). Vymedzte na nich dovolenú pracovnú oblasť určenú na stabilizáciu napätia.
4. Zistite kapacitu varikapu pomocou mostíka RLCG pri rôznych hodnotách záverného napätia U_R. Nakreslite namerané charakteristiky C = f(U_R) a na nich určte zmenu kapacity ΔC vplyvom zmeny napätia ΔU minimálne v troch rôznych prac. bodoch.
5. Nakreslite schému a tabuľku pre meranie VACH LED diódy a overte ju v priepustnom smere, zostrojte VACH, vyznačte prahové napätie.
6. Namerané údaje vyhodnoťte a porovnajte s katalógovými.

**Schémy zapojenia (vytlačené):** „schéma zap. pre Zenerovu diódu" (mA-meter, voltmeter V, dióda) a „schéma zap. pre varikap" (voltmeter V, dióda, blok MER / RLCG).

## Namerané hodnoty (rukou)

### Tabuľka — ZENEROVA dióda

| Typ diódy | U_R (V) | I_R (mA) |
|---|---|---|
| ZENEROVA | 5,4 | 0,5 |
| | 11,6 | 1 |
| | 12 | 10 |
| | 12,27 | 20 |
| | 12,9 | 40 |
| | 13,9 | 80 |

### Tabuľka — LED dióda

*(V tlačenej šablóne bol typ „VARIKAP" prečiarknutý a rukou nahradený „LED";
tlačený nadpis tretieho stĺpca „C(pF)" bol prepísaný na „I_F (mA)". Hodnoty v
prvom stĺpci sú priepustné napätia U_F.)*

| Typ diódy | U_F (V) | I_F (mA) |
|---|---|---|
| LED | 1,71 | 0,6 |
| | 1,74 | 1 |
| | 1,78 | 2 |
| | 1,84 | 5 |
| | 1,87 | 7 |
| | 1,91 | 10 |

## Grafy (rukou, na milimetrovom papieri)

- **Zenerova dióda** — VACH v závernom smere: os y = U_R/V, os x = I_R/mA. Krivka má ostré „koleno" (prieraz) a potom mierny nárast napätia s prúdom — stabilizačná oblasť okolo 12–13 V.
- **LED dióda** — VACH v priepustnom smere: os y = U_F/V (značky 1,71; 1,74; 1,78; 1,84; 1,87; 1,91), os x = I_F/mA (0,6; 1; 2; 5; 7; 10). Rastúca priepustná charakteristika.

## Záver (rukou)

Pri meraní Zenerovej diódy v závernom smere sme zistili, že so zvyšujúcim sa záverným prúdom sa napätie mení len nepatrne a pohybuje sa približne v rozsahu 12 až 13 V. Táto oblasť zodpovedá stabilizačnej oblasti Zenerovej diódy a je v súlade s katalógovými údajmi.

Pri meraní LED diódy v priepustnom smere sme zistili, že dióda začína vodivo viesť pri napätí 1,7 V a pri prúde 10 mA dosahuje priepustné napätie približne 1,9 V. Namerané hodnoty zodpovedajú katalógovým charakteristikám LED diódy.

Cieľ merania bol splnený a potvrdzujú teoretické predpoklady.

---

# Laboratórne cvičenie č. 15 — Bipolárne tranzistory (KF 508), prevodové VACH a „h" parametre

*(ELE – IST 2.ročník; rukou dopísané v rohu: „abs.")*

## Zadanie (vytlačené)

**Názov cvičenia:** Nelineárne súčiastky elektronických obvodov – bipolárne tranzistory. Grafické zostrojovanie prevodových VACH bipolárneho tranzistora a výpočet „h" parametrov.

**Úlohy:**
1. Oboznámte sa so základnými katalógovými hodnotami daného bipolárneho tranzistora KF 508.
2. Z predložených výstupných VACH bipolárneho tranzistora KF 508 graficky zostrojte prevodové VACH pre Uce=10 V a Uce=20 V.
3. Daný pracovný bod P so súradnicami Uce=10 V, Ic=20 mA, Ib=120 μA, preneste do II. a III. kvadrantu.
4. Navrhnite kolektorový odpor Rc tak, aby zaťažovacia priamka išla cez daný pracovný bod P, ak je dané napájacie napätie Ucc= 20 V.
5. V okolí pracovného bodu vyznačte pracovnú oblasť ΔUce=12 V, tomu zodpovedajúce ΔIc a preneste do II. a III. kvadrantu.
6. Vypočítajte parametre:
   - h22 = ΔIc/ΔUce pri podmienke Ib=120 μA
   - h21 = ΔIc/ΔIb pri podmienke Uce=10 V
   - h11 = ΔUbe/ΔIb pri podmienke Uce=10 V
7. Vypočítané parametre porovnajte s katalógovými.

**Graf (vytlačený):** štvorkvadrantová charakteristika bipolárneho tranzistora KF 508 (výstupné VACH I_C = f(U_CE) pre rad hodnôt I_B = 20…220 μA, prevodová charakteristika a vstupná charakteristika U_BE). Do grafu je rukou dokreslená zaťažovacia priamka, pracovný bod P a oblasť ΔU_CE = 12 V.

## Výpočty (rukou)

Odčítané prírastky z grafu:

- ΔI_C = (33 mm / 14 mm) · 10 = 23,6 mA
- ΔI_B = (27 mm / 17 mm) · 100 = 159 μA
- ΔU_BE = (5 / 7) · 100 = 71 mV
- ΔU_CE = 12 V

Parametre:

- h22 = 23,6 mA / 12 V = 23,6 mA / 12 000 mV = **1,96 mS**
- h21 = 23,6 mA / 159 μA = 23 600 / 159 = **148,4**
- h11 = 71 mV / 159 μA = 71 000 / 159 = **446 Ω**
- R_C = U_CC / I_Cmax = 20 / 40 mA = 0,5 · 10³ = **500 (Ω)**

---

# Laboratórne cvičenie č. 16 — Bipolárne tranzistory v zapojení so spoločným emitorom (BT – SE)

*(ELE – IT 2.ročník; rukou dopísané v rohu: „abs.")*

## Zadanie (vytlačené)

**Názov cvičenia:** Nelineárne súčiastky elektronických obvodov – bipolárne tranzistory. Overenie vlastností bipolárnych tranzistorov v zapojení so spoločným emitorom (BT - SE).

**Úlohy:**
1. Vyhľadajte v katalógu obmedzujúce veličiny predložených BT (Icmax., Ucemax., Pcdov.)
2. Zapojte meracie prístroje podľa predloženej schémy.
3. Zmerajte 2 vstupné a 3 výstupné VACH a zostrojte ich.
4. Pre zvolené konštantné výstupné napätie (Uce=k) graficky zostrojte prevodovú charakteristiku.
5. Pre zvolený pracovný bod a pracovnú oblasť vypočítajte parametre h11, h21, h22. Pripravte si vzťahy na výpočet parametrov!
6. Vyhodnotenie merania.

**Funkčné vzťahy pre jednotlivé VACH:**
- VSTUPNÉ VACH: U_be = f(I_b) / U_ce = k
- VÝSTUPNÉ VACH: I_c = f(U_ce) / I_b = k
- PREVODOVÉ VACH: I_c = f(I_b) / U_ce = k

**Schéma zapojenia (vytlačená):** U1 – R1 (potenciometer) – R2 – ampérmeter A – tranzistor – voltmetre V – R3 – U2.

## Namerané hodnoty (rukou) — výstupné VACH

*(Hodnoty I_B v hlavičkách jednotlivých stĺpcov neboli doplnené.)*

| Uce (V) | Ic (A) — stĺpec 1 | Ic (A) — stĺpec 2 | Ic (A) — stĺpec 3 |
|---|---|---|---|
| 1 | 13 | 22 | 25,4 |
| 2 | 15,15 | 22,4 | 27,1 |
| 3 | 15,3 | 22,7 | 27,9 |
| 4 | 15,32 | 23,4 | 28,6 |
| 5 | 15,6 | 24 | 29,3 |
| 10 | 17 | 26,2 | 31,5 |
| 15 | 18,4 | 28,7 | 34,3 |
| 20 | 19,5 | 34,5 | 38,7 |
| 25 | 21,7 | 37,5 | 43,2 |
| 30 | 23 | 41,2 | 48,1 |

**vstupné VACH** — tlačená tabuľka (hlavičky Uce= (V) | U_be(V)) ostala **prázdna**, bez vyplnených údajov.

## Druhá strana zadania č. 16 (vytlačená, bez vyplnenia)

Za tabuľkou nasleduje ešte jedna vytlačená strana zadania (s nadpisom „laboratórne cvičenie č.16"), obsahovo zhodná s úlohami cvičenia č. 15 (grafické zostrojovanie prevodových VACH KF 508 a výpočet h-parametrov, body 1–7). Nie sú v nej žiadne rukou písané odpovede.

---

# Laboratórne cvičenie č. 17 — Unipolárne tranzistory (KF 520) v zapojení so spoločným emitorom (UT – SE)

*(ELE – IST 2.ročník)*

## Zadanie (vytlačené)

**Názov cvičenia:** Nelineárne súčiastky elektronických obvodov – unipolárne tranzistory. Overenie vlastností unipolárnych tranzistorov v zapojení so spoločným emitorom (UT - SE).

**Úlohy:**
1. Vyhľadajte v katalógu obmedzujúce veličiny predložených UT (Icmax., Ucemax., Pcdov.) *(rukou: KF 520)*
2. Zapojte meracie prístroje podľa predloženej schémy.
3. Zmerajte výstupné VACH - UT s vodivým kanálom v obohatenom, aj v ochudobnenom režime a zostrojte ich. *(rukou: 10 V)*
4. Pre zvolené konštantné výstupné napätie (Uce=k) graficky zostrojte prevodovú charakteristiku (alebo ju odmerajte a potom zostrojte).
5. Pre zvolený pracovný bod a pracovnú oblasť vypočítajte parametre y21, y22. Pripravte si vzťahy na výpočet parametrov! *(rukou: bez parametrov)*
6. Vyhodnotenie merania.

**Funkčné vzťahy pre jednotlivé VACH:**
- VÝSTUPNÉ VACH: I_c = f(U_ce) / U_ge = k
- PREVODOVÉ VACH: I_c = f(U_ge) / U_ce = k

**Schéma zapojenia (vytlačená):** R1 – V – R2 – tranzistor KF 520 (značka MOSFET) – V – A – R3.

## Namerané hodnoty (rukou) — výstupné VACH

*(I_C je v mA — rukou dopísané „mA" k hlavičke „Ic(A)".)*

| Uce (V) | Uge=0 V | Uge=2 V | Uge=4 V | Uge=−2 V | Uge=−4 V |
|---|---|---|---|---|---|
| 1 | 0,9 | 1 | 1,17 | 0,7 | 0,56 |
| 2 | 1,5 | 1,76 | 2 | 1,2 | 0,89 |
| 3 | 1,9 | 2,3 | 2,7 | 1,5 | 1,07 |
| 4 | 2,2 | 2,7 | 3,3 | 1,66 | 1,14 |
| 5 | 2,38 | 3 | 3,67 | 1,75 | 1,17 |
| 6 | 2,5 | 3,2 | 4 | 1,78 | 1,18 |
| 8 | 2,55 | 3,36 | 4,3 | 1,8 | 1,2 |
| 10 | 2,58 | 3,42 | 4,45 | 1,83 | 1,22 |
| 15 | 2,63 | 3,5 | 4,57 | 1,86 | 1,24 |
| 20 | 2,67 | 3,56 | 4,6 | 1,9 | 1,3 |

> *(Overené v plnom rozlíšení: predposledný riadok je **15** a hodnota v stĺpci
> U_ge=−2 V pri U_ce=20 je **1,9** — stĺpec teda rastie monotónne 1,8; 1,83;
> 1,86; 1,9. Skoršia neistota „16/1,3" pochádzala z čítania zmenšeného náhľadu.)

## Grafy (rukou, na milimetrovom papieri)

Štvorkvadrantový graf KF 520: vpravo výstupné VACH I_C/mA = f(U_CE/V) pre U_GE = +4, +2, 0, −2, −4 V; vľavo prevodová charakteristika I_C = f(U_GE). Pracovný bod P je vyznačený (×P) pri U_GE = 0 V, približne U_CE ≈ 10 V, I_C ≈ 2,5 mA.

## Záver (rukou)

V cvičení sme merali VACH charakteristiky unipolárneho tranzistora KF 520 pri rôznych hodnotách U_GE. Namerané hodnoty potvrdili, že pri kladnom U_GE (obohatený stav) prúd I_C narastá, a pri zápornom U_GE (ochudobnený stav) klesá. Charakteristiky majú typický priebeh – strmý nárast I_C v odporovej oblasti a stabilizáciu v aktívnej oblasti.

Správanie tranzistora potvrdzuje teoretické poznatky o unipolárnych tranzistoroch.

---

# Laboratórne cvičenie č. 18–19 — Optoelektronické súčiastky

*(ELE – IST 2.ročník)*

## Zadanie (vytlačené)

**Názov cvičenia:** Optoelektronické súčiastky. Overenie vlastností fotoprvkov.

**Úlohy:**
1. Vyhľadajte v katalógu obmedzujúce veličiny predložených fotoprvkov.
2. Zapojte meracie prístroje podľa predložených schém.
3. Overte ako sa mení odpor fotorezistora v závislosti od zmeny intenzity osvetlenia, ktorú určíme pomocou luxmetra.
4. Pri fototranzistore odmerajte výstupné VACH pri dvoch rôznych intenzitách osvetlenia.
5. Pri fotodióde určte vplyv zmeny intenzity osvetlenia na veľkosť jej anódového prúdu v odporovom režime (VACH v závernom smere).
6. V hradlovom režime fotodiódy určte ako sa zmení napätie naprázdno Uo a prúd nakrátko Ik, keď sa zmení intenzita osvetlenia.
7. Zistené údaje vyneste graficky. *(rukou: I_C max = 20 mA, U_CE max = 30 V)*
8. Vyhodnotenie merania.

**Schémy zapojenia (vytlačené, samostatná strana):** FOTOREZISTOR, FOTOTRANZISTOR, FOTODIÓDA – ODPOROVÝ REŽIM, FOTODIÓDA – HRADLOVÝ REŽIM (zvlášť zapojenie s ampérmetrom A pre I_k a s voltmetrom V pre U_o).

## a) Fotoodpor (rukou)

| E (lx) | R (Ω) |
|---|---|
| 100 | 1k8 (1800 Ω) |
| 200 | 1k2 (1200 Ω) |
| 300 | 950 |
| 400 | 800 |
| 500 | 710 |
| 600 | 640 |
| 700 | 588 |
| 800 | 550 |
| 900 | 515 |
| 1000 | 488 |

## b) Fototranzistor (rukou)

| Uce (V) | Ic (mA), E=300 lx | Ic (mA), E=600 lx |
|---|---|---|
| 2 | 2,6 | 4,3 |
| 4 | 2,7 | 4,5 |
| 6 | 2,9 | 4,7 |
| 8 | 2,8 | 4,9 |
| 10 | 2,8 | 5,2 |
| 12 | 3,2 | 5,4 |
| 14 | 3,34 | 5,7 |
| 16 | 3,4 | 6 |
| 18 | 3,4 | 6,3 |
| 20 | 3,46 | 6,7 |

## c) Fotodióda – odporový režim (rukou)

| U_KA (V) | I_A (mA), E=300 lx | I_A (mA), E=600 lx |
|---|---|---|
| 2 | 0,1 | 0,2 |
| 4 | 0,1 | 0,2 |
| 6 | 0,1 | 0,2 |
| 8 | 0,1 | 0,2 |
| 10 | 0,1 | 0,2 |
| 12 | 0,1 | 0,2 |
| 14 | 0,1 | 0,2 |
| 16 | 0,1 | 0,2 |
| 18 | 0,1 | 0,2 |
| 20 | 0,1 | 0,2 |

## d) Fotodióda – hradlový režim (rukou)

| E (lx) | U_o (mV) | I_k (μA) |
|---|---|---|
| 100 | 0,355 | 57 |
| 200 | 0,374 | 87 |
| 300 | 0,384 | 111 |
| 400 | 0,391 | 133 |
| 500 | 0,396 | 153 |
| 600 | 0,400 | 170 |
| 700 | 0,403 | 183 |
| 800 | 0,406 | 204 |
| 900 | 0,409 | 218 |
| 1000 | 0,411 | 235 |

> ⚠️ **Nezrovnalosť jednotiek:** tlačená hlavička stĺpca U_o má jednotku **„(mV)"**,
> no zapísané hodnoty (0,355 … 0,411) zodpovedajú skôr **voltom** (napätie naprázdno
> fotodiódy v hradlovom/fotovoltaickom režime býva ~0,3–0,4 V). Prepisujem verne to,
> čo je na papieri — jednotku odporúčam overiť.

## Grafy

**Rukou (milimetrový papier):**
- Fotoodpor: E/lx (os y) vs R/Ω (os x), klesajúca nelineárna krivka.
- Fototranzistor: I_C/mA (os y) vs U_CE/V (os x), dve krivky E=300 lx a E=600 lx.
- Fotodióda hradlový režim: E/lx vs I_k/μA a E/lx vs U_o/mV.
- Fotodióda odporový režim: I_A vs U_KA, dve takmer vodorovné čiary (E=300 lx ≈ 0,1 mA; E=600 lx ≈ 0,2 mA).

**Počítačovo vysádzané grafy (vytlačené):**
- „Fotodióda - hradlový režim - IK": E (lx) vs I_K (μA), takmer lineárny nárast (body od (57; 100) po (235; 1000)).
- „Fotodióda – odporový režim": I (mA) vs U_ka (V), dve vodorovné čiary E=300 lx (≈ 0,1 mA) a E=600 lx (≈ 0,19–0,2 mA).
- „Fotodióda - hradlový režim - Uo": E (lx) vs U_o (mV), rastúca nelineárna krivka (body od (355; 100) po (411; 1000)).
- „Fotoodpor": E (lx) vs R (Ω), klesajúca krivka (od R≈488 Ω pri 1000 lx po R≈1800 Ω pri 100 lx).
- „Fototranzistor": I_C (mA) vs U_CE (V), krivky E=300 lx a E=600 lx.

## Záver (vytlačený)

Meraním sme overili vlastnosti troch optoelektronických súčiastok.

Odpor fotorezistora klesal so zvyšujúcou sa intenzitou osvetlenia – z 1800 Ω pri 100 lx na 488 Ω pri 1000 lx. Grafom je klesajúca nelineárna krivka.

Výstupné VACH fototranzistora potvrdili, že vyššia intenzita osvetlenia spôsobuje väčší kolektorový prúd. Obe charakteristiky mierne stúpajú s rastom U_CE.

Fotodióda v odporovom režime vykazovala konštantný prúd nezávislý od záverného napätia.

V hradlovom režime napätie rastie nelineárne a prúd rastie približne lineárne s intenzitou osvetlenia.

Všetky namerané závislosti zodpovedajú teoretickým predpokladom.

---

# Laboratórne cvičenie č. 20–21 — Oboznámenie s unitestami; minimalizácia log. funkcií pomocou BA

*(ELE – IT 2.ročník)*

## Zadanie (vytlačené)

**Názov cvičenia:** Oboznámenie s unitestami. Základy číslicovej techniky – minimalizácia log. funkcií pomocou BA

**Úlohy:**
1. Oboznámte sa s predloženými učebnými pomôckami – unitestami, s druhom používaného školského stabilizovaného zdroja, s potrebnými obvodmi a katalógmi.
2. Pri unitestoch treba zohľadňovať veľkosť napájacieho napätia, umiestňovanie obvodov, realizáciu kontroly zapojenia, úroveň výstupných signálov overovať pomocou LED diód. Potrebné informácie si podľa inštrukcií vyučujúceho a pomocou konštrukčného katalógu zapíšte do cvičenia.
3. Pre obvody TTL vypíšte z konštrukčného katalógu hodnoty:
   - napájacieho napätia
   - úrovne vstupných a výstupných signálov (log. 1 a log. 0)
   - označenie vývodov puzdra DIL
4. Zopakujte si zákony BA.
5. Na predložených príkladoch precvičte minimalizáciu log. funkcií pomocou zákonov BA.

## Úloha 3: Hodnoty z konštrukčného katalógu – obvod MH7400 (NAND) (vytlačené)

| Parameter | Hodnota |
|---|---|
| Napájacie napätie VCC | 4,75 V – 5,25 V |
| Min. vstupné napätie log. 1 (UIH min) | 2,0 V |
| Max. vstupné napätie log. 0 (UIL max) | 0,8 V |
| Min. výstupné napätie log. 1 (UOH min) | 2,4 V |
| Max. výstupné napätie log. 0 (UOL max) | 0,4 V |
| Max. vstupný prúd log. 1 (IIH max) | 40 μA |
| Max. vstupný prúd log. 0 (IIL max) | −1,6 mA |

### Označenie vývodov puzdra DIL (MH7400)

| Pin | Signál | Pin | Signál |
|---|---|---|---|
| 1 | 1A – vstup A, hradlo 1 | 14 | VCC – napájacie napätie |
| 2 | 1B – vstup B, hradlo 1 | 13 | 4B – vstup B, hradlo 4 |
| 3 | 1Y – výstup, hradlo 1 | 12 | 4A – vstup A, hradlo 4 |
| 4 | 2A – vstup A, hradlo 2 | 11 | 4Y – výstup, hradlo 4 |
| 5 | 2B – vstup B, hradlo 2 | 10 | 3B – vstup B, hradlo 3 |
| 6 | 2Y – výstup, hradlo 2 | 9 | 3A – vstup A, hradlo 3 |
| 7 | GND – uzemnenie (zem) | 8 | 3Y – výstup, hradlo 3 |

## Úloha 4: Zákony Booleovej algebry (BA) (vytlačené)

| Zákon | Forma AND (konjunktívna) | Forma OR (disjunktívna) |
|---|---|---|
| Identita | A · 1 = A | A + 0 = A |
| Nulový element | A · 0 = 0 | A + 1 = 1 |
| Idempotentnosť | A · A = A | A + A = A |
| Komplementárnosť | A · A̅ = 0 | A + A̅ = 1 |
| Dvojitá negácia | (A̅)̅ = A | (A̅)̅ = A |
| Komutatívnosť | A · B = B · A | A + B = B + A |
| Asociatívnosť | (A·B)·C = A·(B·C) | (A+B)+C = A+(B+C) |
| Distributívnosť | A·(B+C) = A·B + A·C | A+(B·C) = (A+B)·(A+C) |
| Absorpcia | A·(A+B) = A | A + A·B = A |
| De Morganove zákony | (A·B)' = A̅ + B̅ | (A+B)' = A̅·B̅ |

---

# Laboratórne cvičenie č. 22–23 — Vlastnosti logických obvodov; základné a odvodené logické funkcie

*(ELE – IST 2.ročník)*

## Zadanie (vytlačené)

**Názov cvičenia:** Vlastnosti logických obvodov. Overenie vlastností základných logických obvodov. Základné a odvodené logické funkcie - tabuľka

**Úlohy:**
1. Zopakujte si vlastnosti základných log. obvodov, veľkosti napájacieho napätia, úrovne vstupných a výstupných signálov a označovanie vývodov puzdra DIL.
2. Overte logickú funkciu obvodov MH 7400, MH 7410, MH 7420, MH 7430, MH 7404. Pre všetky obvody nakreslite schematickú značku, zostavte pravdivostnú tabuľku a napíšte logickú rovnicu.
3. Charakterizujte správanie nepripojených vstupov obvodov NAND a NOR a navrhnite spôsoby ich ošetrenia. Pre obvody typu NAND zrealizujte aj kontrolu na zapojení obvodu MH 7400.
4. Zopakujte si jednotlivé typy základných a odvodených logických funkcií, charakterizujte ich a pre každú logickú funkciu definujte schematickú značku, rovnicu, KM, PT, principiálne zapojenie cez vypínače. (Tabuľka)

## Úloha 2: Pravdivostné tabuľky (vytlačené; značky hradiel dokreslené rukou)

### MH7400 – dvojvstupový NAND (quad 2-input NAND), Y = (A·B)'

| A | B | Y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

### MH7410 – trojvstupový NAND (triple 3-input NAND), Y = (A·B·C)'

| A | B | C | Y |
|---|---|---|---|
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 |

### MH7420 – štvorvstupový NAND (dual 4-input NAND), Y = (A·B·C·D)'

| A | B | C | D | Y |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 1 |
| 0 | 0 | 0 | 1 | 1 |
| 0 | 0 | 1 | 0 | 1 |
| 0 | 0 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 1 |
| 0 | 1 | 0 | 1 | 1 |
| 0 | 1 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 1 |
| 1 | 0 | 0 | 1 | 1 |
| 1 | 0 | 1 | 0 | 1 |
| 1 | 0 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 1 |
| 1 | 1 | 0 | 1 | 1 |
| 1 | 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 | 0 |

### MH7430 – osemvstupový NAND (single 8-input NAND), Y = (A·B·C·D·E·F·G·H)'

Pravdivostná tabuľka má 2⁸ = 256 riadkov. Princíp je rovnaký: Y = 0 iba keď sú všetky vstupy A–H = log. 1. V ostatných 255 prípadoch Y = 1.

### MH7404 – invertor / NOT (hex inverter), Y = A̅

| A | Y |
|---|---|
| 0 | 1 |
| 1 | 0 |

## Úloha 3: Správanie nepripojených vstupov obvodu (vytlačené)

**NAND – nepripojený vstup:** Voľný vstup obvodu NAND sa správa ako log. 1. Funkcia hradla sa nemení – pracuje správne s pripojenými vstupmi.

**NOR – nepripojený vstup:** Voľný vstup NOR sa tiež správa ako log. 1.

**Spôsob ošetrenia nepripojených vstupov:** Pri NOR pripojiť na GND a pri NAND na VCC.

## Úloha 4: Tabuľka základných a odvodených logických funkcií (vytlačené; značky, vypínače a kontúry v KM dokreslené rukou)

Pre každú funkciu sú uvedené: schematická značka, rovnica, pravdivostná tabuľka (PT), Karnaughova mapa (KM) a principiálne zapojenie cez vypínače.

**AND** — Y = A·B

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

KM (A\B): A=0 → 0, 0; A=1 → 0, **1**. Zapojenie: vypínače A a B v sérii → žiarovka.

**OR** — Y = A+B

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

KM (A\B): A=0 → 0, **1**; A=1 → **1, 1**. Zapojenie: vypínače A a B paralelne → žiarovka.

**NOT** — Y = A̅

| A | Y |
|---|---|
| 0 | 1 |
| 1 | 0 |

KM: A=0 → **1**; A=1 → 0. Zapojenie: rozpínací vypínač A → žiarovka.

**NAND** — Y = (A·B)' = A̅ + B̅

| A | B | Y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

KM (A\B): A=0 → **1, 1**; A=1 → **1**, 0. Zapojenie: rozpínacie vypínače A a B paralelne → žiarovka.

**NOR** — Y = (A+B)' = A̅·B̅

| A | B | Y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

KM (A\B): A=0 → **1**, 0; A=1 → 0, 0. Zapojenie: rozpínacie vypínače A a B v sérii → žiarovka.

**EXOR (XOR)** — Y = A⊕B = A̅·B + A·B̅

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

KM (A\B): A=0 → 0, **1**; A=1 → **1**, 0. Zapojenie: prekrížené prepínače → žiarovka.

**EXNOR (XNOR)** — Y = A⊙B = A·B + A̅·B̅

| A | B | Y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

KM (A\B): A=0 → **1**, 0; A=1 → 0, **1**. Zapojenie: prepínače → žiarovka.

---

# Laboratórne cvičenie č. 24 — Príklad (logická funkcia obvodu z hradiel H1–H7)

*(ELE – IST 2.ročník)*

## Zadanie (vytlačené)

Máte schému zapojenia zostavenú zo základných hradiel. Označte hradlá H1 až H7 podľa zadania príslušnými symbolmi. Potom urobte nasledujúce úlohy, ktoré vyplývajú zo schémy zapojenia:
1. Napíšte logickú funkciu, ktorú obvod vykonáva.
2. Napíšte do pravdivostnej tabuľky funkciu Y, ktorú obvod vykonáva.
3. Na základe pravdivostnej tabuľky vyplňte Karnaughovu mapu.
4. Nakreslite do Karnaughovej mapy kontúry a vypíšte minimalizovanú logickú funkciu.
5. Napíšte LF vo forme, ktorá je realizovateľná hradlami NAND.
6. Nakreslite schému zapojenia obvodu zostaveného z hradiel NAND.
7. Realizujte obvod na stavebnici číslicovej techniky a overte jeho činnosť.

**Schéma (vytlačená):** vstupy A, B, C → hradlá H1, H2, H3 (prvý stĺpec) → H4, H5, H6 (druhý stĺpec) → H7 → výstup Y.

**Priradenie hradiel podľa skupiny (vytlačená tabuľka):**

| Hradlo \ Skupina | H1 | H2 | H3 | H4 | H5 | H6 | H7 |
|---|---|---|---|---|---|---|---|
| A | EXNOR | AND | NAND | EXOR | NOT | NOR | OR |
| B | EXOR | NAND | AND | NOR | NOT | OR | EXNOR |
| C | NOR | AND | NAND | EXNOR | NOT | OR | EXOR |
| D | EXOR | EXNOR | AND | NOR | NOT | OR | NAND |
| E | NAND | EXOR | NOR | AND | NOT | EXNOR | OR |

## Riešenie pre Skupinu A (vytlačené)

**Priradenie hradiel:** H1=EXNOR, H2=AND, H3=NAND, H4=EXOR, H5=NOT, H6=NOR, H7=OR.

### Úloha 1: Logická funkcia obvodu — odvodenie krok za krokom

- H1 = EXNOR(A, B) = (A⊕B)'
- H2 = AND(B, C) = B·C
- H3 = NAND(B, C) = (B·C)'
- H4 = EXOR(H1, H2) = (A⊕B)' ⊕ (B·C)
- H5 = NOT(H1) = (A⊕B)''
- H6 = NOR(H3, H5) = ((A⊕B)'' + (B·C)')'
- Y = H7 = [(A⊙B) ⊕ (B·C)] + ((A⊕B)'' + (B·C)')'

### Úloha 2: Pravdivostná tabuľka

| A | B | C | H1 (EXNOR) | H2 (AND) | H3 (NAND) | H4 (EXOR) | H5 (NOT) | H6 (NOR) | Y=H7 (OR) |
|---|---|---|---|---|---|---|---|---|---|
| 0 | 0 | 0 | 1 | 0 | 1 | 1 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 | 0 | 1 | 1 | 0 | 0 | 1 |
| 0 | 1 | 0 | 0 | 0 | 1 | 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 | 1 | 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 0 | 1 | 0 | 1 | 0 | 0 |
| 1 | 0 | 1 | 0 | 0 | 1 | 0 | 1 | 0 | 0 |
| 1 | 1 | 0 | 1 | 0 | 1 | 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 | 0 | 0 | 0 | 1 | 1 |

### Úloha 3: Karnaughova mapa

|     | B̅·C̅ | B̅·C | B·C | B·C̅ |
|-----|------|------|-----|------|
| **A̅** | 1 | 1 | 1 | 0 |
| **A**  | 0 | 0 | 1 | 1 |

*(do mapy sú rukou dokreslené kontúry zoskupení)*

### Úloha 4: Minimalizovaná logická funkcia

> **Y = A̅·B̅ + A·B + B·C**

### Úloha 5: Logická funkcia vo forme NAND

Y = A̅B̅ + AB + BC

1. Y = NOT[ NOT(A̅·B̅ + A·B + B·C) ]
2. Y = NOT[ NOT(A̅·B̅) · NOT(A·B) · NOT(B·C) ]
3. **Y = NAND[ NAND(A̅, B̅), NAND(A, B), NAND(B, C) ]**

Pomocné (inverzia cez NAND):
- NAND(A, A) = NOT(A·A) = NOT(A) = A̅
- NAND(B, B) = NOT(B·B) = NOT(B) = B̅

### Úloha 6: Popis schémy zapojenia z hradiel NAND (vytlačená tabuľka; schéma dokreslená rukou)

| Hr. | IC | Vstupy | Výstup | Popis |
|---|---|---|---|---|
| H1 | MH7400 | A, A (oba vstupy = A) | A̅ – inverzia vstupu A | NOT realizovaný pomocou NAND |
| H2 | MH7400 | B, B (oba vstupy = B) | B̅ – inverzia vstupu B | NOT realizovaný pomocou NAND |
| H3 | MH7400 | A̅ (z H1), B̅ (z H2) | NOT(A̅·B̅) | |
| H4 | MH7400 | A, B | NOT(A·B) | |
| H5 | MH7400 | B, C | NOT(B·C) | |
| H6 | MH7410 | H3, H4, H5 (tri vstupy) | Y – výstup obvodu | 3-vstupový NAND; výsledná funkcia |

**Schéma (rukou):** H1 a H2 ako invertory z NAND (A̅, B̅); H4 = NAND(A,B); H5 = NAND(B,C); H3 = NAND(A̅, B̅); H6 = 3-vstupový NAND(H3, H4, H5) → Y.

---

# Laboratórne cvičenie č. 26 — Sčítačka

*(ELE – IST 2.ročník)*

## Zadanie (vytlačené)

**Názov cvičenia:** Sčítačka

**Úlohy:**
1. Navrhnite polovičnú 1-bitovú sčítačku a overte jej činnosť. Na realizáciu využite hradlá typu NAND (MH 7400).
2. Navrhnite úplnú 1-bitovú sčítačku a overte jej činnosť. Na realizáciu využite hradlá typu EXL-OR a NAND (MH 7486, MH 7400).
3. Vyhľadajte v katalógu, nakreslite značku, definujte vlastnosti a overte činnosť 4-bitovej úplnej sčítačky (MH 7483) pri sčítaní 3 dvojíc ľubovoľných 4-bitových čísel. Ošetrite nevyužitý vstup Co.
4. Zistite aký bude stav výstupov 4-bitovej úplnej sčítačky (MH 7483) pre súčet dvoch maximálnych 4-bitových čísel? (uvažujte dva prípady ak Co = 0 a Co = 1)

## Úloha 1: Polovičná 1-bitová sčítačka z hradiel NAND (MH7400) (vytlačené)

Logické rovnice:
- S (Súčet) = A ⊕ B = A·B̅ + A̅·B
- P (Prenos) = A·B

| A | B | S = A⊕B | P = A·B |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |

**Realizácia pomocou hradiel NAND (MH7400):**
- Stredný výraz (potrebný pre S aj P): W = NAND(A, B) = (A·B)'
- S = NAND( NAND(A, W), NAND(B, W) ) [realizácia EXOR cez NAND]
- P = NAND(W, W) = NOT(W) = NOT(NOT(A·B)) = A·B
- Obvod celkovo: 5 × 2-vstupový NAND → 2 × MH7400

## Úloha 2: Úplná 1-bitová sčítačka z hradiel MH7486 (EXOR) a MH7400 (NAND) (vytlačené)

Logické rovnice:
- S = A ⊕ B ⊕ C
- P = A·B + B·C + A·C

| A | B | C | S = A⊕B⊕C | P |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 0 | 1 | 0 |
| 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 1 | 0 |
| 1 | 0 | 1 | 0 | 1 |
| 1 | 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 |

**Realizácia (MH7486 + MH7400):**
1. XOR: X = A ⊕ B
2. XOR: S = X ⊕ C
- P = NAND( NAND(A, B), NAND(X, C) )
- Obvod celkovo: 2 × 2-vstupový XOR + 3 × 2-vstupový NAND → 1 × MH7486 + 1 × MH7400

## Úloha 3: 4-bitová úplná sčítačka MH7483 (vytlačené)

**Popis obvodu MH7483:**
- MH7483 je 4-bitová úplná sčítačka.
- Vstupy: A1–A4, B1–B4, C0 (vstupný prenos).
- Výstupy: S1–S4 (súčet), C4 (výstupný prenos).
- Nevyužitý vstup C0 musí byť pripojený na GND (log. 0).

**Overenie funkcie (C0 = 0):**

| A (4-bit) | B (4-bit) | C0 | S (výsledok) | C4 | Overenie |
|---|---|---|---|---|---|
| 0110 (6) | 0011 (3) | 0 | 1001 (9) | 0 | 6 + 3 = 9 |
| 1010 (10) | 0101 (5) | 0 | 1111 (15) | 0 | 10 + 5 = 15 |
| 1100 (12) | 0101 (5) | 0 | 0001 (1) | 1 | 12 + 5 = 17; C4=1, S=0001 |

Nevyužité bity vstupov A, B alebo C0 sa pripájajú na GND (log. 0). C4 indikuje preplnenie (overflow).

## Úloha 4: Maximálny možný súčet 4-bitových čísel (vytlačené)

Najväčšie 4-bitové číslo: 1111₂ = 15₁₀

**Pre C0 = 0:**

| A | B | C0 | S (4-bit) | C4 |
|---|---|---|---|---|
| 1111 (15) | 1111 (15) | 0 | 1110 (14) | 1 → des. výsledok = 30 |

Výsledok: C4=1, S=1110₂ → 2⁴ + 14 = 30₁₀

**Pre C0 = 1:**

| A | B | C0 | S (4-bit) | C4 |
|---|---|---|---|---|
| 1111 (15) | 1111 (15) | 1 | 1111 (15) | 1 → des. výsledok = 31 |

Výsledok: C4=1, S=1111₂ → 2⁴ + 15 = 31₁₀

**Maximálny súčet na MH7483 je 31 (C0=1) resp. 30 (C0=0).**
