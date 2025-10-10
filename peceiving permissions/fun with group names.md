# fun with group names
the objective for this challenge is to find out the group the user hacker is in and then change /flag's group to that to get the flag.

## My solve
**Flag:** `pwn.college{8DIDcD2vMId0Fx0S04mlRzCXYkN.QXycjM1wSN5AzNzEzW}`

in this challenge i used id to find the current users group and then changed /flag's group to that group to get the flag.
```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp14665) groups=1000(grp14665)
hacker@permissions~fun-with-groups-names:~$ chgrp grp14665 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{8DIDcD2vMId0Fx0S04mlRzCXYkN.QXycjM1wSN5AzNzEzW}
```

## What I learned
i learned more about groups and id command.

## References 
None.
