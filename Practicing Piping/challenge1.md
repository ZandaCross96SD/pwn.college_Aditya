# Redirecting Output
In this challenge the objective is to redirect stdout PWN to file COLLEGE.

## My solve
**Flag:** `pwn.college{AoQIDCKU3pcY_zrOzuNJOtq24nS.QX0YTN0wSN5AzNzEzW}`

In this challenge I echoed PWN and redirected the output to file COLLEGE.
```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{AoQIDCKU3pcY_zrOzuNJOtq24nS.QX0YTN0wSN5AzNzEzW}
```

## What I learned
I learned about stdout and how to redirect it to a file using > .

## References 
None.
