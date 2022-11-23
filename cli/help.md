## Help

### Information

`man ls` — display interactive manual pages of command 'ls'.

`ls --help` or `help ls` — display help page.

`apropos list` — search for man pages in 'whatis' database by keyword 'list' (partial match).

`whatis ls` — short information about the 'ls' command 

`whereis ls` — command file location

`which ls` — search for a program (file) in the search path (PATH).

`mandb` — create an index of reference databases for the above utilities.

`stat some-file` show inode information of the file 'some-file'

`ps x` — show list of the process

`ps a` — show list of the process

`ps x | awk '{print $1}'` — show list of the process (only first column)

### Search

`find /dev -name 'pt*' -type d` — find directory with name 'pt*' in '/dev' directory

`find /dev -name 'pt*' -type f` — find file with name 'pt*' in '/dev' directory

`find / -inum 358416841` — find file by inode

`yum install mlocate` — install locate.

`updatedb` — update (initialization) file database.

`locate some.txt` — search for files in the locate database. 

`locate -b` `locate --basename` — search only in filename.

`locate -e` `locate --existing` — display only existing files.

`locate -i` `locate --ignore-case` — ignore case when searching.

`locate -r` `locate --regexp REGEXP` — search for regular expression REGEXP.

`whereis ls` — search for programs, their man pages and source codes.

`type ls` — show how the command will be interpreted by the shell.

### History

`history` — show the command history.

`history -c` — delete the command history.

`history -d 5`— delete the history entry at position 5.



---
[Home](../README.md) -> [CLI](cli.md)
