# Matching Paths with []
The objective for this challenge is to use [] in path to access specific files.

## My solve
**Flag:** `pwn.college{kJrS5pO6v7sTbMLfqCo7-7u6TNi.QX0IDO0wSN5AzNzEzW}`

In this challenge I first made the error of directly giving the files as the argument after reading the error message i again gave the complete path as an argument and got the flag.
```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run file_[bsah]
Error: you will need to specify the path to the files as part of your glob 
argument, since they are in a different directory than your current working 
directory!
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bsah]
You got it! Here is your flag!
pwn.college{kJrS5pO6v7sTbMLfqCo7-7u6TNi.QX0IDO0wSN5AzNzEzW}
```

## What I learned
I gained additional insight into how one can incorporate [] into paths .

## References 
None.
