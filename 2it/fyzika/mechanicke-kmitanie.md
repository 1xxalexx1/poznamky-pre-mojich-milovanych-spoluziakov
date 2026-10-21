# Mechanické kmitanie

## Základné pojmy

- **Mechanické kmitanie** – periodický pohyb, pri ktorom teleso pravidelne prechádza rovnovážnou polohou
- **Mechanický oscilátor** – zariadenie, ktoré môže kmitať bez vonkajšieho pôsobenia (napr. teleso na pružine)
- **Časový diagram** – grafická závislosť okamžitej polohy od času _t_
- **Harmonický pohyb** – pohyb, ktorého časový diagram je sínusoida, tiež nazývaný jednoduchí kmitavý pohyb
- **ω** – uhlová frekvencia (alebo uhlová rýchlosť)

---

## Rovnica harmonického pohybu (rovnica pre okamžitú výchylku)

$$y = y_m \cdot \sin(\omega t ± \varphi_0)$$
kde:

- **y** – okamžitá výchylka
- **y_m** – maximálna výchylka (amplitúda)
- **φ = ωt + φ₀** – fáza harmonického pohybu
- **ω = 2π / T = 2πf**– uhlová frekvencia
- **φ₀** – začiatočná fáza
- **T** – perióda kmitania
- t - čas


$$\sin \varphi = \frac{y}{y_m}$$ $$\omega = \frac{\varphi}{t}$$
### Ďalšie veličiny

- **Frekvencia:** f = 1 / T
- **Perióda:** T = 1 / f

--- 
## Rýchlosť a zrýchlenie 
- časový diagram: *(y – sínusoida, v – kosínusoida, a – záporná sínusoida; všetky tri krivky sú fázovo posunuté)* $$y = y_{max} \cdot \sin(2\pi f t)$$ $$v = v_{max} \cdot \cos(2\pi f t)$$ $$a = a_{max} \cdot \sin(2\pi f t)$$
- ==**a** → najväčšia, najmenší rozdiel kmitov== ?
---
## Rýchlosť a zrýchlenie harmonického pohybu

### Okamžitá rýchlosť

$$v = y_m \cdot \omega \cdot \cos(\omega t + \varphi_0)$$

- maximálna rýchlosť: **v_max = y_m · ω**

### Okamžité zrýchlenie

$$a = -y_m \cdot \omega^2 \cdot \sin(\omega t + \varphi_0)$$

- maximálne zrýchlenie: **a_max = y_m · ω²**

### Fázový diagram

- výchylka _y_, rýchlosť _v_ a zrýchlenie _a_ sú navzájom fázovo posunuté
- rýchlosť predbieha výchylku o π/2
- zrýchlenie predbieha výchylku o π (je v protifáze s výchylkou)

--- 
## Kľúčové vzťahy 
$$v = \omega \cdot r$$ $$v_{max} = \omega \cdot y_m$$ $$a_m = \omega^2 \cdot y_m$$
## Súhrnné rovnice 
$$y = y_m \cdot \sin(\omega t + \varphi_0)$$ $$v = y_m \cdot \omega \cdot \cos(\omega t + \varphi_0)$$ $$a = -y_m \cdot \omega^2 \cdot \sin(\omega t + \varphi_0)$$

---

## Dynamika kmitavého pohybu

V rovnovážnej polohe: **F_V = 0 N**

Celková sila pôsobiaca na teleso:

$$F = F_g + F_p$$

kde:

- **F_g** – tiažová sila
- **F_p** – sila pružiny

Výsledná sila:

$$F_v = -k \cdot y$$

- **F_v = -k · y_m · sin(ωt + φ₀)**
- **F_v_max = -k · y_m**

Pohybová rovnica:

$$F_v = m \cdot a$$ $$-k \cdot y = m \cdot a$$

**Harmonický pohyb mechanického oscilátora je spôsobený silou, ktorá stále smeruje do rovnovážnej polohy a je priamo úmerná okamžitej výchylke.**



## Dynamika kmitavého pohybu 
$$\vec{F_v} = \vec{F_G} + \vec{F_p}$$ V rovnovážnej polohe: **F_v = 0 N** *(Schéma: teleso na pružine – v rovnovážnej polohe pôsobí F_p smerom hore a F_G smerom dole, pružina je predĺžená o Δl)* 
### Sily pôsobiace na teleso 
$$F_G = m \cdot g$$ 
$$\Delta l = l - l_0$$
___
$$F_p = k \cdot (l - l_0)$$
$$F_p = k \cdot \Delta l$$
kde **k** = tuhosť pružiny 
### Rovnovážna poloha 
$$F_G = F_p$$
$$m \cdot g = k \cdot \Delta l$$ 
### Výsledná sila pri výchylke y 
*(Keď je teleso vychýlené o y pod rovnovážnu polohu – F_v smeruje hore, F_p smeruje dole, F_G smeruje dole)* 
$$F_v = m \cdot g - k \cdot (\Delta l + y)$$ $$F_v = (m \cdot g - k \cdot \Delta l) - k \cdot y$$ Keďže $m \cdot g = k \cdot \Delta l$, zátvorka sa rovná nule: 
$$\boxed{F_v = -k \cdot y}$$
- **Harmonický pohyb mechanického oscilátora je spôsobený silou, ktorá stále smeruje do rovnovážnej polohy a je priamo úmerná okamžitej výchylke.** 
### Časový diagram y a F_v 
*(Graf: os x – čas s hodnotami T/4, T/2, 3T/4, T; y a F_v sú v protifáze)* $$y = y_m \cdot \sin(\omega t)$$ $$F_v = -k \cdot y_m \cdot \sin(\omega t)$$ $$F_{v,m} = -k \cdot y_m$$

---

## Vlastné kmitanie oscilátora

- kmitanie bez vplyvu vonkajších síl
- perióda a frekvencia závisí od parametrov oscilátora – tuhosť pružiny, hmotnosť telesa

Z pohybovej rovnice:

$$k \cdot y = m \cdot \omega^2 \cdot y$$ $$\omega = \sqrt{\frac{k}{m}}$$

### Perióda vlastného kmitania

$$T = 2\pi \cdot \sqrt{\frac{m}{k}}$$

### Frekvencia vlastného kmitania

$$f = \frac{1}{2\pi} \cdot \sqrt{\frac{k}{m}}$$
---
## Kyvadlo
 
$$F_v = \frac{y}{l} \cdot m \cdot g$$
 
$$T = 2\pi \sqrt{\frac{l}{g}}$$ $$f = \frac{1}{2\pi} \sqrt{\frac{g}{l}}$$
 
- **l** – dĺžka kyvadla, **g** – gravitačné zrýchlenie
- perióda kyvadla nezávisí od hmotnosti telesa
____
## Energia mechanického kmitania
 
- rovnovážna poloha: v = v_max, F_v = 0 N → **E_k = max**, **E_p = 0**
- krajná poloha: v = 0, y = y_m → **E_k = 0**, **E_p = max**
 
$$E_p = \frac{1}{2} k y^2$$
 
$$E_k = \frac{1}{2} m v^2 = \frac{1}{2} k \cdot y_m^2 \cdot \cos^2(\omega t + \varphi_0)$$
 
$$E_p = \frac{1}{2} k \cdot y_m^2 \cdot \sin^2(\omega t + \varphi_0)$$
 
$$\boxed{E = E_k + E_p = \frac{1}{2} k \cdot y_m^2}$$
 
*(využitie identity $\sin^2\varphi + \cos^2\varphi = 1$)*
 
$$y_m^2 = y^2 + \left(\frac{v}{\omega}\right)^2$$
---



