### YUM

1 `sudo yum clean all`

2 `sudo nano /etc/yum.conf` + `keepcache=1` + `cachedir=/var/cache/yum`

3 `sudo yum install nmap-ncat` and `sudo yum install htop`

4 `yum install epel-release`

5 `yum repolist --enabled` and `yum repolist --disabled` or `yum repolist --all`

6 `sudo yum install htop` and `htop`

7 `sudo yum provides /etc/sysctl.conf` or `sudo yum prov /etc/sysctl.conf` or `sudo rpm -qf /etc/sysctl.conf` -> `systemd-239-58.0.1.el8_6.8.x86_64`

8 `sudo yum remove nmap-ncat`


### RPM

9 `sudo rpm -qa | less`

10 `sudo rpm -ql htop` 

11 `sudo nano /usr/share/doc/htop/README` + some in file (#) and `rpm -V htop` or `rpm --verify htop`

12 `sudo rpm -qf /etc/lvm/lvm.conf` -> `lvm2-2.03.14-3.el8_6.2.x86_64`

13 `sudo find /var/cache/yum -type f -name *.rpm` and `sudo rpm -i /var/cache/yum/ol8_appstream-d4d5cd0a0a095846/packages/nmap-ncat-7.70-8.el8.x86_64.rpm`

### *

14 `rpm2cpio /var/cache/yum/ol8_appstream-d4d5cd0a0a095846/packages/nmap-ncat-7.70-8.el8.x86_64.rpm | cpio -idmv -D ~/rpm_files`
`yum info nmap` and `nmap -v`

15 `yum groupinstall "Development Tools"`
`yum install make`
`wget https://nmap.org/dist/nmap-7.93.tar.bz2` 
`tar -xvf nmap-7.93.tar.bz2`
`cd nmap-7.93`
`./configure`
`make`
`sudo make install`



---
[Home](../README.md) -> [Labs](labs.md)
