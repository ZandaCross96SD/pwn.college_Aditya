# grpups and files
the objective for this challenge is to chgrp to change the /flag's group from root to hacker to get teh flag.

## My solve
**Flag:** `pwn.college{odVG3UAAdsrfXFMXfZtdRVMgC1S.QXxcjM1wSN5AzNzEzW}`

in this challenge i used chgrp to change /flag's group to hacker and then catted it to get the flag.
```bash
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{odVG3UAAdsrfXFMXfZtdRVMgC1S.QXxcjM1wSN5AzNzEzW}
```

## What I learned
i learned about groups and their ownerships of files and how to use chgrp to change a file's group.

## References 
None.
