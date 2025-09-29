# Split piping stderr and stdout
The objective for this challenge is to redirect a programs stdout as stdin for a program and its stderr to stdin of another program.

## My solve
**Flag:** `pwn.college{kJ5jhJiGLMqEsDY7bh1B24ot4eD.QXxQDM2wSN5AzNzEzW}`

After struggling a lot with this challenge and eventually taking help I realized what I was doing wrong, instead of using 2> > to redirect /challenge/hack's stderr as **stdin** of /challenge/the I was treating it like a file and simply writing /challenge/hacks output to /challenge/the , after that redirecting stdout to /challenge/planet was straightforward.
```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) | /challenge/planet
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{kJ5jhJiGLMqEsDY7bh1B24ot4eD.QXxQDM2wSN5AzNzEzW}
```

## What I learned
I learned about the difference redirecting to a file versus redirecting to a program and learned how to split pipe stderr and stdout to two different programs.

## References 
None.
