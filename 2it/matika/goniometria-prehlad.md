# Goniometria – rýchly prehľad pred testom

---

## 1. Základné vzťahy medzi goniometrickými funkciami

### Základná identita (Pytagorova veta na jednotkovej kružnici)
$$\sin^2 x + \cos^2 x = 1$$

Odvodené vzťahy:
- $\sin^2 x = 1 - \cos^2 x \quad \Rightarrow \quad |\sin x| = \sqrt{1-\cos^2 x}$
- $\cos^2 x = 1 - \sin^2 x \quad \Rightarrow \quad |\cos x| = \sqrt{1-\sin^2 x}$

### Tangens a kotangens
$$\operatorname{tg} x = \frac{\sin x}{\cos x} \ (\cos x \neq 0), \qquad \operatorname{cotg} x = \frac{\cos x}{\sin x} \ (\sin x \neq 0)$$
$$\operatorname{tg} x \cdot \operatorname{cotg} x = 1 \quad \Rightarrow \quad \operatorname{tg} x = \frac{1}{\operatorname{cotg} x}, \quad \operatorname{cotg} x = \frac{1}{\operatorname{tg} x}$$

### Vzorce dvojnásobného uhla
$$\sin(2x) = 2\sin x \cos x$$
$$\cos(2x) = \cos^2 x - \sin^2 x \quad (= 2\cos^2 x - 1 = 1 - 2\sin^2 x)$$

### Tabuľka základných hodnôt
| x     | 0   | π/6  | π/4  | π/3  | π/2 |
| ----- | --- | ---- | ---- | ---- | --- |
| sin x | 0   | 1/2  | √2/2 | √3/2 | 1   |
| cos x | 1   | √3/2 | √2/2 | 1/2  | 0   |
| tg x  | 0   | √3/3 | 1    | √3   | –   |

### Znamienka funkcií podľa kvadrantu
| Kvadrant | interval | sin | cos | tg | cotg |
|---|---|---|---|---|---|
| I. | (0, π/2) | + | + | + | + |
| II. | (π/2, π) | + | – | – | – |
| III. | (π, 3π/2) | – | – | + | + |
| IV. | (3π/2, 2π) | – | + | – | – |

### Postup A – výpočet zvyšných funkcií z jednej zadanej hodnoty
1. Pomocou $\sin^2x+\cos^2x=1$ vypočítaj **absolútnu hodnotu** druhej funkcie.
2. Z **intervalu/kvadrantu** urči, aké má znamienko.
3. $\operatorname{tg} x = \sin x / \cos x$, $\operatorname{cotg} x = \cos x/\sin x$ (alebo $1/\operatorname{tg} x$).

**Vzorový príklad:** $\sin x = \tfrac{2}{5}$, $x \in (\tfrac{\pi}{2}; \pi)$ → II. kvadrant ⇒ cos x < 0

$$\cos x = -\sqrt{1-\left(\tfrac{2}{5}\right)^2} = -\sqrt{\tfrac{21}{25}} = -\frac{\sqrt{21}}{5}$$
$$\operatorname{tg} x = \frac{2/5}{-\sqrt{21}/5} = -\frac{2}{\sqrt{21}} = -\frac{2\sqrt{21}}{21}, \qquad \operatorname{cotg} x = -\frac{\sqrt{21}}{2}$$

### Postup B – zjednodušovanie výrazov
- Hľadaj, kde sa dá použiť $\sin^2x+\cos^2x=1$, rozdiel štvorcov $a^2-b^2=(a-b)(a+b)$, vzorce pre $2x$.
- **Vždy** na koniec napíš podmienky (čo nesmie byť rovné nule v menovateli).

**Vzorový príklad:**
$$\frac{\cos^2 x}{1+\sin x} = \frac{1-\sin^2x}{1+\sin x} = \frac{(1+\sin x)(1-\sin x)}{1+\sin x} = 1-\sin x$$
*Podmienka:* $1+\sin x \neq 0 \Rightarrow \sin x \neq -1 \Rightarrow x \neq \tfrac{3\pi}{2}+2k\pi,\ k\in\mathbb{Z}$

---

## 2. Sínusová a kosinúsová veta

Pre $\triangle ABC$ so stranami $a,b,c$ a uhlami $\alpha,\beta,\gamma$ platí:
$$\alpha + \beta + \gamma = 180°$$

### Sínusová veta
$$\frac{a}{\sin\alpha} = \frac{b}{\sin\beta} = \frac{c}{\sin\gamma} = 2r$$

- **Kedy použiť:** keď poznáš jednu dvojicu *uhol – protiľahlá strana* a ešte jeden ďalší údaj (uhol alebo stranu).
- ⚠️ Pri výpočte **uhla** zo sínusovej vety môže vyjsť **2 riešenia** – obe je potrebné overiť (napr. súčtom uhlov = 180°).

