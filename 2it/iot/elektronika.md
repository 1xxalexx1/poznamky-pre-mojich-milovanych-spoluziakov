---
source: "iot.pdf"
tags: [iot, elektronika, 2_it]
date_transcribed: "2026-04-25"
legibility: "high"
---

# Elektronika

## Základné pojmy

- el. prúd je tvorený usporiadaným pohybom nosičov el. náboja — e⁻
- e⁻ s p⁺ tvoria atómy
- el. náboj sa meria v Coulomboch
    - 1 Coulomb = množstvu I pri stálom U A/s

### Chemické prvky

- **el. vodiče** — materiály, ktoré majú slabú príťažlivosť medzi jadrom a e⁻
- **el. izolanty** — materiály, ktoré majú silnú príťažlivosť medzi e⁻ a e⁻; atóm neopúšťa

### Napätie

- energia, ktorá poháňa e⁻
- meriame medzi 2 bodmi
- V = volt

### Prúd

- usporiadaný tok e⁻
- A — ampér

### Výkon

- množstvo energie spotrebovanej v priebehu času
- W = Watt = V · I

### Obvod

- fyzická sieť prepojených el. komponentov

### Schéma

- nákres obvodu

### Integrované obvody

- miniaturizované obvody vyrobené na jednom kuse polovodiča
- často sa označujú ako čipy al. mikročipy
- môžu mať stovky až miliardy el. komponentov

## Sériové zapojenie

- komponenty sú zapojené za sebou
- I je na komponentoch rovnaký
- U = U₁ + U₂ …
- na zvýšenie U
- na jednoduchý obvod
- aby cez obvod pretekal jeden I

> Diagram: tri komponenty zapojené v rade

## Paralelné zapojenie

> Originál uvádza ako „sériové zapojenie" druhýkrát — ide však o paralelné: komponenty sú zapojené vedľa seba, ich konce sú v rovnakých uzloch.

- U je na komponentoch rovnaký
- I = I₁ + I₂ …
- na zvýšenie spoľahlivosti
- ak chcem rovnaké U na každom komp.
- na rôzne I, rovnaké U
- ak sa pokazí 1 komp., ostatné budú fungovať

## Analógový obvod

- hodnoty U al. I sa menia spojite v čase
- kontinuálna zmena signálov
- spracovanie signálov — int. obv.
- napr. operačné zosilňovače

## Digitálny obvod

- nadobúdajú el. signály diskrétne hodnoty
- logická 0/1:
    - zap./vyp.
    - vysoké/nízke
    - 20 mA / 0 mA
    - 3 V / 0 V
- logická 1 — 5 V / 3,3 V
- logická 0 — 0 V

## Jednosmerný prúd

- tečie len 1 smerom
- v IoT využívaný:
    - **napájanie** — baterky / solárne panely → arduino, bezdrôt. zar.
    - **energetická efektívnosť**
    - **stabilizácia napätia** — DC minimalizuje rušenie

## Striedavý prúd

- má smer toku el. periodicky (50/60 Hz)
- smart domácnosti a priemysel
- vysokovýkonové systémy
- diaľkové zariadenia a automatizácia

## Ohmov zákon

> Diagram: trojuholník U / R · I

- v IoT — návrh a ochrana senzorov pred preťažením I
- pr. LED

## Výkon

- ovplyvňuje:
    - spotrebu en.
    - životnosť batérií
    - efektivitu zariadení
- **P = U · I**
- v IoT je nízka spotreba kľúčová
- optimalizácia komp. v IoT — využitie nízkonapäťových komp. — ESP32
- efektívne riadenie napájania — prechod zariadení do deep sleep

## Rezistory

- pasívna el. súčiastka
- obmedzenie prúdu, zmena napätia, vývod tepla

### Podľa konštrukcie

- **drôtové** → výkonné, odolné voči teplu
- **uhlíkové** → lacné, menej presné
- **SMD** → malé

### Podľa funkcie

- **pevné** → konštantný odpor
- **premenlivé (potenciometre)** → nastaviteľný odpor
- **termistor** → závislé od teploty
- **LDR (fotorezistory)** → závislé od svetla

### Potenciometre

- premenlivé rezistory
- regulácia prúdu, napätia, výkonu

#### Podľa konštrukcie

- **otočné (rotory)**
- **posuvné (slidery)**
- **digitálne** — pomocou mikroprocesora

#### Podľa charakteristiky

- lineárne
- logaritmické

### Fotorezistor

- odpor sa mení v závislosti od intenzity svetla
- čím viac svetla, tým menej odporu

> Diagram: schématická značka fotorezistoru

## Aktívne súčiastky

### Dióda

- polovodičová dióda — súčiastky, ktoré prepúšťajú I v jednom smere
- polovodiče fungujú na princípe riadenia toku e⁻ v materiáli, ktorý nie je úplne vodivý ani úplne nevodivý
- pridávanie nečistôt — dopovanie — pridávanie atómov iného prvku
- v IoT sa využíva na usmerňovanie prúdu — ochrana a signalizácia
- skladá sa z 2 prímesových polovodičov typu N a P

#### Typy diód

- **Schottkyho**
    - nízke prahové napätie a rýchla odozva — napájanie IoT zariadení
    - ochrana pred prepätím
- **Zenerova**
    - navrhnutá na prácu v závernom smere
    - umožňuje stabilizované napätie pri určitom prieraznom — zenerovom napätí
- **LED**
    - pri priepustnom smere vyžaruje svetlo
    - funguje na princípe PN prechodu, ale vyžaruje pri ňom svetlo namiesto tepla
    - farba závisí od zloženia polovodičového materiálu
        - s farbou sa menia aj vlastnosti, napr. prahové U
- **RGB LED**
    - v 1 puzdre má 3 LED
    - nastavením intenzity LED vieme namiešať farby
    - LED obrazovky — 1 pixel = 1 RGB LED

> Diagram: I-V krivka diódy so záverným prahovým napätím V_BR (vľavo dolu) a priepustným napätím V_F (vpravo).

### Tranzistor

- trojvrstvová polovodičová súčiastka
- Báza, Emitor, Kolektor

#### Zapojenia

- **spoločný E** — spínanie
- **spoločná B** — zosilnenie napätia
- **spoločný C** — zosilnenie prúdu

### Elektromechanické prvky

- spínače, tlačidlá, prepínače, relé, konektory
- spojenie 2 a viac mechanických kontaktov

#### Spínač

- 2 polohy: zap. a vyp.

#### Prepínač

- 3 a viac kontaktov

#### Relé

- elektricky ovládaný spínač/prepínač
- využíva elektromagnet alebo aj solid state (absencia mechanických častí)

## Súvisiace

- [[hardware-snimace-aktivne-cleny]]
- [[komunikacia]]

## Poznámky k prepisu

- Originál uvádza pri paralelnom zapojení nadpis „sériové zapojenie" druhýkrát — pravdepodobne preklep, prepísané ako paralelné zapojenie podľa kontextu (popis vedľa seba, rovnaké U, súčet I).
- Označenie „pr." = „príklad".
- Skratka „komp." = komponent(y).
- „1-kový" pri ESP32 a podobne nahradené pojmom „nízkonapäťový" tam, kde to dáva zmysel; inde ponechané.
