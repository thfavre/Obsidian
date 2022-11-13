Vim Cheat Sheet : https://vim.rtorr.com/
 
## .Vimrc :
To add some default vim configuration, modify the .vimrc file : 			
My settings  : [github](https://github.com/diabolo257/vimconfig/blob/main/.vimrc)
`:so%` to reload vim with the new settings (otherwise)



## NORMAL mode :
### Change mode 
- `i` go in INSERT mode
- `I` go INSERT mode and at the start of the line
- `a` go in INSERT mode (and move one char at the right)
- `A` go in INSERT mode at the end of the line
- `s` go in insert mode and delete the character (4s to delete 4)
- `cc` delete the line and go in INSERT mode
___
### Save / quit 
`:q` quit vim 
`:w`	 write
`:wq` or `ZZ` write and quit
`:q!` quit without write 
___
### Movement :
- `k` moves up
- `j` moves down
- `h` moves left
- `l` moves right 
- `G` moves at the end of the file (10G move at the line 10) or gg
- `$` moves at the end of the line
- `^` moves at the beginning of the line
- `w` moves at the beginning of the next word
- `b` moves at the beginning of the last word
- `*` moves to the next same word
- `f+CHAR` find and move to the first CHAR
- `H`(igh) moves at the beginning of the screen.
- `M`(iddle) moves at the middle of the screen.
- `L`(ow) moves at the bottom of the screen.
___
### Delete 
- `c+[Movement]` deletes the characters from the current cursor position up to the end of the movement
- `dd` delete a line (3dd will delete 3 lines,   or 3 Z || d$ will delete to the end of the line)
- `dw` delete a word
- `dt` delete the char from the cursor to the end of the word
- `x` delete one charaacter (10 x delete 10 char)  
- `X` delete the previous charaacter
___
### Undo / redo
- `u` undo
- `ctrl+r` redo
- `yy` copy a line (4yy copy 4 lines)			
- `p` paste (p -> paste after, P-> paste before)
___
### Divers 
 - `.` call last command
 - `>` indent the current line (see VISUAL mode to indent multiple lines)
___
### Preference (see [[vim#.Vimrc :]])
`:set number` set numbering to on
`:set nonumber` set numbering to of
`:syntax on` highlight the syntax
___
### Search / replace
- `/foo` search in the file (n ,  next, N, previous)
- `%s/foo1/foo2/g` repalce all foo1 with foo2 
	- `[...]gc` ask confirmation
	- `[...]gi` case insensitive	
___
### Auto-complete
- `:help ins-completion` see all options
- `CTRL+n` auto-complete 
- `CTRL+x+n` search just in THIS file
- `CTRL+x+f` file finder
>After one of those command, we can use `CTRL+n` and `CTRL+p` to go back and forth in the suggestion list 
___
### windows management 
- `ctrl+z` put the document in the background, `fg` (foreground) to open it again 
- `:sh` pause vim,` ctrl+d` to return to vim
- (`:term` go in Terminal-Job mode, `exit` to leave)

#### buffer 
- `vim -b /path/to/file1 /path/to/file2 /path/to/file3` open the files in vim as a buffer
- `:b[uffer] <partial filename><tab>` jump to a buffer
- `:bw` buffer wipe, remove a buffer
- `:e[dit] <file path>` editpen a new buffer
	- `:E` (open the tree selection)
- `:find <file path>` find and add the filename to the buffer
- `pltags` - enable jumping to subroutine/method definitions
- `:ls` list of all buffer
- `:mksession! ~/today.ses`   save the session
	- `vim -S ~/today.ses`   load the session

#### tab
`vim -p /path/to/file1 /path/to/file2 /path/to/file3` open the files in vim as a tab
`:tabe[dit] /path/to/file` open a new tab
`: tabn[ext]` or `gt` jumping to the next tab (`ngt` move in the n tab)
`tabp[revious]` or `gT` jumping to the previous tab
`:tabc[lose] ` close the current tab
`:tabs` display all the tabs / windows

#### splitting window
- `:sp[lit] /path/to/file` splits the window horizontally and opens the file
	- (`ctrl+w s` split the window h. with the same document)
- `:vs[plit] /path/to/file` splits the window vertically (and opens the file
	- (`ctrl+w v`  split the window v. with the same document)
-  `Ctrl+w+[cursor keys]` or `Ctrl+w+[hjkl]` or `Ctrl+w Ctrl+[hjkl]`jump between windows 
- `Ctrl+w w` or `Ctrl+w Ctrl+w` jump to the next window
- `Ctrl+w W `jump to the previous window
- `Ctrl+w p` or `Ctrl-w Ctrl-p` jump to the last accessed window 
- `Ctrl+w c` or `:clo[se]` close  the current window
- `Ctrl+w o` or `:on[ly]` makes the current window the only one and close all other ones
- `Ctrl+W+`   
	- `+` or `-`  to resize the height
	-  `<` or `>` to resize the width 
___
### Macro
1) `q` : record mode 
2) `lettre`
3) make all the commands
4) `ESC` then `q`
`@lettre` to write all the commands

## In INSERT mode :
`ESC`  return to COMMAND mode

## In VISUAL mode :
`maj+V` go in selection mode and select the line
`maj+v` go in selection mode
`>` indent the selection
`<` indent to the left 




