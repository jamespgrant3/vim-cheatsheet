# vim cheatsheet

## global
- **`:help`** keyword - open help for keyword
- **`:saveas file`** - save file as
- **`:close`** - close current pane
- **`K`** - open man page for word under the cursor

## cursor movement
- **`h`** - move cursor left
- **`j`** - move cursor down
- **`k`** - move cursor up
- **`l`** - move cursor right
- **`H`** - move to top of screen
- **`M`** - move to middle of screen
- **`L`** - move to bottom of screen
- **`w`** - jump forwards to the start of a word
- **`W`** - jump forwards to the start of a word (words can contain punctuation)
- **`e`** - jump forwards to the end of a word
- **`E`** - jump forwards to the end of a word (words can contain punctuation)
- **`b`** - jump backwards to the start of a word
- **`B`** - jump backwards to the start of a word (words can contain punctuation)
- **`%`** - move to matching character (default supported pairs: '()', '{}', '[]' - use  `:h matchpairs`  in vim for more info)
- **`0`** - jump to the start of the line
- **`^`** - jump to the first non-blank character of the line
- **`$`** - jump to the end of the line
- **`g_`** - jump to the last non-blank character of the line
- **`gg`** - go to the first line of the document
- **`G`** - go to the last line of the document
- **`5G`** - go to line 5
- **`fx`** - jump to next occurrence of character `x`
- **`tx`** - jump to before next occurrence of character `x`
- **`Fx`** - jump to previous occurrence of character `x`
- **`Tx`** - jump to after previous occurrence of character `x`
- **`;`** - repeat previous f, t, F or T movement
- **`,`** - repeat previous f, t, F or T movement, backwards
- **`}`** - jump to next paragraph (or function/block, when editing code)
- **`{`** - jump to previous paragraph (or function/block, when editing code)
- **`zz`** - puts the current line at the center of the screen
- **`zt`** - puts the current line at the top of the screen
- **`zb`** - puts the current line at the bottom of the screen
- **`Ctrl + e`** - move screen down one line (without moving cursor)
- **`Ctrl + y`** - move screen up one line (without moving cursor)
- **`Ctrl + b`** - move back one full screen
- **`Ctrl + f`** - move forward one full screen
- **`Ctrl + d`** - move forward 1/2 a screen
- **`Ctrl + u`** - move back 1/2 a screen
- **`]m`** - jump to beginning of next method
- **`]M`** - end of next
- **`[m`** - beginning of previous
- **`[M`** - end of previous
- **`g;`** - jump to the last change you made
- **`g,`** - jump back forward through the change list
- **`&`** - repeat the last substitution on the current line
- **`g&`** - repeat the last substitution on the all lines

## insert mode
- **`Ctrl + o <command>`** - execute normal-mode command while in insert-mode
- **`i`** - insert before the cursor
- **`I`** - insert at the beginning of the line
- **`a`** - insert (append) after the cursor
- **`A`** - insert (append) at the end of the line
- **`o`** - append (open) a new line below the current line
- **`O`** - append (open) a new line above the current line
- **`ea`** - insert (append) at the end of the word
- **`Esc`** - exit insert mode

## working with multiple files
- **`:e file`** - edit a file in a new buffer
- **`:bnext`** or  **`:bn`** - go to the next buffer
- **`:bprev`**  or  **`:bp`** - go to the previous buffer
- **`:bd`** - delete a buffer (close a file)
- **`:ls`** - list all open buffers
- **`:sp file`** - open a file in a new buffer and split window
- **`:vsp file`** - open a file in a new buffer and vertically split window
- **`Ctrl + wo`** - toggle maximizing a split
- **`Ctrl + ws`** - split window
- **`Ctrl + ww`** - switch windows
- **`Ctrl + wq`** - quit a window
- **`Ctrl + wv`** - split window vertically
- **`Ctrl + wh`** - move cursor to the left window (vertical split)
- **`Ctrl + wl`** - move cursor to the right window (vertical split)
- **`Ctrl + wj`** - move cursor to the window below (horizontal split)
- **`Ctrl + wk`** - move cursor to the window above (horizontal split)

