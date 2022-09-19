```vim
:vs  // split vertical
ctr + w + arrow
:sp  // split horizontal 
:q  // quit a window

:e fileName // go in the fileName file (create it if not existing)

```

Vim Cheat Sheet : https://vim.rtorr.com/
 
## Tips :
### Configuration :
to add some default vim configuration : 
1) go in .vimrc file : vim .vimrc					
2) write settings :
```vim
syntax on
set tabstop=4
set shiftwidth=4
set autoindent
set smartindent
set termguicolors
colorscheme desert
set number	
```
3):w
4):so%
	

## NORMAL mode:
>i		go in INSERT mode
>I        go INSERT mode and at the start of the line
>a		go in INSERT mode (and move one char at the right)
>A      go in INSERT mode at the end of the line
>s      go in insert mode and delete the character (4s to delete 4)
>cc	delete the line and go in INSERT mode
>dd    delete a line (3dd will delete 3 lines,   or 3 Z || d$ will delete to the end of the line)
>dw    delete a word
>dt     delete the char from the cursor to the end of the word
>x   delete one charaacter (10 x delete 10 char)  
>u     undo
>ctrl-r		redo
>yy		copy a line (4yy copy 4 lines)			
>p		paste (p -> paste after, P-> paste before)
> .		call last command
> ctrl + n    autocompletion
> \>       indent the current line (see VISUAL mode)
### movement :
>k		move up
>j		move down
>h		move left
>l		move right 
>G		move at the end of the file (10G move at the line 10) or gg
>$		move at the end of the line
>^		move at the beginning of the line
>w		move at the beginning of the next word
>b		move at the beginning of the last word
>*		move to the next word under the cursor 

>:q		quit vim 
>:w		write
>:wq || ZZ	write and quit
>:q!		quit without write 
>CRTL-z		put the document in the background to open it again (foreground) : fg
>:term		open the terminal 

>:set number	set numbering to on
>:set nonumber	set numbering to of
>:syntax on	highlight the syntax

>/foo		search in the file (n ,  next, N, previous)
>%s/foo1/foo2/g	repalce all foo1 with foo2 (/gc, ask confirmation, 'foo1' : change only if whole word,  /gi,  case insensitive)		


>ctrl+z		pause vim	fg to return to vim
>:sh		pause vim	ctrl+d to return to vim

>:term		go in Terminal-Job mode		exit to leave

## In INSERT mode :
>ESC	return to COMMAND mode

## In VISUAL mode :
>maj+V     go in selection mode and select the line
> maj+v    go in selection mode
> \>            indent the selection
> <            indent to the left 
> 



## Macro
1 q : record mode 
2 lettre
3 faire toutes les commandes 
4 ESC, q
@lettre

