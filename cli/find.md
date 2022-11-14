### Find

``find /home some`` — find 'some' file or directory in 'home' directory.

``find /home -type f some`` — * simple files

``find /home -type d some`` — * directories

``find /home -type l some`` — * symbolic links

``find /home -type b some`` — * block devices (dev)

``find /home -type c some`` — * symbol devices (dev)

``find /home -type p some`` — * named pipes

``find /home -type s some`` — * sockets