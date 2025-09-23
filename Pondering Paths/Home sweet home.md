# HOME SWEET HOME 
## OBJECTIVE 
to write a copy of the flag to any file you specify as an argument on the commandline, with these constraints:

    Your argument must be an absolute path.
    The path must be inside your home directory.
    Before expansion, your argument must be three characters or less.

## MY SOLVE
**Flag:** `pwn.college{MvOax0NXLV9aw_FR5trPeCVNV09.QXzMDO0wSN5AzNzEzW}`\
Given the constraints i gave the argument as  ~ /~  whixh is home/hacker/home/hacker which satisfied teh constraints.
```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/~
Writing the file to /home/hacker/~!
... and reading it back to you:
pwn.college{MvOax0NXLV9aw_FR5trPeCVNV09.QXzMDO0wSN5AzNzEzW}
```
## What I Learned
I learned about ~.
## Tangents I went on
None.
## References
None
