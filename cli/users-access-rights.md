### Users access rights

#### Files

`/etc/passwd` — file with information about user accounts

`/etc/group` — file with information about group list and user list

`/etc/shadow` — file with user password

`/etc/gshadow` — file with group password

`/etc/sudoers` — file with sudo settings (recommendation: edit with `visudo` only)

`/etc/login.defs` — a file containing various options, which are set by default by the created users

`/etc/default/useradd` — useradd default params

`/etc/skel` — is a directory with a set of files inside that will be placed in the new user's home directory

`/etc/shells` — a file with a list of available shells

`/sbin/nologin` (/usr/sbin/nologin) is a special shell, which does not let the user into the system. At the same time, she reports that the user is not allowed to log in

`/etc/nologin.txt` — the message that will be displayed in if the user shell is /sbin/nologin

`/etc/nologin` — the presence of this file blocks login all regular users. Content of this file displayed when such users try to log in

`/etc/nologin.txt` — file to display information that the user is banned (when user shell is changed to `/sbin/nologin`)

`/etc/nologin` — file to ban all regular users

#### Working with users:

`useradd` — create a user account

`userdel` — deleting a user account

`usermod` — change user account

`passwd` — change authentication token (password)

`chage` — changing temporary policies by user

`vipw` (vigr) — editing configuration files users (groups)

`pwck` (grpck) — checking the integrity of account files users (groups)

#### Working with groups:

`groupadd` — create a group account

`groupdel` — deleting a group account

`groupmod` — change user account

`gpasswd` — change authentication token

#### Commands with which a normal user can change your account information

`chsh` — change the user's shell

`chfn` — change user information

`passwd` — change password (hash)

#### Shell-Specific Commands

`umask` — setting the default access rights for created files and directories

`ulimit` — user limit on the number of processes, open files, etc.

#### View Users and Groups

`id` — display the id of the user and the groups to which he included

`users` — display the names of users who are on currently working in the system

`w` — show who is logged in and what they are doing now

`who` — show who is logged in

`groups` — show the groups the user belongs to

`last` — show user login history

`uptime` — show how long the system has been up + average server load

#### User substitution

`su` — allows you to run commands as someone else user or group

`newgrp` — way to change the current primary group

#### Transfer of privileges

`sudo` – program with which the superuser may enable certain users and groups to run privileged programs

`visudo` — special editor for making changes to file `/etc/sudoers`

#### Access rights

`r` (read), 4 – reading
File: content view
Directory: view list of files (contents of direntry table)

`w` (write), 2 – write
File: change file
Directory: add, remove, rename files (change direntry)

`x` (eXecute), 1 – execution
File: run file for execution
Directory: go to directory

`s` (setuid), 4 – change process EUID to owner UID executable file. For a directory, all attachments that are created have this the same UID as the owner of this directory.

`S` (setgid), 2 – substitution of process EGID for executable GID file

`t` (sticky), 1 – directory to add. In a directory with this bit, any the user can create their own files. These files can only be deleted: 1) superuser, 2) owner of the directory, 3) owner of these files.

#### Change of access rights

`chmod` (change mode) — utility for changing permissions access to files (directories). Works like with numeric representation of access rights, and with symbolic

Examples:

`chmod u+x file` — allow the owner to run the file for execution

`chmod o-rwx file` — disable all actions on the file for everyone else

`chmod g=rx file` — group is allowed to read and run the file for execution

`chmod 755 file` — set permissions to “rwx r-x r-x”

`chmod 4744 file` — set permissions to “rws r-- r--”

`chmod 1777 dir` — set permissions on the directory "rwx rwx rwt"

#### Changing the owner of a file

`chown` (change owner) — utility for changing ownership (group) of the specified file or directory.

Syntax:

`chown [options] NewOwner[:NewGroup] file ...`

Examples:

`chown userok file` — change the owner of the file to userok

`chown userok:grp file` — change at the same time and owner on userok, and group on grp

`chown :grp file` — change group to grp (similar to chgrp)

`chown -R userok Dir` — Change the owner of the Dir directory and owners of all its attachments recursively on userok

#### attr

`lsattr some-dir` — show filesystem attributes 

`chattr some-dir` — change filesystem attributes 


---
[Home](../README.md) -> [CLI](cli.md)
