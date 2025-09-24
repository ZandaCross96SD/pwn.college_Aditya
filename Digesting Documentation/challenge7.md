# Help for builtins
The objective of this challenge is to use help builtin command to get access to information about other builtin commands

## My solve
**Flag:** `pwn.college{s_HP8NRE1WaRCYR1eljFUxi2_1O.QX0ETO0wSN5AzNzEzW}`

In this challenge i used the help command to lookup challenge (now a builtin command) i then used teh secret value and passed it as the argument for the argument secret which gave the flag.
```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "s_HP8NRE".
hacker@man~help-for-builtins:~$ challenge --secret s_HP8NRE
Correct! Here is your flag!
pwn.college{s_HP8NRE1WaRCYR1eljFUxi2_1O.QX0ETO0wSN5AzNzEzW}
```

## What I learned
I learned about the help command for builtin commands and what builtin commands are in Linux.

## References 
None.
