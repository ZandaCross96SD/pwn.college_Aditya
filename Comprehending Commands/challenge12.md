# making directories
the objective of this challenge is to use the mkdir command explained to make the said directories and touch a new blank file in it.

## My solve
**Flag:** `pwn.college{gTal-o0T5vw7hi3AttBJhTwL-8o.QXxMDO0wSN5AzNzEzW}`

I understood how to use the mkdir command to make directories in linux then i navigated to the said parent directory and made a subdirectory in it and subsequently otuched a file named college in it.
```bash
hacker@commands~making-directories:~$ cd /
hacker@commands~making-directories:/$ ls
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~making-directories:/$ cd /tmp
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  tmp.TpSOPGOVKK
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~making-directories:/tmp$ touch pwn/college
hacker@commands~making-directories:/tmp$ ls pwn
college
hacker@commands~making-directories:/tmp$ cd ..
hacker@commands~making-directories:/$ /challenge/run
Success! Here is your flag:
pwn.college{gTal-o0T5vw7hi3AttBJhTwL-8o.QXxMDO0wSN5AzNzEzW}
```

## What I learned
I learned about the mkdir command and how to use it to make directories in linux.

## References 
None.
