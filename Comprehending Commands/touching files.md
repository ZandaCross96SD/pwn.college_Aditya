# touching files
The objective of this challenge is to use the touch command to create a new, blank file in your home directory. The challenge will then check for its existence to give you the flag.

## My solve
**Flag:** `pwn.college{M9YahlQMgxo43SrO9M3xMdLZIOE.QXwMDO0wSN5AzNzEzW}`

The challenge is very straightforward. It introduces the touch command and says to create a file with it. The problem states to create a blank file, so touch is the right tool for the job
```bash
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ touch ./pwn
hacker@commands~touching-files:/tmp$ cd ..
hacker@commands~touching-files:/$ /challenge/run
Success! Here is your flag:
pwn.college{M9YahlQMgxo43SrO9M3xMdLZIOE.QXwMDO0wSN5AzNzEzW}
```

## What I learned
I learned that the touch command is a simple and efficient way to create new, empty files in Linux.

## References 
None.
