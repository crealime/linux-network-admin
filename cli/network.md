## Network 

```
255  11111111  1
254  11111110  2
252  11111100  4
248  11111000  8
240  11110000  16
224  11100000  32
192  11000000  64
128  10000000  128
0    00000000  256
```

`ip a` or `ip address` — show all ip

`ip link` — show network devices

`ip r` — show all routs

`ip n` — show ARP table (mac addresses)

`arp -a` — show ARP table (mac addresses)

`traceroute`

`/etc/nsswitch.conf` — system database configuration and name service manager

Options:
```
passwd: files
shadow: files
group: files
hosts: files dns
protocols: files
rpc: files
services: files
netgroup: nisplus
publickey: nisplus
automount: files nisplus
aliases: files nisplus
```
```
files: text data files
db: binary data files (.db)db))
nis: Network Information Service
dns: Domain Name Service
```

Config files
```
/etc/protocols — network protocol definitions (protocols)
/etc/services — network service definitions (services)
/etc/hosts — network name resolution table (hosts)
/etc/passwd — user accounts (passwd)
/etc/shadow — shadow password file
/etc/group — user group accounts (group)
/etc/rpc — RPC program number database (rpc)
/etc/aliases — mail aliases for sendmail (aliases)
```

`/etc/protocols` — network protocol definitions

`/etc/services` — network service definitions

`/etc/resolve.conf` — network name resolve subsystem configuration

``

`systemctl stop NetworkManager` — stop NetworkManager

`systemctl disable NetworkManager` — disable NetworkManager

`/etc/hosts` — local static network name resolve table

`/etc/sysconfig/network` - basic network configuration file

Options:
```
NETWORKING — allow networking (yes/no))
GATEWAY — default network gateway
GATEWAYDEV — Gateway device name (NIC, if-name)
NISDOMAIN — NIS domain name

NETWORKING=yes
GATEWAY=192.168.116.2
```
`/etc/sysconfig/network-scripts/` — catalog of the network interface configuration (NIC) 

`/etc/sysconfig/network-scripts/ifcfg-<if-name>` — <if-name> – interface name and number (dmesg)

Options:
```
DEVICE - physical or logical device name (dmesg)
BOOTPROTO – boot time protocol (for configuration):
    none or static NIC static configuration (no protocols)
    dhcp use DHCP protocol
BROADCAST — broadcast address (deprecated)
DNS{1,2} — IP addresses of DNS servers Placed in /etc/resolv.conf with PEERDNS=yes
IPADDR — device IP address
NETMASK — netmask
PREFIX — network prefix
ONBOOT — whether to activate the device on boot (yes/no))
PEERDNS — modify /etc/resolv.conf (yes/no))
SRCADDR — IP address for outgoing packets
USERCTL — whether users are allowed to configure the device
    
DEVICE=eth0
BOOTPROTO=static
HWADDR=00:0C:29:F2:98:99
IPADDR=192.168.116.5
NETMASK=255.255.255.0
ONBOOT=yes
```

`ifdown enp0s3` — disable enp0s3 network interface

`ifup enp0s3` — enable enp0s3 network interface

`ip addr add 10.0.5.19/24 dev enp0s3` — add ip to the enp0s3 network interface



---
[Home](../README.md) -> [CLI](cli.md)
