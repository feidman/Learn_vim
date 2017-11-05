# install 
```
sudo apt-get install vim //ubuntu
```

# vimtutor
```
vimtutor

manual \usr\share\vim\vim74\doc\usr_01.txt
*This file is base don this.* 

Reference on topics, such as move, insert and motion etc.
```
# Moving the cursor(usr_03.txt Moving around)
## Moving the cursor
``` 
h,j,k,l: move to Left, down, up and right one char.
w,b: move to the begining of next word(or previous word).
e: move to the end of next word.
```

## Jump
```
#: used before move command as a move step.
4w: move 4 words
3e: move to the last char of third words
0: move to the begining of current line
$: move to the end of current line

H,M,L: Jump to the Top, middle or bottom of current display.(H for Head, M for middle, L for tail)

gg: jump to the first line of current file
G: jump to the last line of current file
%: jump between brace (),{},[],"".

Ctrl+f: move forward one page.
Ctrl+b: move backward one page.
Ctrl+d: move forward half page.
Ctrl+u: move backwar half page.

CTRL+],T,O,I: moving to tags...
```

## scroll screen
```
zt: place the current line to the top of current view.
zz: place the current line to the middle of curent view.
zb: place the current line to the bottome of current view.
Ctrl+e: roll one line.
```
## advanced moving
```
fx: searches farward in the line for the single char x and moving to it
Fx: searches backward in the line for the char x and moving to it
tx: works as fx but moving to the char before the searched one
Tn: backward version of tx
; can repeat the four commands and . will repeat in other direction

3G: go to line 3
%20: go to the line of 20% position of the file
CTRL+G: the bottom line will show where you are and other info of the file

Ctrl+o: Last cursor place
Ctrl+i: Next cursor place
```
# making chages
## operator + motion
```
dw: delete one word
d2w: delete two words
cw: change a word (delete a word and leaves at insert mode)
c2w: change 2 word
dd: delete a whole line
cc: change a whole line
d$: delete to the end of the line
c$: change to the end of the line

dfx: delete untill 'x' was found (included)

shortcuts for most popular "operator + motion"

	x stands for dl
	X stands for dh
	D stands for d$
	C stands for c$
	s stands for cl
	S stands for cc
```
## repeat change
```
. :will repeat last change you've made
<<<<<<< HEAD
{   <B>:	    df>: delete untial > was found
=======

Examples:
   <B>:	    df>: delete untial > was found
>>>>>>> e7af71eb737c82ca7ee0ecd6f90250bf5653ab9b
	    move to next <
	    and . to repeat delete operation
   <B>
   /four:   find word four
   cwfive:  change four to five
   n:	    repeat find operation
   .:	    repeat change operation
   n:	    repeat find operation
   .:	    repeat chage operation
}


```
## Visual mode
```
v: visual mode and char selected
V: visual mode with line seleted
CTRL+v: visual mode with block slected
o: move to the other end of selection
O: move to the outher end of selected block
```

## Copy and p(vim for put)
```
y: copy(vim for Yank). It is a operator and can be used with motion appended.
p: put
yy: copy the whole line
dd: cut the whole line
y$: copy to the end of this line
y2w: copy two words

"*y: copy to clipboard
"*p: past from clipboard
```
## Text object
```
text object:
aw: a word
as
ap
ab: block betwween ()
a'
a"
a[
a{
a


usage:
aw: a word
daw: delete a word
as: a sentence
das: delete a sentence 
a word is refer to the word and the whitespace after it.

is: inner sentence ,same as as(a sentence) exception the whitespace after it.

dis: delete a sentence without white space after it.

is and as can be used in viusal mode to select text.
```
## Switch case
```
~: change the char to lowercase or uper case.
```

# split window
## split window
```
:split: split current window and display current file
:vsplit: do the same as split on in vertical direction
:split path/filename: split window and open new file
:new: split window and open a new file
:tab split: open new window in a tab windw
:gt: go to next tab window
```
## close window
```
:only: close all other windows
:close/quit: close the current window
```
## Resize window
```
:Ctrl w (#)+: to increase the size of a window(# lines)(CTRL W and Shift +/=)
:Ctrl w (#)-: to decrease the size of a window(# lines)
:{heigth}CTRL+w _: to set the window height to a specified number of liens
```

## Jump between windows
```
:Ctrl+w (hjkl,tb): move to (left/below/above/right,top/bottom)
:Ctrl+w (HJKL): move window to the far left/bottom/top/far right
```
## Command for all windos
```
:cmdall: exec a cmd for all windows.:qall will quit all window
```

# Exit vim
```
<esc> enter normal mode of vim
:q!: quit vim discard any changes you made
:wq: save and quit
```

# Delete
```
x: delete the char under the cursor
dw: delete the char until the end of this word
de: delete the char until the end of this word(with the char under the cursor)
d$: delete the chars to the end of this line
dd: delete the whole line
2dd: delete 2 lines
```
# Revise
```
i: insert at the cursor
A: append to the end of this line
a: insert after the cursor
o: insert a blank line after this line
O: insert a blank line before this line
```

# Undo
```
u: undo
CTRL + r: redo
```


# Find
```
/:look forward
?: look backward
%: find the matched brace,[,{,(
n: keep looking
N: keep looking reversing
*: positioning the cursor on the word at its next appearance 
'#': works as the * cmd except it do reversely
\< and \>: searches the whole word
:hlsearch
:nohlsearch
moving with marks......
```

# Replace
```
:r: replace the char under the cursor.
:R: replace mode, type and over
:s/old/new: replace the first matched string
:s/old/new/g: replace all matched strings within this line
:%s/old/new/g: replace all matche strings within the whole file
```


# Go away and come back
Ctrl + Z: go to shell
fg: come back to vim

:marks: show the marks of exit vim
\`mark_#: go back to the exact place.

# Inserting quickly(Insert mode)
## Making Correction
```
CTRL-w: delete the word before cursor
CTRL-u: delete to the beginning of this line.

Shift-Left: move cursor to left one word
Shift-Right:
PageDown
PageUp
Home
ENd
```
## Showing matches
```
:set showmatch: when you now type a text like"(example)", as soon as you type the ) Vim will briefly move the cursor to the matching(, keep it there for a half a second and move back to thwere you were typing. This also good for []{}
```
## Completion
```
Ctrl-p: is previous match
Ctrl-p: is nextious match
```
## Repeat insert
```
Ctrl-a: repeat the inserted text last time and enter Insert mode
Ctrl-@: do the same as Ctrl-a but exit to command mode
```
# configuration
```
set nobackup
set noswapfile
set encoding=utf-8

set ruler: show cursor coordingates

set number

colorscheme pablo (colorscheme are stored in the dir of /usr/share/vim/vim74/colors)
```

# Plugins
## Markdown
```
Plug 'suan/vim-instant-markdown'
let g:instant_markdown_slow = 1
let g:instant_markdown_autostart = 0
'#': InstantMarkdownPreview
```



# Learning tags
2017.10.22: usr_04.txt making small changes
2017.10.29: usr_08.txt split window
2017.11.1:  usr_21.txt go away and come back
2017.11.2:  usr_24.txt Inserting quickly

