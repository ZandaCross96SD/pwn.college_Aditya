# changing permissions
the objective for this challenge is to use chmod to change a files permissions to get the flag.

## My solve
**Flag:** `pwn.college{M8X0gnCr9yukHJnMu5xgLJ9VRH3.QXzcjM1wSN5AzNzEzW}`

in this challenge i first lilsted the permissions of /flag and then changed its permissions to allow all others read access and then read it to get the flag.
```bash
hacker@permissions~changing-permissions:~$ ls -l /flag
-rwxrwx--- 1 root root 60 Oct 10 13:12 /flag
hacker@permissions~changing-permissions:~$ chmod o+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{M8X0gnCr9yukHJnMu5xgLJ9VRH3.QXzcjM1wSN5AzNzEzW}
```

## What I learned
i learned about chmod and how to use it to change a files permissions.

## References 
None.
