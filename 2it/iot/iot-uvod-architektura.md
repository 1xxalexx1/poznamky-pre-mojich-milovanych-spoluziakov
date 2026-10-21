---
source: "iot.pdf"
tags: [iot, uvod, architektura, 2_it]
date_transcribed: "2026-04-25"
legibility: "high"
---

# IoT — úvod a architektúra

## Základné pojmy

- **informácia** — názov pre obsah toho, čo sa vymieňa s vonkajším svetom, keď sa mu prispôsobujeme alebo ovplyvňujeme ho; pomáha sa naň prispôsobovať
- **komunikácia** — prenos informácií medzi najmenej 2 účastníkmi
    - vyjadrenie ako cesta: zdroj → vysielač → signál → kanál → signál → prijímateľ → správa → cieľ
- **údaje (dáta)** — formalizovaný záznam ľudských vedomostí pomocou symbolov, ktorý je prenášateľný, uchovaný, interpretovaný alebo spracovaný
- **znalosť** — informácie v kontexte (súvislosti) tvoria znalosť

## Internet vecí (IoT)

- koncept, ktorého hlavnou myšlienkou je prepojenie všetkých fyzických vecí, ktoré sú napájané elektrickou en. a dokážu byť pripojené do internetu
- hl. cieľom je získať informácie z dát, ktoré všetky veci dokážu generovať

### Rozdiel IT a IoT

- prenášanie údajov
- počet zariadení
- presun hlavnej logiky

### Snímanie a zber dát

- 1 al. viac senzorov pre snímanie fyz. veličín a udalostí vo fyzickom svete
- každý senzor monitoruje špecifické podmienky
- v rámci IoT sa tieto senzory spájajú a tvoria komplexné systémy

### Oblasti nasadenia IoT

- poľnohospodárstvo
- logistika
- doprava
- smart grid — elektrická en. z obnoviteľných zdrojov
    - spojené dokopy — všetci môžu využívať

## Architektúra IoT

- viacero modelov

### Kľúčové vrstvy

- **hardware** — snímače, aktuátory, riadiace systémy
- **middleware** — úložisko dát, nástroje pre analýzu vykonávané nad údajmi
- **prezentačný systém** — spôsob, ako rozumieť údajom získaným z reálneho sveta — bývajú dostupné cez online GUI

### Reálne využívaný model

1. Hardwarová vrstva
2. Komunikačná vrstva (middleware)
3. Analytická vrstva
4. Aplikačná vrstva

## Hardwarová vrstva

- jednoduché zariadenia — snímače, akčné členy
- nepovažované za „inteligentné" členy — skôr senzory a snímače pripojené do siete IoT
- viac možností spracovania dát
- výstupové info napr.:
    - tlak a teplota
    - osvetlenie
    - info o geolokácii
    - počítadlá z výrobných procesov
    - obrázky, videá z kamery
    - dáta z gyroskopu

## Komunikačná vrstva

- označovaná aj ako **EDGE**
- zaistenie a udržovanie kom. medzi cloudom a edge zariadeniami
- zabezpečenie
- spracovanie dát by malo byť in real time
- predbežné spracovanie môže byť napr.:
    - **verifikácia dát** — overenie správnosti
    - **filtrovanie dát** — odstránenie chybných dát
    - **agregácia dát** — odstránenie viacnásobných záznamov

## Analytická vrstva

- spracovanie dát na nové info
- často sa predávajú
- hl. úlohy:
    - **analýza dát** — ktorý parameter má a nemá význam pre prediktívny model
    - **detekcia vzorov** — identifikácia opakujúcich sa dejov
    - **vytváranie prediktívnych modelov**

## Aplikačná vrstva

- interakcia s IoT systémami
- najčastejšie webové aplikácie na zobrazenie dát
- väčšinou len zobrazenie info, niekedy ovládanie

## SWOT analýza IoT

- strategický nástroj na plánovanie projektov
- **strengths** — silné stránky v porovnaní s inými projektmi
- **weaknesses** — slabé stránky v porovnaní s inými projektmi
- **opportunities** — možnosti vhodné využiť pre úspech projektu
- **threats** — riziká, ktoré by mohli spôsobiť problém pre projekt

## Súvisiace

- [[hardware-snimace-aktivne-cleny]]
- [[komunikacia]]

## Poznámky k prepisu

- V origináli „weaknesses — silné stránky" — pravdepodobne preklep, opravené na „slabé stránky" (štandardný význam SWOT).
- Skratka „en." pravdepodobne značí „energiu/energiou".
