`nano /etc/systemd/system/my.service`

```
[Unit]
Description=My Super service

[Service]
ExecStart=/root/my.sh

[Install]
WantedBy=multi-user.target
```

`nano /root/my.sh`

```
#!/bin/bash 
while true; do 
  date >> /var/log/my.log
  sleep 2 
done;
```

`systemctl enable my.service`
