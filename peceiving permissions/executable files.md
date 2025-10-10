# executable files
the objective for this challenge is to give the user executable permissions for the given process to get teh flag.

## My solve
**Flag:** `pwn.college{YZe7OxYIg9GnIXRbjTgeo8G56gg.QXyEjN0wSN5AzNzEzW}`

in this challenge i first listed the permissions of the said process and then changes the groups and users permission to executable to get the flag.
```bash
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r--r--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ chmod gu+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{YZe7OxYIg9GnIXRbjTgeo8G56gg.QXyEjN0wSN5AzNzEzW}
```

## What I learned
i leatned more about chmod and how to use it to change permissions for a file/dir/etc.

## References 
None.
