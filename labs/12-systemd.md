## Systemd

`systemctl set-default rescue.target`

`reboot`

`systemctl list-units --type=target | grep $(systemctl get-default) | awk '{print $1 $2}' | md5sum | cut -c 5-10`

---

`systemctl set-default multi-user.target`

`nano /etc/systemd/system/varsize.service`

```
[Unit]
Description=Size of /var
After=multi-user.target

[Service]
ExecStart=/bin/bash -c "file='/root/varsize.log'; du -ms /var | awk '{print $1}' >> $file"

[Install]
WantedBy=multi-user.target
```

`systemctl enable varsize.service`

`systemctl start varsize.service`

`echo $(systemctl list-unit-files | grep varsize) $(systemctl start varsize 2>&1) $(find /root -mmin -2.0 -type f 2>&1) | md5sum | cut -c 10-16`

---

`nano /etc/systemd/system/custom.target`

```
[Unit]
Description=Custom target
Requires=varsize.service sshd.service
```

`systemctl enable custom.target`

`systemctl start custom.target`

`echo $(systemctl list-units --type=target | grep custom | awk '{print $1 $2 $3}') $(systemctl list-dependencies custom.target | head -3 | sed s/[^a-z]//g | sort) | md5sum | cut -c 10-16`