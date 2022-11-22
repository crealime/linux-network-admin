## 01 Command line

`cp ~/.bashrc ~/.bashrc.reserve` — copy .bashrc file (as reserve version)

`nano ~/.bashrc` — open .bashrc file in nano editor

Add `PS1="RootCommand> "` into .bashrc file. Save the file (ctrl + o, Enter) and exit (ctrl + x)

`source ~/.bashrc` — refresh the bash to apply changes

`ls -la` — show all files in long read format

`passwd` — change password for current user

`adduser slipper` — add user slipper

`passwd slipper` — add password for user slipper

`nano ~/.bashrc` — open .bashrc file in nano editor

Add `export PATH="/sbin"` into .bashrc file. Save the file (ctrl + o, Enter) and exit (ctrl + x)

`cat /etc/passwd` or `cut -d: -f1 /etc/passwd` — show all users

`alias ls='ls -laF` — add temporary alias

`alias ls='ls -la --color --group-directories-first'`

`nano ~/.bashrc` — open .bashrc file in nano editor

Add `alias e='echo New alias'"` into .bashrc file (add constant alias). Save the file (ctrl + o, Enter) and exit (ctrl + x)

`unalias e` — remove alias


---
[Home](../README.md) -> [Labs](labs.md)
