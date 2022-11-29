## Processes

`ps aux -sort` — show processes (more info)

`ps auxwwww -sort` — show processes (more info)

`ps axo pid,cpu,command pid,pcpu,pmem,command --sort=-pcpu` — show processes with pid, cpu, memory and command columns, cpu-sort

`top` show processes in real time `f` (on command work) — columns settings

`kill -USR1 8045` — send the signal USR1 to the process 8045

`while true; do kill -USR1 8045; sleep 2; done` — send signal every 2 seconds

`killall -r 'firefox|chrome'` — send signal to the group of processes (firefox and chrome)

`pstree -ap` — show the tree of the user processes

`jobs` — user tasks

`kill %1` — stop process [1] in process tree (jobs)

`bg 1` — start task 1 in the background

`dd if=/dev/zero of=/dev/null &` — & at the end of the line — run the program in the background mode

`fg 1` — take the program 1 from the background to the terminal

`Ctrl + Z` — send the program to the background

`nice –n -6 top` — run program 'top' with priority 14 (20 - 6)

`renice –n 2 9975` — change priority to 2 for the program with PID 9975

`find /etc /proc -type f 2>&1 | less` — pipe send from the 2-th descriptor (standard errors) to the 1-th descriptor (standard in)

`ls /proc/1263/fd` — show descriptors of the process with PID 1263

`strace mkdir some-dir` — show system calls of the command mkdir

`ls; echo $?` -> — information about program ended (exit code) `0` — correct `1` — failure `2` — error

---

`ping google.com >> tmp/ping.log` — write result of the 'ping' to the file 'tmp/ping.log'

`tail -f tmp/ping.log` — show last line of the file 'tmp/ping.log' in interactive mode

`ps aux | grep ping` — show process 'ping'

`fuser tmp/ping.log` or `lsof tmp/ping.log` — show who is interacting (writing) with the file

---


### Signals

- 1 HUP (Отбой) – перечитать конфигурацию (без останова сервиса), перезапуск, выход, завершение
- 2 INT (Прерывание) – выход, завершение (^C)
- 3 QUIT (Выход) – выход, завершение (редко)
-  KILL (Убить) – не игнорируемое/не обрабатываемое уничтожение (когда другие варианты уже не помогают) – некорректное завершение
- 14 ALRM (Сигнал тревоги) – срабатывание таймера, завершение
- 15 TERM (Завершение) – нормальное завершение работы
- STOP (Остановить) – остановить выполнение процесса
- CONT (Продолжить) – возобновить работу процесса
- USR1 / USR2 (Пользовательские) – определен пользователем




---
[Home](../README.md) -> [CLI](cli.md)

