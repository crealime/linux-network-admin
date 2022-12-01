## 02 File System

`fdisk /dev/sdb` — make disk partitions

`mount -r /dev/sdb1 /media/1` — mount /dev/sdb1 to the /media/1 directory (read only)

`mount -o noatime /dev/sdb5 /media/5` — mount /dev/sdb5 to the /media/5 directory (read only)

`nano /etc/fstab` — file to create constant mount

`/dev/sdb1 /media/1      ext4    defaults        0 0` — in /etc/fstab

`/dev/sdb5 /media/5      ext4    defaults        0 0` — in /etc/fstab

`umount /dev/sdb1`  — unmount /dev/sdb1

`umount /dev/sdb5`  — unmount /dev/sdb5

---
[Home](../README.md) -> [Labs](labs.md)
