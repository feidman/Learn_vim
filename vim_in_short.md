# install 
```
sudo apt-get install vim //ubuntu
```

# vimtutor
```
vimtutor
```
# Moving the cursor
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

#Undo
```
u: undo
CTRL + r: redo
```

#Copy and paste
```
v: enter visual mode
y: copy
p: paste
yy: copy the whole line
dd: cut the whole line
```

# Find
```
/:look forward
?: look backward
%: find the matched brace,[,{,(
n: keep looking
N: keep looking reversing
```

# Replace
```
:r: replace the char under the cursor.
:R: replace mode, type and over
:s/old/new: replace the first matched string
:s/old/new/g: replace all matched strings within this line
:%s/old/new/g: replace all matche strings within the whole file
```


#configuration
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
#: InstantMarkdownPreview
```
