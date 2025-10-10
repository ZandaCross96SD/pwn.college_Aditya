# detatching and attatching
the objective for this challenge is to launch a screen detacth from it run a command and then attatch to it again to get the flag.

## My solve
**Flag:** `pwn.college{cuOauFNfIHqbQrvspoj3W0ZPEiQ.0lN4IDOxwSN5AzNzEzW}`

in this challenge i first launched the screen and then detatched from it suing ctrl+d;d and then ran the given command i then attatched to it again using screen -r to get the flag.
```
screen
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{cuOauFNfIHqbQrvspoj3W0ZPEiQ.0lN4IDOxwSN5AzNzEzW}
Yes! Flag is: pwn.college{cuOauFNfIHqbQrvspoj3W0ZPEiQ.0lN4IDOxwSN5AzNzEzW}
```
```bash
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
[detached from 147.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
Found detached screen session: 147.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
[screen is terminating]
```

## What I learned
i learened about detaching and how to use it using ctrl+a,d and reattatching it using screen -r.

## References 
None.