### Kosinúsová veta
$$a^2 = b^2+c^2-2bc\cos\alpha$$
$$b^2 = a^2+c^2-2ac\cos\beta$$
$$c^2 = a^2+b^2-2ab\cos\gamma$$

- **Kedy použiť:**
  1. poznáme **2 strany a uhol nimi zovretý** (SUS),
  2. poznáme **všetky 3 strany** (SSS).

### Postup riešenia trojuholníka
1. Zisti, čo je zadané (SSS / SUS / USU / SSU).
2. Vyber vhodnú vetu (cos veta pri SSS/SUS, inak sin veta).
3. Doplň zvyšné strany/uhly – kombinuj s $\alpha+\beta+\gamma=180°$.

**Vzorový príklad:** $b=48{,}55\text{ cm}$, $\alpha=69°40'$, $\gamma=6°30'$
$$\beta = 180° - (\alpha+\gamma) = 180° - 76°10' = 103°50'$$
$$a = \frac{b\sin\alpha}{\sin\beta} \approx 46{,}88\text{ cm}, \qquad c = \frac{b\sin\gamma}{\sin\beta} \approx 5{,}66\text{ cm}$$

---

## 3. Zložitejšie goniometrické rovnice

### Univerzálny postup
1. **Substitúcia** – celý argument nahraď premennou $a$ (napr. $a = 3x$, $a = x-\tfrac{3\pi}{4}$).
2. **Vyrieš jednoduchú rovnicu** $\sin a = k$ / $\cos a = k$ / $\operatorname{tg} a = k$ pomocou jednotkovej kružnice – nájdi **všetky** riešenia v $[0,2\pi)$ a priprav periodicitu.
3. **Spätná substitúcia** – vyrieš pre $x$.
4. **Pozor na koeficient!** Ak $a = 3x$, perióda sa pri prevode na $x$ vydelí 3 (z $2\pi$ na $\tfrac{2\pi}{3}$).
5. **Podmienky** – ak sa v rovnici vyskytuje $\operatorname{tg}$/$\operatorname{cotg}$ alebo zlomok, nezabudni doplniť $D = \mathbb{R}\setminus\{...\}$.

### Periodicita
- $\sin a = k$, $\cos a = k$ → $+2k\pi,\ k\in\mathbb{Z}$ (zvyčajne 2 rodiny riešení)
- $\operatorname{tg} a = k$, $\operatorname{cotg} a = k$ → $+k\pi,\ k\in\mathbb{Z}$ (1 rodina riešení)

### Vzorový príklad 1 – substitúcia + zmena periódy
$$\cos(3x) = -\frac{\sqrt2}{2}$$
sub: $a=3x$ → $\cos a = -\tfrac{\sqrt2}{2}$ → $a_1 = \tfrac{3\pi}{4}+2k\pi$, $a_2=\tfrac{5\pi}{4}+2k\pi$

$$3x_1 = \tfrac{3\pi}{4}+2k\pi \;\Rightarrow\; x_1 = \tfrac{\pi}{4}+k\tfrac{2\pi}{3}$$
$$3x_2 = \tfrac{5\pi}{4}+2k\pi \;\Rightarrow\; x_2 = \tfrac{5\pi}{12}+k\tfrac{2\pi}{3}, \qquad k\in\mathbb{Z}$$

➡️ **Toto je najčastejšia chyba** – nezabudni vydeliť periódu rovnakým číslom ako argument.

### Vzorový príklad 2 – kvadratická substitúcia
$$2\cos^2x - 7\cos x + 3 = 0$$
sub: $a=\cos x$ → $2a^2-7a+3=0$ → $a = \dfrac{7\pm5}{4}$ → $a_1=3$, $a_2=\tfrac{1}{2}$

- $\cos x = 3$ → **nemožné** ($|\cos x|\leq1$, zahodiť!)
- $\cos x = \tfrac{1}{2}$ → $x = \tfrac{\pi}{3}+2k\pi \ \lor\ x = -\tfrac{\pi}{3}+2k\pi,\ k\in\mathbb{Z}$

➡️ Po kvadratickej substitúcii **vždy** over, či korene patria do $[-1,1]$ (pre sin/cos).

### Postup C – Homogénne rovnice (zmiešané $\sin^2x$, $\cos^2x$, $\sin x\cos x$)
Rovnica, kde sú všetky členy "rovnakého stupňa" (napr. $a\sin^2x+b\sin x\cos x+c\cos^2x=d$):

