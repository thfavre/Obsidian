#CSS

# What is a Selector
![[Rules#Generality]]


# Selectors
## Universal `*  {`
Select everything.
```CSS 
* {
	color: pink; 
}
```

## Element `selector {` [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/Type_selectors)
Select all `name` of the page.
```CSS
button {
	color: pink;
}
```

## List `selector1, selector2 {`
Select all `h1` and `h2` of the page.
```CSS
h1, h2 {
	color: pink;
}
```

## ID  `#tagname {` [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/ID_selectors)
To style one thing differently.
An [[id]] is only used once!
```html
<button id="signup">Sign Up</button>
```
```CSS
#signup{
	background-color: blue;
}
```

## Class `.classname {` [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/Class_selectors)
To style lot's of things at once.
A [[class]] is usually used more than once.
![[class#^bfe65f]]
```CSS
.tag {
	background-color: pink;
}
```

^fa41ae

## Descendant `selector1 selector2 {`
Select all the `<a>`'s that are nested inside an `<li>` :
```CSS
li a {
	color: pink;
}
```
	The `li` are NOT selected
Select the `<a>` inside all `class="tag"`
```CSS
.tag a {
	color: pink;
}
```

## Adjacent (Combinator) `selector1 + selector2 {`
Select the `<button>` that are just after the `<h2>`
```html
<h2>Header 2 1!</h2>
<button>Button1!</button>

<h2>Header 2 2!</h2>
<button>Button2!</button>
```
```CSS
h2 + button {
	background-color: pink;
}
```

## Direct Child `selector1 > selector2 {`
Select  only the `<p>`'s that are **direct children** of a `<div>` element.
```html
<div>
	<p>Blabla</p>
</div>
```
```CSS
div > p {
	color: white;
}
```

## Attribute `selector[attribute="..."] {` [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/Attribute_selectors)
Select all input elements where the [[Elements#^a70f18|element]] type attribute is set to `"text"`
```html
<input type="text" placeholder="search!" id="search">
<input type="password" placeholder="password!" id="password">
```
```CSS
input[type="text"] {
	color: pink;
}
```

Select all section that have the `class="post"`
```html
<section class="post">
	...
</section>
```
```CSS
input[class="post"] {
	color: pink;
}
```
(same as `section.post`)

## Pseudo-Class `:` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/pseudo-classes)
Keyword added to a selector that specifies a special state of the selected element(s).
### `:over` [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/:hover)
```CSS
/* Selects any <a> element when "hovered" */
a:hover {
	color: pink;
}
```

### `:active` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:active) 
### `:checked` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked) 
### `:nth-of-type()` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-of-type) 
### `:active` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:active) 

## Pseudo-Elements `::` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/pseudo-elements)
Keyword added to a selector that lets you style a particular part of selected element(s).
For example to change the color of the first letter.
### `::first-letter` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-letter)
```CSS
h2::first-letter {
	font-size: 50px;
}
```
### `::selection` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/::selection)
The selection of the `<p>` are `pink`
```CSS
p::selection {
	background-color: pink;
}
```
`::selection {...}` apply to all the document
### `::after` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-letter)
