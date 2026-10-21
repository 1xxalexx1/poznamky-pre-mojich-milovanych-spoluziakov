# Fyzika — Vlnenie

---

## Základné pojmy (mechanický oscilátor)

- **nútené kmitanie** — vzniká pôsobením vonkajšej periodickej sily na oscilátor
- frekvencia nútených kmitaní sa blíži k vlastnej frekvencii oscilátora → amplitúda rastie
- amplitúda kmitov dosahuje najvyššie hodnoty v oblasti rezonancie

### Rezonancia

- nastáva, keď sa frekvencia budiaceho kmitania rovná vlastnej frekvencii sústavy
- amplitúda dosahuje maximum
- **rezonančná krivka** — ostrá = malé tlmenie, plochá = veľké tlmenie

> *príklad — pozri príklad v zošite (str.1)*

---

## Mechanická vlna

- je to šírenie sa mechanického kmitavého pohybu prostredím
- prenosí sa pri tom kinetický pohyb a energia
- vo vlnení sa teda "neračia" samotné čiastočky prostredia — tie kmitajú len okolo rovnovážnych polôh
- energia sa len prenáša — látka nie

- **postupná vlna** — kmitanie lana:
  - pozdĺžna
  - priečna
  - povrchová

### Rýchlosť šírenia vlny

- **fázová rýchlosť** `v` — rýchlosť akou sa šíri vlna prostredím
- **vlnová dĺžka** `λ` — vzdialenosť dvoch bodov kmitajúcich v rovnakej fáze za čas `T`

$$\lambda = v \cdot T = \frac{v}{f}$$

- vzdialenosť 2 najbližších bodov kmitajúcich v rovnakej fáze (minimum vzdialenosti)
- vzdialenosť 2 najbližších bodov rovnakej fázy je `λ` (definícia vlnovej dĺžky)

---

## Rovnica postupnej mechanickej vlny

$$y = y_m \cdot \sin\!\left(2\pi\!\left(\frac{t}{T} - \frac{x}{\lambda}\right)\right)$$

alebo ekvivalentne:

$$y = y_m \cdot \sin\!\left(2\pi\!\left(ft - \frac{x}{\lambda}\right)\right)$$

- `y_m` = amplitúda (maximálna výchylka)
- `T` = perióda
- `f` = frekvencia
- `λ` = vlnová dĺžka
- `v` = rýchlosť šírenia
- znamienko `−` pred `x/λ` → vlna sa šíri v smere osi `+x`

> rovnica postupnej vlny je **funkcia 2 premenných** ⇒ `y = f(x, t)`

**Pre viacero vĺn (biacejúca vlna):**

$$y = y_m \cdot \sin\!\left(2\pi\!\left(\frac{t}{T} - \frac{x}{\lambda}\right)\right)_m$$

---

### Príklad 1

$$y = 4 \cdot 10^{-2} \cdot \sin\!\left[2\pi\!\left(8t - 5x\right)\right]\,\text{m}$$

Určiť: `y_m`, `T`, `λ`, `f`, `v`

$$y_m = 4 \cdot 10^{-2}\,\text{m}$$

$$8t = \frac{t}{T} \Rightarrow 8 = \frac{1}{T} \Rightarrow T = \frac{1}{8} = 0{,}125\,\text{s}$$

$$5x = \frac{x}{\lambda} \Rightarrow \lambda = \frac{1}{5}$$

$$f = 8\,\text{Hz}$$

$$\lambda = \frac{1}{5} = 0{,}2\,\text{m}$$

$$v = 1{,}6\,\text{m·s}^{-1}$$

Overenie: `λ = v · T` → `0,2 = v · 0,125` → `v = 1,6 m·s⁻¹` ✓

---

### Príklad 2

Od zdroja sa šíri vlna s `y_m = 10 cm`, `λ = 3 m` a `T = 2 s`. Vypočítaj výchylku bodu, ktorý je vzdialený `1,5 km` od vlnenia v čase `30 min` od vzniku vlnenia.

$$y = y_m \cdot \sin\!\left[2\pi\!\left(\frac{t}{T} - \frac{x}{\lambda}\right)\right]$$

$$y_m = 10\,\text{cm} = 0{,}1\,\text{m},\quad \lambda = 3\,\text{m},\quad T = 2\,\text{s}$$

$$t = 30\,\text{min} = 1800\,\text{s},\quad x = 1{,}5\,\text{km} = 1500\,\text{m}$$

$$y = 0{,}1 \cdot \sin\!\left[2\pi\!\left(\frac{1800}{2} - \frac{1500}{3}\right)\right] = \underline{0\,\text{m}}$$

---

### Príklad 3

Zapíšte rovnicu. `f = 1 kHz`, `y_m = 3 mm`, `v = 340 m·s⁻¹`. Vektor rýchlosti šírenia je orientovaný nesúhlasne s kladnou osou `x`.

$$f = 1\,\text{kHz} = 1 \cdot 10^3\,\text{Hz} \Rightarrow T = 1 \cdot 10^{-3}\,\text{s}$$

