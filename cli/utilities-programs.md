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

`screen -S sessionname` — option can be used to name the session when its creation.

`screen -ls` or `screen -list` — lists strings identifying screen sessions.

`screen -d` or `screen -D` — does not start a new session, but instead disconnects already launched earlier.

`screen -x sessionname` — Connect to the given screen session.

`screen -R` Resume the first disabled one it encounters session.

`screen -X command` send the specified command to a running screen session.

`screen -wipe [match]` deletes destroyed session files instead of mark them as "dead" (dead).

#### Keyboard shortcuts

`Ctrl + a w` Show window list.

`Ctrl + a ?` (help) Show key bindings.

`Ctrl + a c` Create a new window with the interpreter running and switch to this window.

`Ctrl + a C` Clear the screen.

`Ctrl + a d` Disable screen from this terminal.

`Alt + q` Navigate windows to the left.

`Alt + w` Navigate windows to the right.

`Ctrl + d` End the screen window or end the entire screen if one window has been created.

`Ctrl + a >` Write clipboard to file.

`Ctrl + a <` Read exchange file (screen-exchange) into clipboard exchange.

`Ctrl + a ]` Write clipboard contents to standard stream input of the current window.

#### Areas

`Ctrl + a S` - Split the current region into two new ones (horizontal).

`Ctrl + a |` - Split the current region into two new ones (vertical).

`Ctrl + a tab` - Switch input focus to the next area.

`Ctrl + a X` - Close current area.

### Syslog

Demon `rsyslogd` and his config `/etc/rsyslog.conf`

Library commands:
`openlog`
`rsyslog`
`closelog`

Format of the file `/etc/rsyslog.conf` : `mail.err /var/log/mail.errors`

Examples:

`mail.info /var/log/maillog`

`mail.=debug /var/log/maillog.debug`

or

`mail.info /var/log/maillog`

`mail.>info /var/log/maillog.debug`

### Logrotate

Example of the config file `etc/logrotate.conf`:

```
"/home/<user-www>/logs/access.log"
{
rotate 10 # number of compressed fragments to store
size=16M # maximum uncompressed file size; while the size of the current
# log file will not exceed this threshold, the file will not be "rotated"
missingok # missing file is not an error
nocopytruncate # don't dump the log file after copying
nocreate # don't create an empty log
nodelaycompress # don't defer file compression to the next cycle
nomail # do not send the contents of deleted (old) logs by mail
notifempty # don't process empty files
noolddir # keep all files in the same directory
compress # compress
postrotate
/usr/bin/killall -HUP httpd
endscript # There are commands between postrotate and endscript
# sh(1) interpreter, executed immediately after rotation.
# In this example, the kill command is placed here, restarting
# httpd-server. This is necessary for the normal procedure
}
```

### Cron

`crontab -e` — edit config file in editor

`/etc/crontab` — config file

```
#minute  hour   mday    month   wday        command
0,20,40  */5    1-31    *       mon-fri     echo hello
```

```
Minute minute from 0 to 59.
Hour hour from 0 to 23.
Mday is the day of the month from 1 to 31.
Month month from 1 to 12 (three letters from the name of the month are allowed, casedoesn't matter from jan to dec).
Wday day of the week from 0 to 7 (0 is Sunday, you can write from sunto sat).
```

### At (batch)

`at time [date][+delay]`

`at -r job_id ...`

`at -l [jobi_d ...]`

`-r` — Delete jobs previously scheduled with at
or batch, by job_id.

`-l` — Display information about scheduled tasks by job_id.

Job scheduling example:

`echo "sh file" | at 1900 thursday next week`

### Less

`PageUp` — Move one page up

`PageDown` — Move one page down

`SPACE` — Move down one page

`ENTER` — Move down one line

`d` — Move half a page down

`b` — Move up one page

`/pattern/` — Search for the specified pattern forward

`?pattern?` — Search by pattern back

`n` — next in search

`N` — previous in search

`h` — Help

`q` — Exit

### Tail

`tail [options] filename` — Syntax

`-n` — number of lines

`-f` — the tail utility watches the file, and newlines (added to the end of the file by another process) are automatically printed to the screen in real time

Example:
`tail -20 /var/log/messages`
`tail -f /var/log/messages`

### Head

head is a utility on UNIX and UNIX-like systems that displays the first n lines from file, default n is 10.

Syntax:

`head [-strings] [file...]`

Example:

`df | head -n 2 | tail -n 1`

### Split

split is a command that copies a file and splits it into separate files of a given length.

Syntax:

`split [-l lines] [-b bytes[km]] [file [output_prefix]]`

`-l` — Each output file should contain no more than the specified number of rows

`-b` — Each output file should contain no more than the specified

the number of bytes. Additional specifiers stand for: `k` — kilobytes, `m` — megabytes

`-n parts` — (not in all versions of split) Splits the file into n equal parts


---
[Home](../README.md) -> [CLI](cli.md)
