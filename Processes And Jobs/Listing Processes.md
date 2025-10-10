# Listing Processes
The objective for this challenge is to learn about processes and ps command and its attributes to get the flag.

## My solve
**Flag:** `pwn.college{ox50MTFdjJFzixRVWx3_AfLL7ac.QX4MDO0wSN5AzNzEzW}`

In this challenge I first used ps -ef to list all processes then used the name is the 3rd listing to get the flag.
```bash
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 10:47 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 10:47 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 10:47 ?        00:00:00 /challenge/4802-run-2771
root         135     132  0 10:47 ?        00:00:00 sleep 6h
hacker       146       1  0 10:47 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.
hacker       150     146  0 10:47 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       160     150  0 10:48 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/4802-run-2271
bash: /challenge/4802-run-2271: No such file or directory
hacker@processes~listing-processes:~$ /challenge/4802-run-2771
Yahaha, you found me! Here is your flag:
pwn.college{ox50MTFdjJFzixRVWx3_AfLL7ac.QX4MDO0wSN5AzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

## What I learned
I learned about processes and how to use ps to list them.

## References 
None.