$$y_m = 3\,\text{mm} = 0{,}003\,\text{m}$$

$$v = 340\,\text{m·s}^{-1}$$

$$y = 0{,}003 \cdot \sin\!\left[2\pi\!\left(\frac{t}{1 \cdot 10^{-3}} - \frac{x}{-340 \cdot 1 \cdot 10^{-3}}\right)\right]$$

*(znamienko pri x záporné — vlna sa šíri v smere −x)*

---

### Príklad 4

Anej m od rovnakej polohy je bod vlnenia k.t. v čase `(1/6)T` je od zdroja vzdialený `(λ/12)x`, `y_m = 5 cm`.

$$d = \frac{1}{6}T,\quad x = \frac{\lambda}{12}$$

$$y_m = \frac{5}{2}\,\text{cm} = 0{,}025\,\text{m}$$

$$y = y_m \cdot \sin\!\left(2\pi\!\left[\frac{t}{T} - \frac{x}{\lambda}\right]\right)$$

$$y = 0{,}05 \cdot \sin\!\left(2\pi\!\left[\frac{\frac{1}{6}T}{T} - \frac{\frac{1}{12}\lambda}{\lambda}\right]\right) = y = 0{,}05 \cdot \sin\!\left(2\pi\!\left[\frac{1}{6} - \frac{1}{12}\right]\right)$$

$$\underline{y = 2{,}5\,\text{cm}}$$

---

## Interferencia

- **skladanie vlnenia** — na miestach kde súčasne prebieha viacero vlnení nastáva skladanie vlnení, tzv. **interferencia vlnení**

**Princíp superpozície:**
- ak teleso súčasne koná niekoľko harmonických pohybov, rovnakého smeru, s okamžitými výchylkami `y₁, y₂, y₃, ..., yₙ`, je okamžitá výchylka výsledného kmitania:

$$y_v = y_1 + y_2 + \cdots + y_n$$

### 1. Vlny s rovnakou fázou sa skladajú (zosilnenie)

- `d = 0` → vlny kmitajú súfázovo → zosilnenie
- `d = 2·(λ/2)` = `λ`

**Zosilnenie vlnenia:**

$$\boxed{d = 2k \cdot \frac{\lambda}{2},\quad k = 0, 1, 2, \ldots}$$

- keď sa dráhový rozdiel interferujúcich vlnení rovná **párnemu** počtu polvĺn → nastáva **zosilnenie vlnenia**

### 2. Interferencia vlnení s opačnou fázou (zoslabenie)

$$\boxed{d = (2k+1) \cdot \frac{\lambda}{2},\quad k = 0, 1, 2, \ldots}$$

- keď sa dráhový rozdiel interferenčných vlnení rovná **nepárnemu** počtu polvĺn → nastáva **zoslabenie vlnenia**

---

### Príklad — graficky, zobraziť ak `y_m1 = 3 cm` a `y_m2 = 2 cm`

**a) d = λ/2:**

$$\vec{y_v} = \vec{y_1} + \vec{y_2};\quad y_{v0} = 3 - 2 = 1\,\text{cm}$$

*(vlny protifázové — zoslabenie)*

**b) d = 2·(λ/2):**

$$\vec{y_v} = \vec{y_1} + \vec{y_2};\quad y_{v0} = 3 + 2 = 5\,\text{cm}$$

*(vlny súfázové — zosilnenie)*

---

## Fázový rozdiel

$$\boxed{\Delta\varphi = \varphi_1 - \varphi_2 = 2\pi \cdot \frac{d}{\lambda}}$$

kde `d` = vzdialenosť (dráhový rozdiel) medzi dvoma bodmi vlny.

- `Δφ = 2π·k` → body kmitajú **súfázovo**
- `Δφ = (2k+1)·π` → body kmitajú **protifázovo**

Fázový rozdiel:

$$\Delta\varphi = \left|2\pi\!\left(\frac{t}{T} - \frac{x_1}{\lambda}\right) - 2\pi\!\left(\frac{t}{T} - \frac{x_2}{\lambda}\right)\right| = \left|2\pi \cdot \frac{x_2 - x_1}{\lambda}\right| = 2\pi \cdot \frac{d}{\lambda}$$

$$\boxed{\Delta\varphi = \varphi_1 - \varphi_2;\quad \Delta\varphi = 2\pi \cdot \frac{x_2 - x_1}{\lambda} = 2\pi \cdot \frac{d}{\lambda}}$$

### Príklad 5

Vlna s frekvenciou `600 Hz` a rýchlosťou `340 m·s⁻¹`. Určte fázový rozdiel medzi dvoma bodmi vzdialeným:

**a) 0,17 m:**

$$\Delta\varphi = 2\pi \cdot \frac{x_2 - x_1}{\lambda} = 2\pi \cdot \frac{0{,}17}{\lambda} = 2\pi \cdot \frac{0{,}17}{\frac{340}{600}} = \underline{0{,}6\pi}$$

