# Helpful Programs
The objective of this challenge is to use -h or help argument to look up documentation of programs with no manual page and get the flag using information in it.

## My solve
**Flag:** `pwn.college{QXQMrSVJEe9KvsJCvttrB5sgUxD.QX3IDO0wSN5AzNzEzW}`

In this challenge I used the --help argument ot access the documentation for the program in which i found the hidden number 953 using the -p argument which i gave as teh value for -g argument to get the flag.
```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 953
hacker@man~helpful-programs:~$ /challenge/challenge -g 953
Correct usage! Your flag: pwn.college{QXQMrSVJEe9KvsJCvttrB5sgUxD.QX3IDO0wSN5AzNzEzW}
```

## What I learned
I learned about the --help argument for programs and how it can be used to get access to additional informatin about that program.

## References 
None.
