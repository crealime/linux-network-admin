## Command line interface (CLI)

[username@hostname location]$ — information in command line (prompt).

``command [-argument] [--long-argument] file`` — typical syntax in command line.

``whoami`` — name of the current user (who am I).

``pwd`` — name of the current directory (print working directory).

``ls`` — content of the current directory (list).

``man ls`` — show all possible arguments of 'ls' command.

``whereis ls`` — show 'ls' program location.

``ls -a`` — * with all files, including files starting with '.' character (hidden files).

``ls -l`` — * with a long listing format.

``ls -al`` — combination of the arguments.

``ls -al | grep a`` * with all files and directory whose names include 'a'.

``ls -al > tmp/my-new-file`` — write result to the 'my-new-file' file.

``cat < / tmp/my-new-file`` or ``cat tmp/my-new-file`` — show content of the 'my-new-file' file.

``cd dir`` — goto the 'dir' directory.

``cd ..`` — goto the parent directory.

``cd ~`` — goto the home directory.

``cd -`` last directory

``mkdir some-folder`` create folder 'some-folder' in current directory.

``touch app.js`` create new file 'app.js'.

``du`` — estimates of disk usage by all files recursively starting from the current directory (disk usage).

``du --summarize /usr`` * size of the topmost directory.

``du --summarize /usr --human-readable`` or ``du -sh /usr`` * more readable result.

``du -hd 2 --threshold=10M /usr`` — show a size of all files (and directories) recursively, starting from specified directory /usr, but will only print entries till two levels below it. Also, we ask du to print sizes in a human-readable format.

``ip a`` — show all IPs.

``mkdir some-dir; cd some-dir`` — sequential execution of commands.

### Command history

``history`` — show the command history.

``history -c`` — delete the command history.

``history -d 5``— delete the history entry at position 5.



---
[Home](../README.md) -> [CLI](cli.md)
