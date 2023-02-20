#CSS 

It a element has no style, it will take the one of his parent.
```html
<body>
	<h1>Blaaa</h1>
	<section>
		</h2>HEY!</h2>
		<p>
		sads
		asdasd
		sdaasd
		</p>
		<button>Press</button>
	</section>
</body>
```

```CSS
body {
	color: pirple;
}
```
It will make all the text purple, because the child of the `body` have no [[Rules]].

```CSS
body {
	color: pirple;
}
section {
	color: red;
}
```
The `h1` will be purple.
All text that come after will be red.

## `inherit` keyword [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Inherit)
The color in the button `placeholder` is not set to the color of the parent.
===Certain elements don't inherit things by default===
But there is a way if we want to :
```CSS
button {
	color: inherit;
}
```
It will take the style of the closest parent 

