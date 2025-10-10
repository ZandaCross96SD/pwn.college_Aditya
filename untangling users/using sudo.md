# using sudo
the objective for this challenge is to use sudo to get teh flag as root user.

## My solve
**Flag:** `pwn.college{oOG_JkSkZo6EFcqil4zmgfiDJKX.QX4UDN1wSN5AzNzEzW}`

in this challenge i used sudo to list the directories and then read flag file to get the flag.
```bash
hacker@users~using-sudo:~$ sudo ls /
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@users~using-sudo:~$ sudo cat flag
cat: flag: No such file or directory
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{oOG_JkSkZo6EFcqil4zmgfiDJKX.QX4UDN1wSN5AzNzEzW}
```

## What I learned
i learned about sudo cmd and how to use it gain root access for a cmd.

## References 
None.
