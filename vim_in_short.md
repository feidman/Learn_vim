# install 
```
sudo apt-get install vim //ubuntu
```

# vimtutor
```
vimtutor
```
# Move Cursor
## Move a char or a word
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
0: move to the begining of current line;
$: move to the end of current line

H,M,L: Jump to the Top, middle or bottom of current display.(H for Head, M for middle, L for tail)

gg: jump to the first line of current file
G: jump to the last line of current file
%: jump between brace (),{},[],"".

Ctrl+f: move forward one page.
Ctrl+b: move backward one page.
Ctrl+d: move forward half page.

## scroll screen
zt: place the current line to the top of current view.
zz: place the current line to the middle of curent view.
zb: place the current line to the bottome of current view.
Ctrl+e: roll one line.



