## Screen

dot-screenrc
```
vbell off
startup_message off
defscrollback 10000
shelltitle "> |bash"
shell -$SHELL
# enable SHIFT-PGUP / SHIFT-PGDOWN scroll
termcapinfo xterm ti@:te@
termcapinfo xterm 'hs:ts=;:fs=:ds=;'
backtick 1 1 1 ~/.screenrc-getuptime -dhms
caption always '%{= d} %= %{= w} %-w %{+b r} %n * %t %{-b r} %{= w} %+w %='
hardstatus alwayslastline '%{= Y} Host: %H %{= M} Uptime: %1` %{= G} Load: %l %= %{= C}%C %A = %c:%{=B R}%s%{= C} %{= B}%D %d %M(%m) %Y'
#alt-q and alt-w
bindkey "^[w" next
bindkey "^[q" prev
```

dot-bashrc
```
# add these lines to .bashrc
# start screen on SSH login
if [ "$PS1" != "" -a $TERM != "screen" -a "${STARTED_SCREEN:-x}" = x -a "${SSH_TTY:-x}" != x ]
then
 STARTED_SCREEN=1
 export STARTED_SCREEN
 sleep 1
 screen -RR
 #screen -qRD
fi
```

dot-screenrc-getuptime
```
#!/bin/bash
uptime=$(</proc/uptime)
uptime=${uptime%%.*}
result=""
while getopts "dhms" param; do
 case ${param} in
 s)
 seconds=$(( uptime%60 ))
 result=$result$seconds
 ;;
 m)
 minutes=$(( uptime/60%60 ))
 result=$result$minutes":"
 ;;
 h)
 hours=$(( uptime/60/60%24 ))
 result=$result$hours":"
 ;;
 d)
 days=$(( uptime/60/60/24 ))
 result=$result$days" days "
 ;;
 esac
done
echo $result
```

`screen`

`<Ctrl + d>`

`screen -S current-screen`
`screen -S current-screen`

`screen -S 2975.current-screen -X sessionname current-screen-2`

7 `<Ctrl + a c>` * 4

```
top
<Ctrl + a Tab>
tail -f /var/log/messages
<Ctrl + a Tab>
yum update
<Ctrl + a Tab>
ls
```

8 `<Ctrl + a d>`

9 `screen -ls` `screen -x current-screen-2`

10 `<Ctrl + a S>` (horizontal) or `<Ctrl + a |>` (vertical)


