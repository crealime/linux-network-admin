## Command line interface (CLI)

[username@hostname location]$ — information in command line (prompt).

``command [-argument] [--long-argument] file`` — typical syntax in command line.

``whoami`` — name of the current user (who am I).

``pwd`` — name of the current directory (print working directory).

``ls`` — content of the current directory (list).

``ls -a`` — * with all files, including files starting with '.' character (hidden files).

``ls -l`` — * with a long listing format.

``ls -al`` — combination of the arguments.

``ls -al | grep a`` * with all files and directory whose names include 'a'

``cd dir`` — goto the 'dir' directory

``cd ..`` — goto the parent directory

``cd ~`` — goto the home directory

``du`` — estimates of disk usage by all files recursively starting from the current directory (disk usage).

``du --summarize /usr`` * size of the topmost directory.

``du --summarize /usr --human-readable`` or ``du -sh /usr`` * more readable result.

``du -hd 2 --threshold=10M /usr`` — show a size of all files (and directories) recursively, starting from specified directory /usr, but will only print entries till two levels below it. Also we ask du to print sizes in a human-readable format.

``ip a`` — show all IPs


### Aliases

``alias fjpg="find . | grep -iE '\.jpg$'"`` -> ``fjpg`` = ``find . | grep -iE '\.jpg$'`` — make alias

``unalias fjpg`` — remove alias

## Command history

``history`` — show the command history

``history -c`` — delete the command history

``history -d 5``— delete the history entry at position 5



---
[Home](../README.md)
