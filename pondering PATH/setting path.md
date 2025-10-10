# setting path
the objective for this challenge is to set the PATH variable to the given directory to directly invoke the command and get the flag.

## My solve
**Flag:** `pwn.college{wgEzCJzupEsCj_AX1k6wvj9V_VF.QX1cjM1wSN5AzNzEzW}`

in this challenge i set the path variable to the given path and then ran the command to get the flag.
```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{wgEzCJzupEsCj_AX1k6wvj9V_VF.QX1cjM1wSN5AzNzEzW}
```

## What I learned
i learned about how to set PATH variable to a directory to look for needed commands.

## References 
None.
