## 2

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

## 3

`sudo yum repolist all`

`screen -S logviewer`

`sudo tail -f /root/services.log`

`Ctrl+a d`

## 4

## 5

`ps axu | grep /root`

`sudo kill 1461`

## 6

`sudo nano /home/serviceman/write.sh`

↓
```
#!/bin/bash
ps aux --sort=-%mem | head -2 | tail -1 >> /home/serviceman/services.log
sudo cp /home/serviceman/services.log /root/services.log
```

`ps -eo lstart,cmd --sort=-%mem | head -2 | tail -1 | awk '{c="date -d\""$1 FS $2 FS $3 FS $4 FS $5"\" +\047%Y-%m-%d %H:%M\047"; c|getline d; $1=$2=$3=$4=""; $5="=>"; printf "%s\n",d$0 }'`





