## Users

`groupadd universe`

`useradd -d /creator -g universe creator`

`useradd -d /home/des -g universe destroyer`

`passwd creator`

`passwd destroyer`

---

`whereis mount` -> `/usr/bin/mount`

`whereis umount` -> `/usr/bin/umount`

`visudo` add line `creator  ALL=(creator)    NOPASSWD:/usr/bin/mount, /usr/bin/umount`

---

`whereis ip` -> `/usr/sbin/ip`

`visudo` add line `%universe       ALL=(ALL)       NOPASSWD:/usr/sbin/ip`



---
[Home](../README.md) -> [Labs](labs.md)