**b) 1,7 m:**

$$\Delta\varphi = 2\pi \cdot \frac{1{,}7}{\frac{340}{600}} = 6\pi$$

---

### Príklad 6 — Vypočítaj fázový rozdiel

*(z grafu: `x = 10`, `d = 4`)*

$$\Delta\varphi = 2\pi \cdot \frac{x_2 - x_1}{\lambda} = 2\pi \cdot \frac{4 - 0}{10} = \frac{4}{5}\pi$$

---

## Šírenie vlnenia v prostredí

### Huygensov princíp

- každý bod vlnoplochy, do kt. vlnenie v danom okamihu dospeje, môžeme považovať za zdroj elementárneho vlnenia
- výsledná vlnoplocha je vonkajšia obalová plocha všetkých elementárnych vlnoplôch rovnakého tvaru
- všetky body vlnoplochy kmitajú s rovnakou fázou — holmice na vlnoplochu
- lúče určujú smer šírenia vlnenia — holmice na vlnoplochu
- `v = v` — parameter vlnoplôch

### Ak vlnenie dopadne na rozhranie 2 prostredí

*(diagram: dopadajúci lúč, odrazený lúč, lomený lúč, uhol dopadu, uhol odrazu, uhol lomu)*

#### Zákon odrazu

$$\text{uhol dopadu} = \text{uhol odrazu} \Rightarrow \alpha = \alpha'$$

#### Zákon lomu — Snellov zákon

$$\boxed{\frac{\sin\alpha}{\sin\beta} = \frac{v_1}{v_2} = n_{12}} \quad \leftarrow \text{relatívny index lomu}$$

- **lom ku kolmici** (`β < α`): `v₂ < v₁`
- **lom od kolmice** (`β > α`): `v₂ > v₁`

### Príklad 7

`v₁ = 340 m·s⁻¹`, `v₂ = 1450 m·s⁻¹`, `β = 45°`, `α = ?`

$$\frac{\sin\alpha}{\sin 45°} = \frac{340}{1450}$$

$$\sin\alpha = \frac{340}{1450} \cdot \sin(45°) = 0{,}1658$$

$$\underline{\alpha = 9{,}54°}$$

---

### Kritický uhol — úplný odraz

- `α_m` — najmenší uhol dopadu, pri ktorom lúč ide po hranici
- platí: `sin(α_m) / sin(90°) = v₁ / v₂`

$$\boxed{\sin\alpha_m = \frac{v_1}{v_2}}$$

- lom ku kolmici: `β < α` → `v₂ < v₁`
- lom od kolmice: `β > α` → `v₂ > v₁`

### Príklad 8

Pod akým najväčším uhlom môže dopadnúť zvuková vlna aby prenikla do vody?

`v₁ = 340 m·s⁻¹`, `v₂ = 1450 m·s⁻¹`, `α_m = ?`

$$\sin(\alpha_m) = \frac{v_1}{v_2} = \frac{340}{1450}$$

$$\underline{\alpha_m \approx 13{,}56°}$$

$$\alpha < \alpha_m \Rightarrow \alpha < 13{,}56°$$

---

### Ohyb vlnenia — difrakcia

- vlnenie vstupuje do oblasti v tieni prekážky — za prekážku s vlnovou dĺžkou porovnateľnou s rozmermi prekážky
- aby nastal ohyb, musia byť rozmery prekážky porovnateľné s vlnovou dĺžkou vlnenia

*(diagram: vlnoplochy sa ohýbajú za okrajmi prekážky)*

---

## Stojaté vlnenie

- stojaté vlnenie vzniká interferenciou — skladaním priamej a odrazenej vlny
- vznikajú **kmitne** a **uzly**
  - **kmitňa** — bod s najväčším pohybom (maximálna amplitúda)
  - **uzol** — bod bez pohybu

- ak je koniec bodu pevný → nastáva odraz s opačnou fázou → **uzol**
- ak je rad bodov na konci voľný → odráža sa s rovnakou fázou → **kmitňa**

*(diagram: stojatá vlna s uzlami a kmitňami, pevný a voľný koniec)*

- body kmitajúce s max. amplitúdou sú **kmitne**
- body kmitajúce s 0 amplitúdou sú **uzly**
- vzdialenosť 2 susedných kmitní a 2 susedných uzlov je `λ/2`
- vzdialenosť najbližších kmitní a uzlov je `λ/4`

### Základná frekvencia stojatého vlnenia `f₀` (1 kmitňa)

$$l = \frac{1}{2}\lambda \Rightarrow \lambda = 2l$$

$$\boxed{f_0 = \frac{v}{2l}}$$

### Vyššie harmonické frekvencie

- 1 kmitňa, 2 kmitne: `l = (2/2)λ` → 2 kmitne
- 3 kmitne: `l = (3/2)λ`

$$\boxed{f_k = k \cdot f_0,\quad k = 2, 3, 4, 5, \ldots}$$

kde `k` = počet kmitní.
