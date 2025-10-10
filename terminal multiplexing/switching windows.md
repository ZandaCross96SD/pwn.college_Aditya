# switching windows
the objective for this challenge is to use shortcuts inside screen to get the flag.

## My solve
**Flag:** `pwn.college{MRqokhb1fcXI0ztdKnJAMl-z6R-.0FO4IDOxwSN5AzNzEzW}`

in this challenge i first reattached the screen and then switched to window 0 using ctrl+a,0 to get the flag.
```bash
hacker@terminal-multiplexing~switching-windows:~$ screen -r
[screen is terminating]
Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!
MSG
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Welcome to the window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-A 0 to switch to window 0!
> MSG
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{MRqokhb1fcXI0ztdKnJAMl-z6R-.0FO4IDOxwSN5AzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{MRqokhb1fcXI0ztdKnJAMl-z6R-.0FO4IDOxwSN5AzNzEzW}
```

## What I learned
i learned about screen shortcuts.

## References 
None.
