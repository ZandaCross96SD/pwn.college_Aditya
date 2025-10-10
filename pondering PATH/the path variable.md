# the path variable
the obbjective for this challenge is to set PATH variabel to empty get the flag.

## My solve
**Flag:** `pwn.college{kWoV4ujkShrvHBMRVNkn5VS02zw.QX2cDM1wSN5AzNzEzW}`

in this challenge i set the path variable empty so that /challenge/run cant find the rm command to remove the flag and then ran the command to get the flag.
```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{kWoV4ujkShrvHBMRVNkn5VS02zw.QX2cDM1wSN5AzNzEzW}
```

## What I learned
i learend about PATH vatriable and its function.

## References 
None.
