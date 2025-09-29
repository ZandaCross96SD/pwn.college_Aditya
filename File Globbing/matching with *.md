# Matching with *
THe objective of this challenge is to use * for changing directories in less than 4 character.

## My solve
**Flag:** `pwn.college{IgffwE2wzVS6MxLLMvOCGx5kIWD.QXxIDO0wSN5AzNzEzW}`

In this challenge i changed to the challenge directory using /ch and * as the placeholder for allengeholder, once in the directory i ran the given program.
```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{IgffwE2wzVS6MxLLMvOCGx5kIWD.QXxIDO0wSN5AzNzEzW}
```

## What I learned
I learned about * and how one can use it to avoid writing complete file names or paths.

## References 
None.
