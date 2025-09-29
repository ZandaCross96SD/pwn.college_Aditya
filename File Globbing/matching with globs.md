# Multiple Globs
The objective of this challenge is to combine multiple globs to access set of files.

## My solve
**Flag:** `pwn.college{A5dtCbqoKE8YDOkvxr6vkazOxj6.0lM3kjNxwSN5AzNzEzW}`

Again this challenge was pretty straightforward , I cd to the said directory and then ran the program with argument of all files that have p in it.
```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{A5dtCbqoKE8YDOkvxr6vkazOxj6.0lM3kjNxwSN5AzNzEzW}
```

## What I learned
I learned how i canuse multiple globs to refer to paths or files.

## References 
None.
