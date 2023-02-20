#CSS

What happens when conflicting styles target the same elements?

**Specificity** is how the browser decides which rules to apply when multiple rules could apply to the same element.

It is a measure of how specific a given selector is. ==The more specific selector "wins"==.

## Priority
`Inline Styles` > `ID` > `CLASS` > `ELEMENT`
[Specificity Calculator](https://specificity.keegan.st/)

## Same specific  
**The Cascade** : The order your styles are declared in and linked to matters!
```CSS
h1 {
	color: red;
}
h1 {
	color: pink;
}
```
Pink wins!

## Example
```CSS
p {
	color: yellow;
}

section p {
	color: red;
} 
```
`red` win!

## Inline style
Have the highest priority but should not be used. 

## `!important`  [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/Specificity)
Should almost never be used.
It will overwrite all other specificities. 
```CSS
p {
	color: yellow; !important
}
```
