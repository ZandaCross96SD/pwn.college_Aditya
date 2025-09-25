# Redirecting Input
The objective of this challenge is to use < to redirect input of files or programs to other programs.

## My solve
**Flag:** `pwn.college{gpWABeAssGBjZg3bX5ddHdT1c3l.QXwcTN0wSN5AzNzEzW}`

In this challenge I first made the file PWN store COLLEGE and then i gave the input of that to /challenge/run.
```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{gpWABeAssGBjZg3bX5ddHdT1c3l.QXwcTN0wSN5AzNzEzW}
```

## What I learned
I learned how similar to redirecting output stream you can redirect input streams as well in linux.

## References 
None.
