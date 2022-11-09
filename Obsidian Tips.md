
# Keybindings
| Key    | Description             |
| ------ | ----------------------- |
| ctrl-p | open command palette    |
| ctrl-o | open file switch prompt |


# Markdown feature :
## Header :
### Blabla!

## Horizontal Rules
___
---
***

## Emphasis
**This is bold text**
__This is bold text__
*This is italic text*
_This is italic text_
~~Strikethrough~~
==This is highlighted==

## Blockquotes
> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.

## Lists
### Unordered
+ Create a list by starting a line with `+`, `-`, or `*`
+ Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    * Ac tristique libero volutpat at
+ Very easy!
### Ordered
1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
### Check
- [ ] This  is a 
- [ ] checklist 
	 - [ ] Indented check list or sub-task

## Code
### Inline 
`code`
### ndented code

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
### Block code "fences"
```
Sample text here...
```
### Syntax highlighting
``` js
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```

## Links
[link text](http://dev.nodeca.com)
[link with title](http://nodeca.github.io/pica/demo/ "title text!")

## Images
![Minion](https://octodex.github.com/images/minion.png)
## Embed
### Page
`![[Page Name]]`
### Paragraph
` ![[Page Name^block to link to]]`
### Heading and it’s subsequent content
`![[Page Name#heading to link to]]`