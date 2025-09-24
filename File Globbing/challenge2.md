# Matching with ?
In this challenge the objective is to use the placeholder ? to change directories and then get the flag.

## My solve
**Flag:** `pwn.college{4qB6Vki6ocNohmLohqrbkRpESDx.QXyIDO0wSN5AzNzEzW}`

This challenge was pretty straightforward and similar to the previous one i used placeholder ? but instead only for a single character here.
```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{4qB6Vki6ocNohmLohqrbkRpESDx.QXyIDO0wSN5AzNzEzW}
```

## What I learned
I learned about ? and how you can use it to standin as a placeholder for a single character.

## References 
None.
