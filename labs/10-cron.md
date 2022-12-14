## Cron
### 1

1. `tail -f /var/log/cron`
2. `crontab -e` `*       *       *       *       *       date >> /tmp/date`
3. `sudo less  /var/spool/cron/slipper`
4. `sudo tail -f /tmp/date`
5. `crontab -e` `*       *       *       *       *       data >> /tmp/date`

### 2

1. `crontab -e` `*/20       *       *       *       *       '' > /tmp/date`
2. `crontab -e` `1       9       *       *       mon-fri       echo 'Hello World!'`
3. `crontab -e` `1       *       *       *       *      sudo cat /var/log/cron | grep 'END EDIT' | wc -l > /tmp/cron_count`
4. `echo $(date) | awk '{print $2" "$3}'`

echo $(date) | key = awk '{print $2" "$3}' | echo key
