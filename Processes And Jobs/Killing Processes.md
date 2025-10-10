# Killing Processes
The objective for this challenge is to use kill cmd to kill the dont run process to get the flag.

## My solve
**Flag:** `pwn.college{Qz0zKb1UcpTAwBQJ_G9TGg51gZu.QXyQDO0wSN5AzNzEzW}`

in this challenge i first ran ps without the full format but got two bash cmds after running it with ef i got the commands and it pid then i killed that process and ran cha*/run to get the flag.
```bash
hacker@processes~killing-processes:~$ ps -e | grep /challenge/dont_run
hacker@processes~killing-processes:~$ ps -e
    PID TTY          TIME CMD
      1 ?        00:00:00 docker-init
      7 ?        00:00:00 /run/dojo/bin/s
    135 ?        00:00:00 su
    136 ?        00:00:00 bash
    137 ?        00:00:00 sleep
    148 ?        00:00:00 ttyd
    152 pts/0    00:00:00 bash
    164 pts/0    00:00:00 ps
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 10:56 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 10:56 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 10:56 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 10:56 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 10:56 ?        00:00:00 sleep 6h
hacker       148       1  0 10:56 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.
hacker       152     148  0 10:56 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       165     152  0 10:57 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{Qz0zKb1UcpTAwBQJ_G9TGg51gZu.QXyQDO0wSN5AzNzEzW}
```

## What I learned
I learned about kill cmd and how to use it.

## References 
None.