## editing
- **`r`** - replace a single character
- **`J`** - join line below to the current one with one space in between
- **`gJ`** - join line below to the current one without space in between
- **`gUw`** - uppercase until end of word
- **`gUU`** - uppercase entire line
- **`gu$`** - lowercase until the end of the line
- **`gwip`** - reflow paragraph
- **`cc`** - change (replace) entire line
- **`C`** - change (replace) to the end of the line
- **`c$`** - change (replace) to the end of the line
- **`ciw`** - change (replace) entire word
- **`cw`** - change (replace) to the end of the word
- **`dap`** - delete the whole paragraph
- **`s`** - delete character and substitute text
- **`S`** - delete line and substitute text (same as cc)
- **`u`** - undo
- **`vaw`** - visually select word
- **`xp`** - transpose two letters (delete and paste)
- **`Ctrl + r`** - redo
- **`.`** - repeat last command
- **`:sort`** - sort all lines
- **`:sort!`** - sort in reverse
- **`:sort u`** - removes dupes and sort
- **`:sort i`** - ignore case
- **`:sort n`** - sort numerically

## visual mode
- **`v`** - start visual mode, mark lines, then do a command (like y-yank)
- **`V`** - start line-wise visual mode
- **`=`** - indent line(s) after selecting in visual mode
- **`V%`** - select a block of text
- **`o`** - move to other end of marked area
- **`Ctrl + v`** - start visual block mode
- **`O`** - move to other corner of block
- **`vaw`** - mark a word
- **`vab`** - a block with ()
- **`vaB`** - a block with {}
- **`vib`** - inner block with ()
- **`viB`** - inner block with {}
- **`Esc`** - exit visual mode
- **``** - exit visual mode
- **`>`** - shift text right
- **`<`** - shift text left
- **`y`** - yank (copy) marked text
- **`d`** - delete marked text
- **`~`** - switch case

## registers
- **`:reg`** - show registers content
- **`"xy`** - yank into register `x`
- **`"xp`** - paste contents of register `x`

## marks
- **`:marks`** - list of marks
- **`ma`** - set current position for mark A
- **`` `a``** - jump to position of mark A
- **`` y`a``** - yank text to position of mark A

## macros
- **`qa`** - record macro `a`
- **`q`** - stop recording macro
- **`@a`** - run macro `a`
- **`@@`** - rerun last run macro

## cut and paste
- **`Vyp`** - copy line(s) of text
- **`yy`** - yank (copy) a line
- **`2yy`** - yank (copy) 2 lines
- **`yw`** - yank (copy) the characters of the word from the cursor position to the start of the next word
- **`y$`** - yank (copy) to end of line
- **`p`** - put (paste) the clipboard after cursor
- **`P`** - put (paste) before cursor
- **`dd`** - delete (cut) a line
- **`2dd`** - delete (cut) 2 lines
- **`dw`** - delete (cut) the characters of the word from the cursor position to the start of the next word
- **`D`** - delete (cut) to the end of the line
- **`d$`** - delete (cut) to the end of the line
- **`x`** - delete (cut) character

## exiting
- **`:w`** - write (save) the file, but don't exit
- **`:w !sudo tee %`** - write out the current file using sudo
- **`:wq`** or **`x`** or  **`ZZ`** - write (save) and quit
- **`:q`** - quit (fails if there are unsaved changes)
- **`:q!`** or **`ZQ`** - quit and throw away unsaved changes
- **`:wqa`** - write (save) and quit on all tabs

## search and replace
- **`/pattern`** - search for pattern
- **`?pattern`** - search backward for pattern
- **`\vpattern`** - 'very magic' pattern: non-alphanumeric characters are interpreted as special regex symbols (no escaping needed)
- **`n`** - repeat search in same direction
- **`N`** - repeat search in opposite direction
- **`:%s/bad/good/g`** - replace all bad with good throughout file
- **`:%s/bad/good/gc`** - replace all bad with good throughout file with confirmations
- **`:28s/bad/good/g`** - replace all bad with good on line 28
- **`:6,11s/bad/good/g`** - replace all bad with goo in lines 6 to 11, including 6 and 11
- **`:noh`** - remove highlighting of search matches

## search in multiple files
- **`` :vimgrep /pattern/ {`{file}`}``**- search for pattern in multiple files
- **`:cn`** - jump to the next match
- **`:cp`** - jump to the previous match
- **`:copen`** - open a window containing the list of matches

