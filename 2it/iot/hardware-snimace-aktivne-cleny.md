---
source: "iot.pdf"
tags: [iot, hardware, snimace, aktuatory, 2_it]
date_transcribed: "2026-04-25"
legibility: "high"
---

# Hardware a jeho komponenty

> Poznámka v origináli: „test odtiaľto dole"

## Rozdelenie

- snímače (senzory)
- akčné členy (servopohony)
- ovládače (kontroléry)

## Snímače

- zariadenia, ktoré merajú parametre a vlastnosti fyzického sveta (merajú fyzikálne vlastnosti / jednotky)
- menia tieto veličiny na elektronické signály

### Podľa signálu rozdeľujeme

- **digitálne snímače**
    - 1 alebo 0 — nie presná hodnota, len áno/nie
- **analógové snímače**
    - merajú presnú hodnotu
    - osvetlenie, vlhkosť…
- analógový snímač povie presne, koľko °C má objekt; digitálny povie len, či je horúci

### Podľa princípu delíme

- **odporové**
    - menia svoj odpor na základe fyzikálnej veličiny
    - napr. termistor (R-T krivka)
- **kapacitné**
    - merajú zmenu kapacity medzi elektródami
    - merajú napr. vlhkosť al. vzdialenosť
- **induktívne**
    - merajú zmenu indukcie v prítomnosti kovového objektu
- **piezoelektrické**
    - mechanickou deformáciou vzniká elektrický náboj, ktorý dokážeme merať
    - väčšinou v krištále
- **optické**
    - merajú napr. vlhkosť al. vzdialenosť
    - využívajú svetlo (normálne al. infračervené) na meranie vzdialenosti
- **ultrazvukové**
    - vyšle signál a meria, kým sa vrátil
    - využívajú zvukové vlny s vysokou frekvenciou na meranie vzdialenosti

## Akčné členy

- prvok, ktorý dostane na vstupe el. signál a na výstupe niečo vykoná
- akcia môže byť zmena:
    - mechanická
    - elektrická
    - informatívna

### Rozdeľujeme podľa typu pohonu

- **elektrické** — využívajú el. en. na vykonanie mechanickej operácie
- **hydraulické** — využívajú tlak kvapaliny na vykonanie mechanickej operácie
- **pneumatické** — využívajú stlačený vzduch na vykonanie mechanickej operácie

### Akčné členy — motory

- elektrické — využívajú el. en. na vykonanie mechanickej operácie
- hydraulické — využívajú tlak kvapaliny na vykonanie mechanickej operácie
- pneumatické — využívajú stlačený vzduch na vykonanie mechanickej operácie

### Iné akčné členy

- **zobrazovacie prvky** — LED, displeje
- **elektroakustické prvky** — sirény, reproduktory
- **ventily** — regulácia prietoku plynov a kvapalín
- **relé**

## Riadiace prvky

- jeho úlohou je prijať údaje zo snímačov → upraviť ich → vyhodnotiť → poslať signál akčnému členu
- nemusí pracovať okamžite — môže posielať dáta do servera
- môže byť aj obvod zo súčiastok na vykonávanie 1 úlohy — jednoúčelové zariadenie — embedded

### Mikropočítač / mikrokontrolér

- v hobby al. prototypovaní
- 1-čipový mikropočítač — mikrokontrolér — MCU
    - čip, ktorý obsahuje základné prvky počítača — CPU, RAM…

#### ESP32

- mikrokontrolér podobný arduinu
- Wi-Fi modul — rozdiel od arduina

#### Raspberry Pi

- poskytuje takmer 1000× väčší výkon a pamäť
- PC, na ktorom beží Linux (aj iné OS)
    - možnosť pripojiť myš a iné drivre
- vstavaný Wi-Fi a ethernet modul
- 1-kové napätie 3,3 V

### Rozširujúce moduly

- samé o sebe niektoré senzory nemôžu fungovať bez rezistorov a tranzistorov
- sú to kvalitnejšie moduly, ktoré sa dajú pripojiť napr. do arduina
- pre arduino existujú:
    - displeje
    - relé políčka
    - Wi-Fi moduly
    - atď.

## Parametre snímačov

- špecifikácie, ktoré popisujú vlastnosti a schopnosti s obmedzením rezistora
- sú kľúčové pri výbere senzora

### Rozsah teplôt

- definuje teploty, pri ktorých je snímač ešte plne ovládateľný

### Linearita

> Originál nedefinuje — termín samotný označuje, ako lineárne snímač reaguje na zmeny meranej veličiny.

### Presnosť

- miera, do akej senzor správne zodpovedá skutočnej hodnote meranej veličiny
- vyjadruje, akú veľkú odchýlku má výstup senzora od skutočnej hodnoty
- zahŕňa chyby spôsobené rôznymi faktormi: citlivosť, linearita, teplota, šum

### Životnosť

- čas, počas ktorého si senzor udržiava svoju funkčnosť a presnosť
- po uplynutí životnosti sa začnú prejavovať výraznejšie chyby alebo senzor úplne prestane fungovať
- životnosť závisí od typu senzora, kvality a podmienok, pri ktorých pracuje

## Súvisiace

- [[iot-uvod-architektura]]
- [[elektronika]]

## Poznámky k prepisu

- V origináli „1-kové napätie" pri Raspberry Pi — pravdepodobne myslené „logické napätie / napájacie napätie 3,3 V".
- „R-T krivka" pri termistore: nakreslený náčrt grafu závislosti odporu od teploty.
- „relé políčka" pre arduino — pravdepodobne „relé moduly".
