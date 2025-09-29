# catting absolute paths
## Objective
to use the cat command with absolute paths
## my solve
**flag:** `pwn.college{kj09wWjgEHCGAsdAG9a6VqCwDRR.QX5ETO0wSN5AzNzEzW}`  
much like the previous question i used cat to acces flag with the difference being i had to specify its absolute position 
```bash
hacker@commands~catting-absolute-paths:/$ ls
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~catting-absolute-paths:/$ cat ./flag
pwn.college{kj09wWjgEHCGAsdAG9a6VqCwDRR.QX5ETO0wSN5AzNzEzW}
```
## What i learned
what cat is in linux and how to use it with absolute paths.
## references
none.
