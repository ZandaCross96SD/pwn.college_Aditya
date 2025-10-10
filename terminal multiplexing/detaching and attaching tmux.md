# detaching and attaching
the objective for this challenge is to launch temrinal multiplexer using tmux and detach from it run the said command and the reattach to it to get the flag.

## My solve
**Flag:** `pwn.college{wPcloe-sIMxooE4S7z-r7t_1Rbh.0VO4IDOxwSN5AzNzEzW}`

in this challenge i first launched tmux and then detached from it using ctrl+b,d then ran the given command then attatched to it again using tmux a.
```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{wPcloe-sIMxooE4S7z-r7t_1Rbh.0VO4IDOxwSN5AzNzEzW}
Congratulations, here is your flag: pwn.college{wPcloe-sIMxooE4S7z-r7t_1Rbh.0VO4IDOxwSN5AzNzEzW}
```

## What I learned
i learend about tmux and how to attach detach and retach to it.

## References 
None.
