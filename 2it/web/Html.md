- `<p> Contents </p>` - paragraph
- `<body><p>Contents </p></body>` - puts a paragraph into the body element
	- important - ==almost everything goes inside==
	- each line has to be in a different `<p> </p>`
		- `<body> <p> Line 1` 
				    `Line 2 </p>`
			`<body/>`
			- doesnt work
		-  `<body> <p> Line 1 </p>
				 `<p> Line 2 </p>`
			`<body/>`
			- works
- `<h1> heading </h1>` - headings
	- ==it goes inside the body==
	- from h1 to h6
		- ![HTML headings sizes comparison](https://www.codedex.io/images/html/html-headings.png)
- `<br>` - line break inside a paragraph
	- doesnt need a closing tag (`</tag>`)
- `<b>` element to **bold** text.
- `<i>` element to _italicize_ text.
- `<u>` element to underline text.
- `<s>` element to ~~strikethrough~~ text.
- `<ul>` Unordered lists
	- bullet points
	- element - for each item inside we need `<li>`
```html
<ul>
  <li>item 1<li>
  <li>item 2<li>
  <li>item 3</li>
</ul>
```
- `<ol>` Ordered lists
	- numbered lists
	- element - for each item inside we need `<li>`
```html
<ol>
  <li>item 1<li>
  <li>item 2<li>
  <li>item 3</li>
</ol>
```
- `<a href="https://website.com">website</a>` - anchor element - hyprlinks
	- href - hyprlink reference
	- there are other anchor variants:
		- `<a href="mailto:email@gmail.com">📧</a>`
		- `<a href="tel:212-555-2368">🤙</a>`
		- `<a href="sms:320-250-HTML">💬</a>`
- `<img src="https://i.redd.it/5unn16axx1v81.jpg">` - image tag - makes images
	- src - source
	- "link" - is the source

## Related
- [[html-inline-vs-block]]
- [[html-span]]
- [[html-aside]]
- [[html-main]]
- [[js]]
- [[single-page-applications]]