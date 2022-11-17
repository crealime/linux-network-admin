## Disks

``df -h`` — show free disk space

``df -ih`` — show free inodes

``du -h /home``  — show used space of the /home (all dir info)

``du -sh /home`` or ``du --max-dept=0 /home``  — show used space of the /home (summary info)

``du -sh /home /root`` — show used space of the /home and /root (summary info)

``du --max-dept=1 /home`` — show used space of the /home (first nesting level with hidden files)

``lsblk`` — show information about discs

``blkid`` — display the type of file system on a block device (which may not be mounted), as well as device-specific attributes

``fdisk -l /dev/sda`` show 'sda' disk information

``fdisk /dev/sdb`` create disk layout

``mkfs`` — build a Linux filesystem

``mkfs.ext4 /dev/sdb5`` — build the ext4 Linux filesystem

``tune2fs -l /dev/sdb5 | less`` — adjust tunable filesystem parameters on ext2/ext3 filesystems (list attr)

``xfs_info`` — FS-specific utilities of various types

``xfs_admin`` — FS-specific utilities of various types

``losetup`` — disk imaging utility

``fsck`` — checking and restoring the integrity of the file system

``mount`` — show mounted devices

``mount /dev/sdb1 /media/1`` — mount /dev/sdb1 to the /media/1 directory

``mount -r /dev/sdb1 /media/1`` — mount /dev/sdb1 to the /media/1 directory (read only)

``mount -o noatime /dev/sdb5 /media/5`` — mount /dev/sdb5 to the /media/5 directory (read only)

``mount -o loop ./CentOS-7.0.iso /mnt `` or ``mount ./CentOS-7.0.iso /mnt `` mount CentOS-7.0.iso image to the /mnt directory (read only)

``mount --bind /usr/sdin /mnt `` mount /usr/sdin directory to the /mnt directory

``umount /dev/sdb5`` or ``umount /media/5`` — unmount /dev/sdb5

``nano /etc/fstab`` — file to create constant mount

``mount -a`` — mount all after edit /etc/fstab

``swapon`` ``swapon -s`` show usage space

``swapon /dev/mapper/ol-swap`` add swap

``swapoff /dev/mapper/ol-swap`` remove swap and load all from it to the RAM


---
[Home](../README.md) -> [CLI](cli.md)
