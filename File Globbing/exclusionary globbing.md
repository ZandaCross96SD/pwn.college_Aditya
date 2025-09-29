# Exclusionary Globbing
The objective of this challenge is to give the arguments as files whoes names don't start with p,w,or n.

## My solve
**Flag:** `pwn.college{cv5u-vYG1EFn9PdJ5IrfGj0_-p9.QX2IDO0wSN5AzNzEzW}`

Similar to previous problems, but instead it is asked to exclude set of characters here.
```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{cv5u-vYG1EFn9PdJ5IrfGj0_-p9.QX2IDO0wSN5AzNzEzW}
```

## What I learned
I learend how to use [!] to filter out files.

## References 
None.
