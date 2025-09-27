# Position yet Elsewhere
The objective for this challenge is to change directory into a specified path and run a program from there.

## My solve
**Flag:** `pwn.college{w_efbiLKzIWsSIP9Ch3PDFFVo-C.QX4QTN0wSN5AzNzEzW}`

In this challenge i first ran the program and then changed directory to the mentioned path to run the progrma again to get the flag.
```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /proc/138/fd directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /proc/138/fd
hacker@paths~position-yet-elsewhere:/proc/138/fd$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{w_efbiLKzIWsSIP9Ch3PDFFVo-C.QX4QTN0wSN5AzNzEzW}
```

## What I learned
I learned about changing directories.

## References 
None.
