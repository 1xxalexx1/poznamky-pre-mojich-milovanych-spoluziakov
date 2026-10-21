# Fyzika – Mechanické vlnenie (poznámky)

> **Poznámky k prepisu:**
> - Ide o ručne písané zošitové poznámky (7 fotografovaných strán). Grafy a
>   schémy sú opísané slovne.
> - Miesta, kde text na fotografii dobieha do väzby zošita a je čiastočne
>   zakrytý, sú označené `[...]` s mojím doplnením v hranatých zátvorkách a
>   upozornením ⚠️.
> - `ω₀` = vlastná (uhlová) frekvencia, `y_m` = amplitúda, `λ` = vlnová dĺžka,
>   `T` = perióda, `f` = frekvencia, `v` = rýchlosť šírenia.

---

## Nútené kmitanie, rezonancia

### Nútené kmitanie
- vzniká pôsobením vonkajšej periodickej sily na oscilátor
- frekvencia kmitov oscilátora — ω₀ v ustálenom stave je potom zhodná s frekvenciou pôsobiacej sily — ω a kmitanie je netlmené 
### Rezonancia
- nastáva ak ω = ω₀
- amplitúda kmitov dosiahne najväčšiu hodnotu a dochádza k rezonančnému zosilneniu nútených kmitov

**Rezonančná krivka** *(graf)*: os y = y_m/y₀ (pomer amplitúd, značky 2, 4, 6, 8, 10), os x = ω/ω₀ (značky 0,5; 1; 1,5). Nakreslených je niekoľko kriviek pre rôzne tlmenie (ostrý vysoký vrchol „1", nižší širší „2" a najplochšia krivka) s maximom okolo ω/ω₀ = 1.

- poloha max. krivky určuje rezonančnú f. oscilátora a tvar krivky je ovplyvnený tlmením

---

## Mechanické vlnenie

- dej, pri kt. sa šíri mechanický kmitavý pohyb pružným prostredím
- prenáša sa pri ňom kmitavý pohyb a energia
- vo vákuu sa nešíri – nie sú častice, ktoré by mohli kmitať
- prenáša sa len energia – látka nie:
- poznáme:
	  - **postupné**
	    - priečne – kmitanie lana
	    - pozdĺžne – zvuk
	  - **stojaté**
	    - priečne
	    - pozdĺžne

### Fázová rýchlosť a dĺžka vlny
- **fázová rýchlosť v** – rýchlosť, akou sa vlnenie šíri prostredím
- **dĺžka vlny λ** – vzdialenosť, do kt. sa dostane vlnenie za čas T
	-  [ λ ] = m
	- vzdialenosť 2 najbližších bodov, kt. kmitajú v rovnakej fáze
	- vzdialenosť 2 najbližších maxím (miním) / zhustení (zriedení)
> **λ = v·T = v/f**



### Rovnica postupnej mechanickej vlny

*(schéma: zdroj kmitania Z, bod M vo vzdialenosti x; λ = v·T; x = v·τ, kde
x = vzdialenosť od zdroja a τ = čas oneskorenia kmitavého pohybu zo zdroja)*

Odvodenie:
- zdroj: y = y_m · sin(ω·t)
- bod M (oneskorený o τ): y = y_m · sin[ω·(t − τ)]
- keďže τ = x/v: y = y_m · sin[ω·(t − x/v)]
- keďže ω = 2π/T: y = y_m · sin[(2π/T)·(t − x/v)]

Ďalšie tvary (str. 2):
- y = y_m · sin[2π·(t/T − x/(v·T))]
- **y = y_m · sin[2π·(t/T − x/λ)]**  [m]

- rovnica postupnej vlny je funkcia 2 premenných ⟹ y = f(x; t)

---

## Riešené príklady – postupná vlna

### Príklad 1
**Zadanie:** y = 4·10⁻² · sin[2π(8t − 5x)] m. Určte y_m, T, λ, f, v.

- y_m = 4·10⁻² m
- porovnanie 8t = t/T ⟹ 8 = 1/T ⟹ T = 1/8 = **0,125 s**, f = **8 Hz**
- porovnanie 5x = x/λ ⟹ 5 = 1/λ ⟹ λ = 1/5 = **0,2 m**
- λ = v·T ⟹ 0,2 = v·0,125 ⟹ v = **1,6 m·s⁻¹**

