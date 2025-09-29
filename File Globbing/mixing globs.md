# Mixing Globs
The objective of this challenge is to match given 3 strings with less than 6 character passed as an argument to the program /challenge/run

## My solve
**Flag:** `pwn.college{opfNlUbIGUQBb2LvzW10AXjUl2L.QX1IDO0wSN5AzNzEzW}`

In this challenge I had some difficulty choosing the set of placeholders after some error i arrived at the solution.
```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *[in]*
Your expansion did not expand to the requested files (challenging, educational, 
pwning). Instead, it expanded to:
amazing beautiful challenging delightful educational fantastic incredible jovial kind laughing magical nice optimistic pwning queenly radiant splendid thrilling uplifting victorious wonderful xenial
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [pce]*[glg]
Error: your argument is too long! It must be 6 characters or less.
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [pce]*
You got it! Here is your flag!
pwn.college{opfNlUbIGUQBb2LvzW10AXjUl2L.QX1IDO0wSN5AzNzEzW}
hacker@globbing~mixing-globs:/challenge/files$ 
```

## What I learned
I revised previously learned concepts.

## References 
None.
