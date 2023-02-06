#html

# TO PUT IN ELEMENT 
Represents a document section containing interactive controls for submitting information.
When summiting a form, a [[http request ]]will be send.

[MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/form)

# Form
```html
<form action=""></form>
```

## `<input>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/input)
Used to create interactive controls for web-based forms in order to accept data from the user; a wide variety of types of input data and control widgets are available, depending on the device and [user agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent). The `<input>` element is one of the most powerful and complex in all of HTML due to the sheer number of combinations of input types and attributes.
```html
<form>
	<input type="text" id="name" name="name" required
       minlength="4" maxlength="8" size="10">
</form>
```
The `type` can be [password](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/password), [color](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/color), [number](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number), ...

### Attributes :
- [`placeholder`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#placeholder) : Text that appears in the form control when it has no value set.
- [`minlength`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#minlength) : Minimum length (number of characters) of `value`
- ...

## `<label>` [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/label)
Represents a caption for an item in a user interface.
```html
<div class="preference">
    <label for="cheese">Do you like cheese?</label>
    <input type="checkbox" name="cheese" id="cheese">
</div>
```
The [[id]] and `for` should be the same.