### Príklad 2
**Zadanie:** Od zdroja sa šíri vlna s y_m = 10 cm; λ = 3 m a T = 2 s. Vypočítaj výchylku y bodu, ktorý je vzdialený 1,5 km od zdroja vlnenia, v čase 30 min od vzniku vlnenia.

- y = y_m · sin[2π(t/T − x/λ)]
- y_m = 10 cm = 0,1 m; λ = 3 m; T = 2 s; t = 30 min = 1800 s; x = 1,5 km = 1500 m
- y = 0,1 · sin[2π(1800/2 − 1500/3)] = **0 m**

### Príklad 3
**Zadanie:** Zapíšte rovnicu. f = 1 kHz, y_m = 3 mm, v = 340 m·s⁻¹. Vektor rýchlosti šírenia je orientovaný nesúhlasne s kladnou osou x.

- f = 1 kHz ⟹ T = 1/f = 1·10⁻³ s
- y_m = 3 mm = 0,003 m; v = 340 m/s (smer −x ⟹ v = −340)
- **y = 0,003 · sin[2π·(t/(1·10⁻³) − x/(−340·1·10⁻³))]**

### Príklad 4 *(str. 3)*
**Zadanie:** Aká je výchylka y (od rovnovážnej polohy) bodu vlnenia, ktorý je v čase t = (1/6)T od zdroja vzdialený x = (1/12)λ? y_m = 5 cm.

- t = (1/6)T; x = (1/12)λ; y_m = 5 cm = 0,05 m
- y = y_m · sin[2π(t/T − x/λ)]
- y = 0,05 · sin[2π(1/6 − 1/12)] = 0,05 · sin(2π · 1/12) = 0,05 · sin(30°) = 0,05 · 0,5
- y = **2,5 cm**

---

## Interferencia

- **skladanie vlnenia** 
- v miestach, kde súčasne prebieha viacero vlnení, nastáva skladanie vlnení alebo **interferencia vlnenia**
- **princíp superpozície:** ak teleso súčasne koná niekoľko harmonických pohybov rovnakého smeru s výchylkami y₁, y₂, y₃ … yₙ, je okamžitá výchylka výsledného kmitania
  > **y_v = y₁ + y₂ + … + yₙ** &nbsp;*(vektorový súčet)*

### 1. Vlny s rovnakou fázou sa skladajú
*(schémy: dva zdroje z₁ = z₂ pri d = 0, a posun d = 2·(λ/2); vlny sa sčítavajú – väčšia amplitúda)*

- ak sa dráhový rozdiel interferujúcich vlnení rovná **párnemu** počtu polvĺn, nastáva **zosilnenie vlnenia**
  > **d = 2k·(λ/2)**, &nbsp; kde k = 0, 1, 2; …

### 2. Interferencia vlnení s opačnou fázou
*(schéma: vlny v protifáze sa rušia)*

- ak sa dráhový rozdiel interferujúcich vlnení rovná **nepárnemu** počtu polvĺn, nastáva **zoslabenie vlnenia**
  > **d = (2k+1)·(λ/2)**

---

## Grafické skladanie vĺn

**Zadanie:** Graficky znázornite (skladanie) pre y_m1 = 3 cm; y_m2 = 2 cm.

**a) d = λ/2** *(vlny v protifáze – odčítanie):*
- y_v = y₁ − y₂ = 3 − 2 = **1 cm**

**b) d = 2·(λ/2) = λ** *(vlny v rovnakej fáze – sčítanie):*
- y_v = y₁ + y₂ = 3 + 2 = **5 cm**

---

## Fázový rozdiel

**Definícia (odvodenie):**
- Δφ = | 2π(t/T − x₁/λ) − 2π(t/T − x₂/λ) | = | 2π·t/T − 2π·x₁/λ − 2π·t/T + 2π·x₂/λ |
- Δφ = φ₁ − φ₂
  > **Δφ = 2π·(x₂ − x₁)/λ = 2π·(d/λ)**

### Príklad (f = 600 Hz)
**Zadanie:** Vlna s frekvenciou 600 Hz a rýchlosťou 340 m·s⁻¹. Určte fázový rozdiel medzi dvoma bodmi vzdialenými:
*(λ = v/f = 340/600)*

**a) 0,17 m:** Δφ = 2π·0,17/λ = 2π·0,17/(340/600) = **0,6π**

