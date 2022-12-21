## 1

`sudo useradd serviceman`

`sudo passwd serviceman`

`sudo touch /home/serviceman/services.log`

`sudo chmod a+w /home/serviceman/services.log`

`sudo nano /home/serviceman/write.sh`

↓
```
#!/bin/bash
ps aux --sort=-%mem | head -2 | tail -1 >> /home/serviceman/services.log
sudo cp /home/serviceman/services.log /root/services.log
```

`sudo chmod a+x /home/serviceman/write.sh`

`sudo crontab -eu serviceman`

↓
```
* * * * * /home/serviceman/write.sh
```

`sudo systemctl status crond`

`sudo systemctl enable crond`

`sudo systemctl start crond`

## 2

`sudo yum repolist all`

ol8_developer_EPEL


