# hidden files
The objective of this challenge is to use ls command with -a argument to list all the fiels(including hidden files) inside a directory and use that to find the flag.

## My solve
**Flag:** `pwn.college{okLmYKerRKpN-JcgVXpTxNsRDG9.QXwUDO0wSN5AzNzEzW}`

I used the ls command to list all the files within the root directory along with -a to get the flag. I then used teh cat to open the most likely file to get the flag.
 
```bash
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-22943140426114  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat ./.flag-22943140426114
pwn.college{okLmYKerRKpN-JcgVXpTxNsRDG9.QXwUDO0wSN5AzNzEzW}
```
## Tangents I went On
None.

## What I learned
I learned that files starting with . are hidden and arenot shown with just ls command adn one need to use -s with ls to get teh hidden files in linux.

## References 
None.
