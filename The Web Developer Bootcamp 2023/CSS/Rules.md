#CSS 

# Generality
Almost everything you do in CSS follow this basic pattern:
```CSS
selector {
	property: value;
}
```

# Examples :
- Make all the `<h1>` elements purple :
```CSS
h1 {
	color: purple;
}
```

- Make all image elements 100px wide and 200px tall:
```CSS
img {
	width: 100px;
	height: 200px;
}
```

# Where to style ?
## Inline style
Inside the html : (**bad** practice) 
```html
<h1 style="color: purple">Title!</h1>
<button style="background-color: green">Button</button>
<button style="background-color: green">Another button</button>

```
Bad because I have to write it on every button, and if I want to change the color, I have to change it individually. 

## The `<style>` [[Elements]]
Inside the html (**bad practice**)
```html
<style>
	h1 {
		color: purple;
	}
</style>

<h1>I am a purple h1</h1>
<h1>I am also a purple h1</h1>
```
Bad because if I have more than I document, I will have to write it in each. 

## External Stylesheet
**Good** practice :)
Write the style in a `.css` file, and then include the file using a `<link>` in the head of the [[HTML]] document.
```css:path_to_style.css
h1 {
	color: purple;
}
```
```html
<head>
    <title>Title!</title>
    <link rel="stylesheet" href="folder/path_to_style.css">

</head>

```