**b) 1,7 m:** Δφ = 2π·1,7/(340/600) = **6π**

### Príklad (z grafu)
**Zadanie:** Vypočítaj fázový rozdiel *(z grafu: λ = 10, d = x₂ − x₁ = 4 − 0 = 4):*
- Δφ = 2π·(x₂ − x₁)/λ = 2π·(4 − 0)/10 = **(4/5)π**

---

## Šírenie vlnenia v prostredí

### Huygensov princíp
- každý bod vlnoplochy, do kt. vlnenie v určitom okamihu dospelo, môžeme pokladať za zdroj elementárneho vlnenia
- výsledná vlnoplocha je vonkajšia obalová plocha všetkých elementárnych vlnoplôch
- všetky body vlnoplochy kmitajú s rovnakou fázou
- lúč určuje smer šírenia vlnenia – kolmica na vlnoplochu
  > **r = v·t** &nbsp; – polomer vlnoplôch

*(schéma: lúč, elementárna vlnoplocha, výsledná vlnoplocha, vlnoplocha)*

### Lom na rozhraní 2 prostredí
*(schéma: dopadajúci lúč, prostredie 1 s v₁, prostredie 2 s v₂, dopadajúci uhol, odrazený lúč a odrazený uhol, uhol lomu β, lomený lúč, rozhranie)*

**Zákon odrazu**
- uhol dopadu = uhlu odrazu ⟹ **α = α'**

**Zákon lomu – Snellov zákon**
> **sin α / sin β = v₁ / v₂ = n** &nbsp; – relatívny index lomu

- lom **ku** kolmici: β < α, &nbsp; v₂ < v₁
- lom **od** kolmice: β > α, &nbsp; v₂ > v₁

### Príklad (Snellov zákon)
**Zadanie:** v₁ = 340 m·s⁻¹; v₂ = 1450 m·s⁻¹; β = 45°; α = ?

- sin α / sin β = v₁/v₂
- sin α / sin(45°) = 340/1450
- sin α = (340/1450)·sin(45°) = 0,1658
- **α = 9,54°**

### Medzný uhol
- α_m – medzný uhol dopadu; lúč ide po hladine (β = 90°)
- sin α_m / sin 90° = v₁/v₂ &nbsp; (sin 90° = 1)
  > **sin α_m = v₁ / v₂**

**Príklad:** Pod akým najväčším uhlom môže dopadnúť [zvuková vlna], aby prenikla do vody?
- v₁ = 340 m·s⁻¹; v₂ = 1450 m·s⁻¹; α_m = ?
- sin α_m = v₁/v₂ ⟹ **α_m = 13,56°**
- podmienka: α < α_m ⟹ **α < 13,56°**

---

## Ohyb vlnenia – difrakcia
- vlnenie vstupuje do oblasti v tieni prekážky – za prekážku
- aby nastal ohyb, musia byť rozmery prekážky porovnateľné s vlnovou dĺžkou vlnenia

*(schéma: vlnoplochy ohýbajúce sa za prekážkou / štrbinou)*

---

## Stojaté vlnenie

- stojaté vlnenie vzniká interferenciou – skladaním priamej a odrazenej vlny
- vznikajú **kmitne** a **uzly**
  - kmitňa – bod s najväčším pohybom
  - uzol – bod bez pohybu
- ak je koniec bodu pevný, nastáva odraz s opačnou fázou – **uzol**
- ak je rad bodov na konci voľný, odráža sa vlnenie so súhlasnou fázou – **kmitňa**

*(schémy: stojatá vlna s vyznačenými uzlami a kmitňami)*

- body kmitajúce s max. amplitúdou sú **kmitne**
- body kmitajúce s 0 amplitúdou sú **uzly**
- vzdialenosť 2 susedných kmitní (a 2 susedných uzlov) je **λ/2**
- vzdialenosť najbližšej kmitne a uzla je **λ/4**

### Základná frekvencia stojatého vlnenia f₀ (1 kmitňa)
*(schéma: l = (1/2)λ ⟹ λ = 2l)*
> **f₀ = v / (2l)**

### Vyššie harmonické frekvencie
*(schémy: 2 kmitne → l = (2/2)λ; 3 kmitne → l = (3/2)λ)*
> **fₙ = n · f₀**, &nbsp; n = 2, 3, 4, 5 … &nbsp; *(n = počet kmitní)*
