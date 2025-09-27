# Position Elsewhere
The objective for this challenge is to change the directory and then run a progrma from that directory using cd.

## My solve
**Flag:** `pwn.college{Q9rZx4mj4-iRtdiLLzzr1t-XRTo.QX3QTN0wSN5AzNzEzW}`

In this challenge i ran the program first and then changed to the mentioned directory to run the program again to get the flag.
```bash
hacker@paths~position-elsewhere:/$ /challenge/run
Incorrect...
You are not currently in the /home directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:/$ cd /home
hacker@paths~position-elsewhere:/home$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Q9rZx4mj4-iRtdiLLzzr1t-XRTo.QX3QTN0wSN5AzNzEzW}
```

## What I learned
I learned about cd.

## References 
None.
