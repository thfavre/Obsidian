#HTML #VS-Code

To quickly write [[HTML]] code in `VS-Code`.

[Cheat Sheet](https://docs.emmet.io/cheat-sheet/)

# Examples :
## Skeleton
`!` 
To create the [[Skeleton]]
```html
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

##  Child: > 
`main>section>h1`
```html
<main>
    <section>
        <h1></h1>
    </section>
</main>
```

## Sibling: +
`div+p+bq`
```html
<div></div>
<p></p>
<blockquote></blockquote>
```

## Multiplication: *
`ul>li*3`
```html
<ul> 
	<li></li> 
	<li></li> 
	<li></li> 
</ul>
```

## Item numbering: $
`nav>ul>li*3>a[href=$]`
```html
<nav>
    <ul>
        <li><a href="1"></a></li>
        <li><a href="2"></a></li>
        <li><a href="3"></a></li>
    </ul>
</nav>
```

## Text: {}
`a{Click me}`
```html
<a href="">Click me</a>
```