1. Ak $d\neq0$, prepíš $d = d\cdot(\sin^2x+\cos^2x)$, aby bola rovnica homogénna (všetko na jednej strane = 0).
2. **Over, či $\cos x=0$ je riešením** – dosaď priamo (vtedy $\sin x=\pm1$).
3. Ak $\cos x\neq0$ nie je riešením, vydeľ celú rovnicu $\cos^2x$ → vznikne kvadratická rovnica v $\operatorname{tg}x$.
4. Vyrieš kvadratickú rovnicu pre $\operatorname{tg}x$, potom $x=\arctan(...) + k\pi$.

**Príklad:** $\sin^2x-6\cos^2x+\sin x\cos x=0$
- $\cos x=0 \Rightarrow \sin^2x=1\neq0$ → nie je riešenie, môžeme deliť $\cos^2x$:
$$\operatorname{tg}^2x+\operatorname{tg}x-6=0 \;\Rightarrow\; (\operatorname{tg}x+3)(\operatorname{tg}x-2)=0$$
$$\operatorname{tg}x=-3 \ \lor\ \operatorname{tg}x=2$$

### Postup D – Rovnice/výrazy kombinujúce $x$ a $2x$
Ak sa v rovnici objaví aj $\sin x,\cos x$ aj $\sin2x,\cos2x$ spolu, prepíš všetko cez $x$:
$$\sin2x=2\sin x\cos x, \qquad \cos2x=\cos^2x-\sin^2x=1-2\sin^2x=2\cos^2x-1$$

**Príklad:** $\sin x+\sin2x=0$
$$\sin x+2\sin x\cos x=0 \;\Rightarrow\; \sin x(1+2\cos x)=0 \;\Rightarrow\; \sin x=0 \ \lor\ \cos x=-\tfrac12$$

**Príklad:** $(\sin x+\cos x)^2=1$
$$\sin^2x+2\sin x\cos x+\cos^2x=1 \;\Rightarrow\; 1+\sin2x=1 \;\Rightarrow\; \sin2x=0$$

### Postup E – Rovnice s $\operatorname{tg}$ a $\operatorname{cotg}$ (substitúcia)
Na rozdiel od $\sin$/$\cos$, rovnice $\operatorname{tg}\,a=k$ a $\operatorname{cotg}\,a=k$ majú **len JEDNU rodinu riešení**, s periódou $\pi$ (nie $2\pi$, a nie dve rodiny):
$$\operatorname{tg}\,a=k \ \lor\ \operatorname{cotg}\,a=k \quad\Rightarrow\quad a=a_0+k\pi,\ k\in\mathbb{Z}$$
$a_0$ je referenčný uhol – pre kladné $k$ z I. kvadrantu, pre záporné $k$ z II. kvadrantu (jeden stačí, druhý je od neho vzdialený presne o $\pi$, čo už pokrýva $+k\pi$).

**Príklad:** $\operatorname{cotg}\left(\frac{\pi}{6}-x\right)=\frac{\sqrt3}{3}$
sub: $a=\frac{\pi}{6}-x$ → $\operatorname{cotg}\,a=\frac{\sqrt3}{3}$ → $a_0=\frac{\pi}{3}$ (pretože $\operatorname{cotg}\frac{\pi}{3}=\frac{\sqrt3}{3}$, kladná hodnota → I. kvadrant)
$$a=\frac{\pi}{3}+k\pi \;\Rightarrow\; \frac{\pi}{6}-x=\frac{\pi}{3}+k\pi \;\Rightarrow\; x=-\frac{\pi}{6}-k\pi=-\frac{\pi}{6}+k\pi,\ k\in\mathbb{Z}$$

### Ďalšie typické triky
- **Rovnica typu $f(x)\cdot g(x)=0$** → rieš každý faktor osamote (napr. $\sin x(2\cos x-\sqrt3)=0$).
- **Rovnice s $\operatorname{tg}$** – prevod na $\sin/\cos$, vynásobenie $\cos x$ → nezabudni podmienku $\cos x\neq0$.
- **Substitúcia so znamienkom mínus** (napr. $a=\tfrac{\pi}{4}-2x$) – pri prevode "$-k$" na "$+k$" sa nič nemení, pretože $k$ prebieha celé $\mathbb{Z}$ (kladné aj záporné).

---

## Pred testom – rýchla kontrola
- [ ] Vieš naspamäť všetkých 5 základných vzťahov z bodu 1?
- [ ] Vieš bez rozmýšľania povedať znamienka sin/cos/tg/cotg vo všetkých 4 kvadrantoch?
- [ ] Vieš rozlíšiť, kedy použiť sin vetu a kedy cos vetu?
- [ ] Vieš vysvetliť, prečo sa pri $\cos(3x)$ perióda vydelí tromi?
- [ ] Nezabúdaš na podmienky pri každom príklade?
