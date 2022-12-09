## Installing and updating software

### Compilation

`wget http://...` — download from link 

`configure` — installation configuration

`make install` — install

### Package

### rpm

`rpm2cpio some-package.rpm | cpio -vdim` — rpm package content ???

`rpm -i some-package.rpm` — install utility

`rpm -U some-package.rpm` — update or install if the utility is not installed

`rpm -e some-package.rpm` — delete utility

`rpm -qa | less` — show all utilities in system

`rpm -qf /usr/bin/dd` -> `coreutils-8.30-12.0.1.el8.x86_64` — show the program that includes 'dd'

`rpm -ql coreutils` show a list of programs that contains 'coreutils'

### yum 

`yum install some-package.rpm` (from local) or `yum install some-package` (from server) — install utility

`yum remove lsof` — remove program 'lsof'

`yum list installed | less` — show all installed programs in the system

`yum search lsof` -> `lsof.x86_64...` — search 'lsof' program on the yum server

`yum info lsof.x86_64` — show information about lsof.x86_64

`yum deplist lsof` — show dependencies of the 'lsof' program

`yum provides lsof` — show repositories that includes 'lsof'

`yum grouplist` — groups of the packages 

`yum groupinfo 'System Tools'` — show information about program group 'System Tools'

`yum groupinstall 'System Tools'` — install program group 

`yum groupremove 'System Tools'` — remove program group

`nano /etc/yum.conf` — yum configuration 

`man yum.conf` — help about yum configuration

`yum clean packages` — clean yum packages from cache

`yum clean all` — clean yum metadata and packages from cache

`ls /etc/yum.repos.d` — files repositories settings










---
[Home](../README.md) -> [CLI](cli.md)
