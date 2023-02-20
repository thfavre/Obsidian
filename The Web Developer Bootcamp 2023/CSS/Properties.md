#CSS 

- [[]]
# Colors
## `color` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
Change the text [[Color]].
```CSS
h1 {
	color: blue;
}

button {
	color: rgb(255, 0, 0); 
}
```

## `background-color` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
Change the background [[Color]].
```CSS
h1 {
	background-color: grey;
}

button {
	background-color: pink;
}
```

# Text
## `text-align` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
Sets the horizontal alignment of the inline-level content inside a block element or table-cell box. This means it works like [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align) but in the horizontal direction.
```CSS
h1 {
	text-align: center;
}
```

## `font-weight` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)
Sets the weight (or boldness) of the font. The weights available depend on the [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) that is currently set.
```CSS
h1 {
	font-weight: 400;
}
```

## `text-decoration` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
Sets the appearance of decorative lines on text. It is a shorthand for [`text-decoration-line`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-line), [`text-decoration-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-color), [`text-decoration-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-style), and the newer [`text-decoration-thickness`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-thickness) property.
```CSS
h1 {
	text-decoration: blue underline wavy;
}
a {
	text-decoration: none;
}
```

## `line-height` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
Sets the height of a line box. It's commonly used to set the distance between lines of text. On block-level elements, it specifies the minimum height of line boxes within the element. On non-[replaced](https://developer.mozilla.org/en-US/docs/Web/CSS/Replaced_element) inline elements, it specifies the height that is used to calculate line box height.
```CSS
h1 {
	line-height: 2;
}
```

## `letter-spacing` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing)
Sets the horizontal spacing behavior between text characters. This value is added to the natural spacing between characters while rendering the text. Positive values of `letter-spacing` causes characters to spread farther apart, while negative values of `letter-spacing` bring characters closer together
```CSS
h1 {
	letter-spacing: 15px;
}
```

## `font-size` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)
Sets the size of the font. Changing the font size also updates the sizes of the font size-relative [`<length>`](https://developer.mozilla.org/en-US/docs/Web/CSS/length) units, such as `em`, `ex`, and so forth.
```CSS
h1 {
	font-size: 12px;
}
```

## `font-family` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)
Specifies a prioritized list of one or more font family names and/or generic family names for the selected element.
[Use of fonts on Windows and Mac](https://www.cssfontstack.com/)
```CSS
h1 {
	font-family: Arial;
}
h2 {
	font-family: Segoe UI, Furura, Arial, sans-serif;
}
```

## `MODEL` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/)
Blabla
```CSS
h1 {
	
}
```


# Box
## `width` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/width) and `height` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/height)
```CSS
div {
	width: 200px; 
}
```

## `border` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
```CSS
div {
	border-width: 5px;
	border-color: #21f120;
	border-style: solid;
	border-left-color: #fff2ff;
	border-radius: 12%;
	...
}
```
It creates a border of 5 `px`, if the width if 200, the total with is now 210 (200+5+5)
To make it be 200 with the border, we can add :
`box-sizing: border-box;`
#### Shorted syntax [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
```CSS
div {
	/* width | style | color */ 
	border: medium dashed green;
}
```