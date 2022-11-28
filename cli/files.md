## Files

`echo 'Hello, world!'` — Write arg 'Hello world!' in the command line

`echo -n 'Hello, '; echo 'world!'` — Write arg 'Hello world!' in the command line (`-n` don`t write last symbol (\n))

`echo 'Hello world' > some-file` — write text 'Hello world' to the 'some-file' file

`echo 'Hello world' | tee -a some-file` — show and write text 'Hello world' to the 'some-file' (`-a` — append to file)

`file some-file` — show information about the 'some-file' file

`stat some-file` — show information about the 'some-file' file (inode content)

`touch some-file` — create new empty 'some-file' file

`cat some-file` — show file 'some-file' content

`cat some-file > some-file-new` — writing the contents of the file 'some-file' to the file 'some-file-new' (create file if it doesn't exist)

`less some-file` — show file 'some-file' content (page by page)

- `CTRL+ f` — go to next page

- `CTRL+ b` — go to previous page

- `F` — show changes in dynamic files in real time

- `v` — edit file in vi-editor `INS` — edit mode `ESC` — quite from edit mode `:wq` — write and quite

- `/pattern +ENTER` — search 'pattern' in the file  `n` — move forward `N` move back

`grep -i 'pattern' some-file` — search lines with 'pattern' in the file 'some-file' (`-i` — case insensitive)

`grep -B5 -A12 'pattern' some-file` — show 5 lines before and 12 lines after match with the 'pattern'

`grep -C10 'pattern' some-file` — show 10 lines before and 10 lines after match with the 'pattern'

`grep -E '192\.168\.14\[0-9]{1,3}'` or `egrep '192\.168\.14\[0-9]{1,3}'` search with regexp

`find ~ -name 'some*' -type f -exec rm -f` — find and delete all files with name 'some*' in home directory

`find ~ -name 'some*' -type f | xargs grep 'some text'` — find files with name 'some*' and show matches 'some text' in they

`xargs` — ???

`echo 'hello world' | sed -e 's/l/L/g'` -> `heLLo worLd` —  replacement

`cmp some-file some-other-file` — show files content differences

`diff -urBNE file1.txt file2.txt > file.patch` — make patch-file

`patch < file.patch` apply patch

`patch -d some-dir file1.txt < file.patch` patch 'file1.txt' in 'some-dir' directory

`cp file1 file2` — copy the file 'file1' to the same directory with name 'file2'

`cp -r dir1 dir2` — recursive copy the directory to the same directory with name 'dir2'

`dd` — can copy all objects

`echo some | tr -s 's' 'c'` -> `come` — replace symbols in all content

`mv` — move files and directories

`ps a | cut -f1,3,4 -d ' '` — show column

`head -2 file1` — show first two lines of the file content

`tail -2 file1` — show last two lines of the file content

`echo '/dev/disk/by-id/some.txt' | xargs basename` —> `some.txt`

`echo '/dev/disk/by-id/some.txt' | xargs dirname` —> `/dev/disk/by-id`

`wc some-file` —> `2 2 14 some-file` — two lines, two words, fourteen symbols, file name

`cmod a-w some-file` — change file permissions (write prohibition for all users)

- `u` — owner
- `g` — group
- `o` — others
- `a` — all
- `-` — prohibition
- `+` — permission
- `=` — assignment
- `r` — reading
- `w` — writing
- `x` — execution

`ls | uniq` — only uniq lines

`ls | sort -u` — only sort uniq lines

`ln -s some-file link-file` — add the symbol link 'link-file' for the 'some-file' (file or directory)

`ln some-file link-file` — add the hard link 'link-file' for the 'some-file' (file or directory)

`rm some-file` — remove file

`cmd1 | cmd2` — transferring the result of the program 'cmd1' to the program 'cmd2'

`some-cmd > some-file` write output result of the program 'some-cmd' to the file 'some-file' (overwrite file)

`some-cmd >> some-file` write output result of the program 'some-cmd' to the file 'some-file' (append to file)

`find / -type f -user lime > my-files.log 2> error.log` — redirecting output to the file 'my-files.log' and redirecting errors to the file 'error.log'




---

[Home](../README.md) -> [CLI](cli.md)

