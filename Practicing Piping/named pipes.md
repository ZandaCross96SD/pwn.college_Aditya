# Named Pipes
The objective for this challenge is to make a fifo file and redirect the output of a command into that file to get the flag.

## My solve
**Flag:** `pwn.college{wiGQhHNGcNei9jLbiAgD9lAWDHZ.01MzMDOxwSN5AzNzEzW}`

In this challenge I first created a fifo file using mkfifo command in the specified path and then redirected /challenge/run output to it then I opened a new terminal to cat the fifo file to get the flag.
```bash
TERMINAL 1
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo 
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!

TERMINAL 2
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{wiGQhHNGcNei9jLbiAgD9lAWDHZ.01MzMDOxwSN5AzNzEzW}
```

## What I learned
I learned about fifo files their nature and how they work in this challenge.

## References 
None.
