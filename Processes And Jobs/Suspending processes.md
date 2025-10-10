# suspending processes
the objective for this challenge is to use ctrl+z to suspend the process in the background to get the flag.

## My solve
**Flag:** `pwn.college{MldyThEtOfpmyJ_UbHjieukYJ4s.QX1QDO0wSN5AzNzEzW}`

in this challenge i first ran the /challenge/run process adn then suspended it to background to run it again to get the flag.
```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 11:36 pts/0    00:00:00 bash /challenge/run
root         148     146  0 11:36 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 11:36 pts/0    00:00:00 bash /challenge/run
root         153     136  0 11:36 pts/0    00:00:00 bash /challenge/run
root         155     153  0 11:36 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{MldyThEtOfpmyJ_UbHjieukYJ4s.QX1QDO0wSN5AzNzEzW}
```

## What I learned
i learned about ctrl+z commands to suspend the process.

## References 
None.
