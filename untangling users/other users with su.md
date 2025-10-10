# other users with su
the objective for this challenge is to use su to switch to another user and thenn get the flag by running the givem process.

## My solve
**Flag:** `pwn.college{A4zS02gzM64u931EAIEBSk4DClO.QX2UDN1wSN5AzNzEzW}`

in this challenge i used su to seitch to zardus user and then ran the process given to get the flag.
```bash
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{A4zS02gzM64u931EAIEBSk4DClO.QX2UDN1wSN5AzNzEzW}
```

## What I learned
i leaerned how ot switch to another user using su.

## References 
None.
