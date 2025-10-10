# finding sessions
the objectvie for this challenge is to find the current screen sessions and then reattatch them to find the flag.

## My solve
**Flag:** `pwn.college{UgCLHsPVFWvRBr3Y7HCh1jWzFiX.01N4IDOxwSN5AzNzEzW}`


```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        144.session_b135ebba38912874    (Detached)
        147.session_91a2f9a40a012e71    (Detached)
        150.session_4a34d0560e3a7043    (Detached)
3 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_4a34d0560e3a7043
[screen is terminating]
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_91a2f9a40a012e71
[screen is terminating]
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{UgCLHsPVFWvRBr3Y7HCh1jWzFiX.01N4IDOxwSN5AzNzEzW}
pwn.college{UgCLHsPVFWvRBr3Y7HCh1jWzFiX.01N4IDOxwSN5AzNzEzW}
```

## What I learned
i learned how to list the current screen sessions and then launch a specific screen session suing screen -r name.

## References 
None.
