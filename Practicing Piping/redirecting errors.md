# Redirecting errors
The objective of this challenge is to redirect the standard error stream into instructions and standard output stream into myflag.

## My solve
**Flag:** `pwn.college{070xr1ecp_rdJed0dkFryUEIgX2.QX3YTN0wSN5AzNzEzW}`

I first redirected the output of the program to myflag and then redirected the error stream to instructions file using fd2 stderr.
```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{070xr1ecp_rdJed0dkFryUEIgX2.QX3YTN0wSN5AzNzEzW}
```

## What I learned
I learned about file descriptors and their numbering system and how to use it to redirect different streams into different files.

## References 
None.
