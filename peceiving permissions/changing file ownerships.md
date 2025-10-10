# changing file ownerships
the objective for this challenge is to chown to change the owner of flag to hacker and then read it to fet the flag.

## My solve
**Flag:** `pwn.college{Y7KXrFZKi8O-dYHbhwvjBeCRP31.QXxEjN0wSN5AzNzEzW}`

in this challenge i used chown to change ownership of /flag to hacker and then read it to get teh flag.
```bash
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{Y7KXrFZKi8O-dYHbhwvjBeCRP31.QXxEjN0wSN5AzNzEzW}
```

## What I learned
i learned about and how to use it to lchange a files ownerships.

## References 
None.
