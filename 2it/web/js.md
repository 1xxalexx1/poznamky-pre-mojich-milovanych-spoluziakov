# JavaScript – cvicenie 4 notes

---

## Basics (commented-out examples at the top of script.js)

### alert
```js
alert("Medved");
```
Pops up a browser dialog box with a message. Useful for quick debugging, but annoying in real apps.

---

### Variables – `let` and `const`
```js
let polomer = 5;   // can be reassigned later
const cislo = 4;   // cannot be reassigned
var nieco = 4;     // global scope - whole file
```
- `let` – block-scoped variable, value can change.
- `const` – block-scoped constant, value is fixed after assignment.
- `var` is the old way (avoid it – has confusing scoping rules).

---

### Math object
```js
Math.pow(polomer, 2)  // polomer squared (polomer²)
Math.PI               // 3.14159...
Math.floor(x)         // rounds DOWN to nearest integer
Math.random()         // random decimal: 0 ≤ x < 1
```

---

### console.log – three string styles
```js
console.log("Vysledok je " + vys);   // double quotes + concatenation
console.log('Vysledok je ' + vys);   // single quotes – same thing
console.log(`Vysledok je ${vys}`);   // template literal – embed variables with ${}
```
Template literals (backtick strings) are the modern, preferred way when you need to insert a variable into text.

---

### if / else if / else
```js
if (cislo > 0) console.log(`cislo ${cislo} je kladne`);
else if (cislo < 0) console.log(`cislo ${cislo} je zaporne`);
else console.log(`cislo je 0`);
```
Braces `{}` are optional for single-line bodies, but usually good practice to include them.

---

## DOM – selecting elements

```js
const vstup   = document.querySelector("#vstup");
const body    = document.querySelector("body");
const polomer = document.querySelector("#polomer");
const vypis   = document.querySelector("#vypocetKruhu");
```
`document.querySelector(selector)` returns the **first** element matching a CSS selector.
- `"#id"` selects by id
- `"body"` selects the tag
- `".class"` selects by class

---

## DOM – changing styles from JS

```js
vstup.style.color = "red";
body.style.backgroundColor = `rgb(${r}, ${g}, ${b})`;
body.style.backgroundColor = `hsl(${h}, 50%, 50%)`;
```
Every CSS property is available on `.style`, but written in camelCase (`background-color` → `backgroundColor`).

---

## DOM – reading input values

```js
vstup.value     // text currently typed in the #vstup input
polomer.value   // text currently typed in the #polomer input (comes as a string!)
```

---

## DOM – writing to an element

```js
vypis.innerHTML = `obsah je ${obsah}`;
```
Sets the HTML content of the element. Use `.textContent` instead if you don't need HTML tags.

---

## Functions

```js
function aplikujZmenu() {
    console.log(`Dobry den, ${vstup.value}`);
}
```
Reads the value from the text input and logs a greeting. Called from the HTML `onchange` event.

```js
function obsah() {
    let obsah = Math.pow(polomer.value, 2) * Math.PI;
    vypis.innerHTML = `obsah je ${obsah}`;
}
```
Calculates the area of a circle (π·r²) from the input and displays it in the `<p>` element.

```js
function zmenFarbu() {
    const r = Math.floor(Math.random() * 256);
    const g = Math.floor(Math.random() * 256);
    const b = Math.floor(Math.random() * 256);
    body.style.backgroundColor = `rgb(${r}, ${g}, ${b})`;
}
```
Picks three random integers 0–255 and applies them as an RGB background color.

```js
let h = 0;
function zmenFarbuPlynulo() {
    h += 10;
    body.style.backgroundColor = `hsl(${h}, 50%, 50%)`;
}
```
Uses **HSL** color (Hue, Saturation, Lightness). Each call shifts the hue by 10°, cycling smoothly through the color wheel.

---

## Timers – setInterval / clearInterval

```js
let casovac = null;

function autozmena() {
    if (casovac === null) {
        casovac = setInterval(zmenFarbu, 17);   // start: call zmenFarbu every 17 ms
    } else {
        clearInterval(casovac);                  // stop
        casovac = null;
    }
}
```
- `setInterval(fn, ms)` – calls `fn` repeatedly every `ms` milliseconds. Returns a timer ID.
- `clearInterval(id)` – cancels the interval.
- 17 ms ≈ 60 fps (frames per second), which is smooth animation speed.
- The `casovac` variable acts as an on/off toggle: `null` = stopped, anything else = running.

`plynulazmena()` works exactly the same way but calls `zmenFarbuPlynulo` instead.

---

## HTML – events

```html
<input type="text" onchange="aplikujZmenu()" id="vstup">
<input type="text" onchange="obsah()"        id="polomer">
<button onclick="zmenFarbu()">zmena farby</button>
<button onclick="autozmena()">Auto-zmena farby</button>
<button onclick="plynulazmena()">Auto-zmena plynula</button>
<p id="vypocetKruhu">nieco</p>
```
- `onchange` fires when the user changes the input value and moves focus away.
- `onclick` fires when the button is clicked.
- The JS file is linked at the **bottom** of `<body>` so the HTML elements exist before the script runs.

---

## Quick reference table

| Concept | Syntax |
|---|---|
| Select element | `document.querySelector("#id")` |
| Read input value | `element.value` |
| Change style | `element.style.propertyName = "value"` |
| Write to element | `element.innerHTML = "..."` |
| Template literal | `` `text ${variable} text` `` |
| Random integer 0–255 | `Math.floor(Math.random() * 256)` |
| Repeat function | `setInterval(fn, ms)` |
| Stop repeating | `clearInterval(id)` |

## Related
- [[Html]]
- [[single-page-applications]]
- [[portfolio]]