## folding
- **`zc`** - close a fold at the cursor
- **`zf#j`** - creates a fold from the cursor down # lines
- **`zf/string`** - creates a fold from the cursor to string
- **`zj`** - moves the cursor to the next fold
- **`zk`** - moves the cursor to the previous fold
- **`zi`** - toggle folding entirely
- **`zo`** - opens a fold at the cursor
- **`zO`** - opens all folds at the cursor
- **`zm`** - increases the foldlevel by one
- **`zM`** - closes all open folds
- **`zr`** - decreases the foldlevel by one
- **`zR`** - decreases the foldlevel to zero — all folds will be open
- **`zd`** - deletes the fold at the cursor
- **`zE`** - deletes all folds
- **`[z`** - move to start of open fold
- **`]z`** - move to end of open fold

## quickfix list
- **`:copen`** - open the quickfix list
- **`:ccl`** - close the quickfix list
- **`:cn`** - go to next item in the list
- **`:cp`** - go to previuos item in the list

## netrw
- **`%`** - create a new file
- **`-`** - go up one directory
- **`d`** - create a directory
- **`D`** - delete a file or directory
- **`h`** - open the file in a horizontal split
- **`p`** - preview a file
- **`<C-w>z`** - close the preview
- **`R`** - rename a file or directory
- **`t`** - open the file in a new tab
- **`qf`** - display file information
- **`v`** - open the file in a vertical split
- **`mt`** - assign a target directory, used for move/copy commands
- **`mf`** - marks a file or directory for action to be taken
- **`mc`** - copy marked files into target directory
- **`mm`** - move marked files into target directory
- **`I`** - toggle header

# plugins

## vim-bookmarks
- **`<leader><leader>`** - add/remove bookmark at current line
- **`<leader>ba`** - add annotation at current line
- **`<leader>bsa`** - show all bookmarks (toggle)
- **`<leader>bn`** - jump to next bookmark in buffer
- **`<leader>bp`** - jump to previous bookmark in buffer
- **`<leader>bca`** - clear all bookmarks
- **`<leader>bmu`** - move up bookmark at current line
- **`<leader>bmd`** - move down bookmark at current line
- **`<leader>bmt`** - move bookmark at current line to another line

## fugitive
- **`<leader>`gs** - to show a window that lists changes
- **`<leader>`gb** - to show blame
- **`<leader>`gc** - to commit staged changes
- **`<leader>`gd** - to diff
- **`<leader>`gl** - to show log
- **`cb\<space\>`** - after running `\gs`, allows list, create, or delete branches
- **`co\<space\>`** - after running `\gs`, allows for switching branches
- **`+`** - after running `\gs`, and the cursor over a file, this will toggle showing file changes
- **`-`** - after running `\gs`, and the cursor over a file, this will toggle staging/unstaging a file
- **`X`** - after running `\gs`, and the cursor over a file, this will discard changes of a file
- **`-`** - after running `\gs`, and the cursor over a commit, this will prompt to push changes to the remote

## tmux general shortcut keys
- **`<leader>k`** - to clear the terminal window

## tmux window navigation
- **`<leader>\<window number\>`** - to toggle between windows
- **`<leader>w`** - to toggle between tmux sessions
- **`<leader>,`** - to rename a window
- **`<leader>h`** - split window horizontal
- **`<leader>v`** - split window vertical
- **`<leader>c`** - open a new window
- **`<leader>xy`** - close the current window
- **`<leader><right arrow>`** - move to the window to the right of the current window
- **`<leader><left arrow>`** - move to the window to the left of the current window
- **`<leader><up arrow>`** - move to the window above the current window
- **`<leader><down arrow>`** - move to the window below the current window

## tmux pane navigation
- **`C-h`** - move to the pane to the left
- **`C-l`** - move to the pane to the right
- **`C-j`** - move to the pane above
- **`C-k`** - move to the pane below
- **`<leader>{`** move the current pane left
- **`<leader>}`** move the current pane right

## tmux move windows
- **`C-S-left`** - move the window to the left
- **`C-S-right`** - move the window to the right

## tmux move panes
- **`<leader>c`** - move current pane clockwise
- **`<leader>u`** - move current pane counter clockwise
