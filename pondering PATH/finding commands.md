# finding commands
the objective for this challenge is to use which command to find the directory of win command and then cat the flag in the same directory to get the flag.

## My solve
**Flag:** `pwn.college{s3n06bjlIJcXQmEKU7YYPjuVG0r.01NzEzNxwSN5AzNzEzW}`

in this challenge i first used which on win which gave me a directory i then catted the flag in the same directory to get the flag.
```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/23231/win
hacker@path~finding-commands:~$ cat /challenge/p*/23231/fl*
pwn.college{s3n06bjlIJcXQmEKU7YYPjuVG0r.01NzEzNxwSN5AzNzEzW}
```

## What I learned
i learned about which command and how to use it to find the path of a command.

## References 
None.
