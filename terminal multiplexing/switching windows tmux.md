# switching windows(tmux)
the objective for this challenge is to launch tmux and then switch to the said window to get the flag.

## My solve
**Flag:** `pwn.college{IOjQesNczyh1nZnqKVbPYBHdkJL.0FM5IDOxwSN5AzNzEzW}`

in this challenge i first launched the tmux window and then used ctrl+b,0 to switch to window 0 to get the flag.
```bash
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux
   Welcome to the tmux window switching challenge!                                                                                                                                                                                  ┐
      You are currently in window 1.                                                                                                                                                     
      The flag is hidden in window 0.                                                                                                                                                    
      Use Ctrl-B 0 to switch to window 0!                                                                                                                                                
      MSG                                                                                                                                                                                
   Welcome to the tmux window switching challenge!                                                                                                                                      
   You are currently in window 1.                                                                                                                                                       
   The flag is hidden in window 0.                                                                                                                                                      
   Use Ctrl-B 0 to switch to window 0!
Here is your flag: pwn.college{IOjQesNczyh1nZnqKVbPYBHdkJL.0FM5IDOxwSN5AzNzEzW                                                                                                                                                   ┐
   }                                                                                                                                                                                    
      MSG                                                                                                                                                                                
   Excellent work! You found window 0!                                                                                                                                                  
   Here is your flag: pwn.college{IOjQesNczyh1nZnqKVbPYBHdkJL.0FM5IDOxwSN5AzNzEzW}                                                                                                      
   hacker@terminal-multiplexing~switching-windows-tmux:~$
```

## What I learned
i learned about window switching methods for tmux.

## References 
None.
