## Systemd

`/usr/lib/systemd/system/` — systemd units distributed with installed RPM packages

`/run/systemd/system/` — systemd units created at run time.

`/etc/systemd/system/` — systemd units created and managed by system administrator.

`man systemd` `man systemctl` `man systemd.unit` `man systemd.service` — help

`systemctl` — management of services

`systemctl list-dependencies` — list target tree

`systemctl list-dependencies --all` — list all tree

`nano /etc/systemd/system/port-watcher.service`

```
[Unit]
Description=Our test service
After=multi-user.target

[Service]
ExecStart=/bin/bash -c "file='/var/log/port-watcher.log'; date >> $file; ss -tlpn >> $file; echo '' >> $file"

[Install]
WantedBy=multi-user.target

```

`systemctl deamon-reload`

`systemctl list-unit-files'` — show all services

`systemctl list-unit-files | grep 'my.service'` — show my.service services

`systemctl status port-watcher.service` — show status `port-watcher.service`

`systemctl enable port-watcher.service` — enable service

`systemctl disable port-watcher.service` — enable service

`systemctl start my.service`

`systemctl stop my.service`

`systemctl isolate rescue.target` — go to another runlevel (single user mode)

`systemctl list-units` — show active units

`systemctl list-units --type=target` — show active target units

`systemctl get-default` — show default target

`systemctl set-default rescue.target` — set default target (single user mode)

`systemctl set-default multi-user.target` — set default target (multi user mode)

`systemctl reboot`

`systemd-analyze blame` — show most long loading services

`scp -o Port=12345 root@localhost:root/time.svg ~`















---
[Home](../README.md) -> [CLI](cli.md)
