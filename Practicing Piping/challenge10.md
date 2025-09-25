# Duplicating Piped Data with Tee
The objective of this challenge is to use the tee command to check the pipe stream for data to get the hint for the flag.

## My solve
**Flag:** `pwn.college{0En1I1_Kb5r-kvkDc-e9VH-RX9V.QXxITO0wSN5AzNzEzW}`

In this challenge I first ran the incorrect program ch*/run instead of ch*/pwn by mistake, after reading the error message i used tee to copy the contents to /challenge/secret after reading teh secret file I added the said argument with the value to get the flag.
```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/run | tee a | /challenge/college
bash: /challenge/run: No such file or directory

/challenge/secret needs to the on the receiving end of the output of 
'/challenge/pwn' (or 'tee' for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ 
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee /challenge/secret | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat /challenge/secret
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "0En1I1_K"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret 0En1I1_K | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{0En1I1_Kb5r-kvkDc-e9VH-RX9V.QXxITO0wSN5AzNzEzW}
```

## What I learned
I learned about tee command and how to use it for debugging pipe statements.

## References 
None.
