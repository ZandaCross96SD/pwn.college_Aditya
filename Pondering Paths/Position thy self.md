# POSITION THY SELF
OBJECTIVE:TO CHANGE DIRECTORIES AND RUN PROGRAMS IN IT WITH CD
## MY SOLVE
**Flag** `pwn.college{c6vY9zc7x0rLF_PzxzXIo52btFT.QX2QTN0wSN5AzNzEzW}`

in this challenge I changed to the mentioned directory and then ran the command to get the flag.
```bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /use/share/doc
bash: cd: /use/share/doc: No such file or directory
hacker@paths~position-thy-self:~$ cd /usr/share/doc
hacker@paths~position-thy-self:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{c6vY9zc7x0rLF_PzxzXIo52btFT.QX2QTN0wSN5AzNzEzW}

```
## Tangents I went on
None.
## What I Learned
How to use cd to change directories.
## References
pwn.college explaination videos
