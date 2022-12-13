## Utilities and programs

### Vim

`vim some.txt` — edit file some.txt in vim editor

How to work

`h` — go left

`j` — go down

`k` — go up

`l` — go right


`x` — delete the character highlighted by the cursor

`dw` — delete text from cursor to end of word, including trailing space

`d$` — delete from cursor to end of line

`d^` — remove from cursor to start of line

`de` — deleting from the cursor to the end of the word, NOT including the terminator space

`dd` — delete entire line

`<Ins>` or `i` — switch to edit mode

`<Esc>` — return to normal mode

`:q` — quit vim

`:q!` — exit vim without saving any changes made

`:wq` — save changes and exit

`:wq!` — force save changes and exit


#### Commands and objects

`d[number]object` — The format of the "delete" command d is as follows.

Where:

`d` — delete command.

`number` — of times to execute the command

`object` — with which the command should be executed

Short list of objects:

`w` — from the cursor to the end of the word, including the trailing space.

`e` — from the cursor to the end of the word, NOT including the trailing space.

`$` — from cursor to end of line.

`^` — from cursor to start of line.

#### Undo and paste commands

`u` — cancel the result of the previous command

`U` — Undo corrections in the entire line

`p` — inserts after the last deleted (or copied) cursor. text (if a line has been deleted, it will be placed in line under the cursor).

`r` — replacement of a single character under the cursor (the character must follow to which it is being replaced).

`c[<number>]<object>` — Change text (deletes the object and switches to inserts

`o` — create a blank line UNDER the cursor and enter insert mode

`O` — create a blank line ABOVE the cursor and enter insert mode

`a` — insert (switch to insert mode) text AFTER the cursor

`Ctrl+g` — location in the file and information about it

`<line number>Shift+g` —move to the specified line in the file

`Shift+g` — move to end of file

#### Find and replace commands

`:s/<was>/<will be>` replaces ONLY the first occurrence found in current line

`:s/<was>/<will become>/g` substitution GLOBALLY in the entire line (replaces all found in the occurrence string)

`:s/<was>/<will become>/gc` found in the occurrence string) with confirmation of each replacement

`:#,#s/<was>/<will become>/g` replace all occurrences of a sequence characters between two lines (#,# are the numbers of these lines)

`:%s/<was>/<will become>/g` replace all occurrences in entire file

`/<text> search <text>` GO

`?<text> search <text>` BACK

`n` - go to the next occurrence of the search string

`:set ic` – ignore case when searching or replacingе

`hlsearch` – search highlight

`incsearc`h – incremental search

#### Executing External Commands

`:!<command>` execute external command

`:w FILENAME` write the currently edited file to disk under  name FILENAME

`:#,#w` FILENAME save lines # through # to file FILENAME

`:r FILENAME` Read FILENAME from disk and put it in to the current file following the cursor position.

#### Vim Tutorial

`vimtutor` or `vimtutor ru`

### Screen















---
[Home](../README.md) -> [CLI](cli.md)
