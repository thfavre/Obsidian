#html

# TO PUT IN ELEMENT 

[MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/table)

## Elements

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


## Example :
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