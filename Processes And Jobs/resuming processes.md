# resuming processes
the objective for this challenge is to use fg command to resume the suspended process to get teh flag.

## My solve
**Flag:** `pwn.college{wiyuV3GaVOrd7jsHEWy7GCmkZ9k.QX2QDO0wSN5AzNzEzW}`

in this challenge i first ran the given cmd suspended it and then used fg to bring ti back to get teh flag.
```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{wiyuV3GaVOrd7jsHEWy7GCmkZ9k.QX2QDO0wSN5AzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

## What I learned
i learned about fg cmd and how to use it to resume suspended processes

## References 
None.
