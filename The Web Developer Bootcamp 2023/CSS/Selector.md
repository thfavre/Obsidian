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

## Element `selector {`
Select all `name` of the page.
```CSS
button {
	color: pink;
}
```

## List `selector1, selector2 {`
Select all `name` of the page.
```CSS
h1, h2 {
	color: pink;
}
```

## ID  `#tagname  {`
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

## Class `.classname {`
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