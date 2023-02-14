#HTML

# Inline VS Block Elements
- Inline elements fit in the alongside other elements.
- Block level elements take up a whole "block" of space.
# Elements
## Bold `<b> </b>`
```html
I am <b>bold</b>.
```
> I am **bold**.

## Paragraph `<p> </p>`
A group of content that go together.
```html
<p>
para1
</p>

<p>
para2
</p>
```
> para1
>
> para2

## Heading `<h1> </h1>`
We should have at most one h1 at the top of the page.
We should never have a `<h3>` if we dont have a `<h2>`, etc.
```html
<h1>Title<\h1>
<h2>Terminology<\h2>

```
> Title
> Terminology

## Lists
We can only use `<li>`, `<script>` and `<template>` inside lists.
### Unordered `<ul> </ul>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)
```html
<ul>
	<li>First</li>
	<li>Second</li>
</ul>
```
> o First 
> o Second
### Ordered `<ol> </ol>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)
```html
<ol>
	<li>First</li>
	<li>Second</li>
</ol>
```
> 1. First 
> 2. Second

## Anchor `<a> </a>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)
With its `href` [[Attribute]], creates a hyperlink to web pages, files, email addresses, locations in the same page, or anything else a URL can address.
Content within each `<a>` _should_ indicate the link's destination. If the `href` attribute is present, pressing the enter key while focused on the `<a>` element will activate it.
```html
<p>You can reach Michael at:</p>

<ul>
  <li><a href="https://example.com">Website</a></li>
  <li><a href="mailto:m.bluth@example.com">Email</a></li>
  <li><a href="tel:+123456789">Phone</a></li>
  <li><a href="test.html">Test</a></li>
</ul>
```
> You can reach Michael at:
> -   [Website](https://example.com/)
> -   [Email](mailto:m.bluth@example.com)
> -   [Phone](tel:+123456789)
> -   [test](test.html)

## Image `<img>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img) 
- There is no closing tag.
-   The `src` attribute is **required**, and contains the path to the image you want to embed.
-   The `alt` attribute holds a text description of the image, which isn't mandatory but is **incredibly useful** for accessibility — screen readers read this description out to their users so they know what the image means. Alt text is also displayed on the page if the image can't be loaded for some reason: for example, network errors, content blocking, or linkrot.
- `width` and `height` is not recommended (use [[CSS]] instead)
```html
<img src="https://fr.wikipedia.org/wiki/Image#/media/Fichier:Image_created_with_a_mobile_phone.png" alt="Description of the image">
```

## Comment `<!-- -->`
```html
	<!--Comment blabla -->
```
> [!Shortcut] VS-Code Shortcut
> `CTRL` + `\` : comment the selected lines

## Content Division `<div> </div>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div) 
- Used to group elements together and style it all at once.
- It should be used only when no other [[Elements#Semantic Elements |Semantic Elements]] is appropriate.
The **`<div>`** [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) element is the generic container for flow content. It has no effect on the content or layout until styled in some way using [CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS) (e.g. styling is directly applied to it, or some kind of layout model like [Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout) is applied to its parent element).
```html
<div class="warning">
    <img src="/media/examples/leopard.jpg"
         alt="An intimidating leopard.">
    <p>Beware of the leopard</p>
</div>
```
As a "pure" container, the `<div>` element does not inherently represent anything. Instead, it's used to group content so it can be easily styled using the [`class`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#class) or [`id`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#id) attributes, marking a section of a document as being written in a different language (using the [`lang`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#lang) attribute), and so on.

## Content Span `<span> </span>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span) 
- Same as [[Elements#Content Division `<div> </div>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div) |Content Division]] but [[Elements#Inline VS Block Elements |inline]].
- It can be used to group elements for styling purposes (using the [`class`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#class) or [`id`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#id) attributes)
- It should be used only when no other [[Elements#Semantic Elements |Semantic Elements]] is appropriate.
```html
<p>Add the <span class="ingredient">basil</span>, <span class="ingredient">pine nuts</span> and <span class="ingredient">garlic</span> to a blender and blend into a paste.</p>

<p>Gradually add the <span class="ingredient">olive oil</span> while running the blender slowly.</p>
```
```CSS
span.ingredient {
    color: #f00;
}
```
> Add the ===basil===, ===pine nuts=== and ===garlic=== to a blender and blend into a paste.
> Gradually add the ===olive oil=== while running the blender slowly.

## Horizontal Rule `<hr>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr)
- Create a ~line 
```html
<hr>
```

## Line Break `<br>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr)
```html
Blabla<br>Tititi
```
> Blabla
> Tititi

## Superscript `<sup> <\sup>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sup)
Specifies inline text which is to be displayed as superscript for solely typographical reasons. Superscripts are usually rendered with a raised baseline using smaller text.
```html
Bla<sup>2<\sup>
```
> Bla²

## Subscript `<sub> <\sub>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sub)
Specifies inline text which is to be displayed as superscript for solely typographical reasons. Superscripts are usually rendered with a raised baseline using smaller text.
```html
C<sup>8<\sup>H<sup>10<\sup>
```
> C₈H₁₀

## Form [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/form)
Represents a document section containing interactive controls for submitting information.
When summiting a form, a [[http request ]]will be send.
```html
<form action=""></form>
```

### Input `<input>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/input)
Used to create interactive controls for web-based forms in order to accept data from the user; a wide variety of types of input data and control widgets are available, depending on the device and [user agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent). The `<input>` element is one of the most powerful and complex in all of HTML due to the sheer number of combinations of input types and attributes.
```html
<form>
	<input type="text" id="name" name="name" required
       minlength="4" maxlength="8" size="10" placeholder="TEXT">
</form>
```
The `type` can be [password](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/password), [color](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/color), [number](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number),  [checkbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox),  [radio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/radio), …
#### Attributes :
- [`placeholder`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#placeholder) : Text that appears in the form control when it has no value set.
- [`minlength`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#minlength) : Minimum length (number of characters) of `value`
- …
### Button `<button> </button>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/button)
Is an interactive element activated by a user. Once activated, it then performs an action, such as submitting a [form](https://developer.mozilla.org/en-US/docs/Learn/Forms) or opening a dialog.
Outside a 'form' the default type is 'button';
```html
<button class="favorite styled"
        type="button">
    Add to favorites
</button>
```
When a button is inside a form, the default behavior ('type=submit') is to submit the form. (go to `relative_link`)
```html
<form action="/relative_link">
	<button>Submit</button>
</form>
```

### Select `<select> </select>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select)
Represents a control that provides a menu of options.
```html
<label for="pet-select">Choose a pet:</label>

<select name="pets" id="pet-select">
    <option value="">--Please choose an option--</option>
    <option value="dog">Dog</option>
    <option value="cat">Cat</option>
    <option value="hamster">Hamster</option>
    <option value="parrot">Parrot</option>
    <option value="spider">Spider</option>
    <option value="goldfish">Goldfish</option>
</select>
```
### Example : a form that make a reddit search
```html
<form action="https://www.reddit.com/search">
	<input type="text" name="q">
	<button>Search Reddit</button>
</form>
```
## Label `<label>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/label)
Represents a caption for an item in a user interface.
When a `label` is clicked, the button, input,.. is selected.
```html
<div class="preference">
    <label for="cheese">Do you like cheese?</label>
    <input type="checkbox" name="cheese" id="cheese">
</div>
```
The [[id]] and `for` should be the same.
## Table `<table> </table>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/table)

### Elements

### `<td>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/td)
Defines a **cell** of a table that contains data. It participates in the _table model_.

### `<th>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/th)
Defines a cell as header of a group of table cells. The exact nature of this group is defined by the [`scope`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th#attr-scope) and [`headers`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th#attr-headers) attributes.

### `<tr>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/tr)
Defines a **row** of cells in a table. The row's cells can then be established using a mix of [`<td>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td) (data cell) and [`<th>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th) (header cell) elements.

### `<thead>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/thead)
Defines a set of rows defining the head of the columns of the table.

### `<tbody>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/tbody)
Encapsulates a set of table rows ([`<tr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr) elements), indicating that they comprise the body of the table ([`<table>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)).

### `<tfoot>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/tfoot)
Defines a set of rows summarizing the columns of the table.

### Example :
```html
<table>
	<tr>
		<th>Title Col 1</th> 
	</tr>
	<tr>
		<th>Title Col 2</th> 
	</tr>
	<tr>
		<td>Col 1 Row 1</td>
		<td>Col 2 Row 1</td>
	</tr>
	<tr>
		<td>Col 1 Row 2</td>
		<td>Col 2 Row 2</td>
	</tr>
</table>
```


# Semantic Elements
- Make the code more readable to human and applications.
- Useful for screen reader (for ex. voice over) to quickly find some elements (for blind people).

## `<main> </main>`  [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main)
Represents the dominant content of the [[Skeleton#body|body]] of a document. The main content area consists of content that is directly related to or expands upon the central topic of a document, or the central functionality of an application.

## `<nav> </nav>`  [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)
Represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.
```html
<nav>
	<ul>
		<li><a href="home.html">Home</a></li>
		<li><a href="about.html">About</a></li>
	</ul>
</nav>

```

## `<section> </section>`  [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section)
Represents a generic standalone section of a document, which doesn't have a more specific semantic element to represent it. Sections should always have a heading, with very few exceptions.

## `<article> </article>`  [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article)
Represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). Examples include: a forum post, a magazine or newspaper article, or a blog entry, a product card, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.

## `<aside> <\aside>`  [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside)
Represents a portion of a document whose content is only indirectly related to the document's main content. Asides are frequently presented as sidebars or call-out boxes.

## `<header> <\header>`  [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header)
Represents introductory content, typically a group of introductory or navigational aids. It may contain some heading elements but also a logo, a search form, an author name, and other elements.

## `<footer> <\footer>`  [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer)
Represents a footer for its nearest ancestor [sectioning content](https://developer.mozilla.org/en-US/docs/Web/HTML/Content_categories#sectioning_content) or [sectioning root](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements#sectioning_root) element. A `<footer>` typically contains information about the author of the section, copyright data or links to related documents.

# Example 
```html

```