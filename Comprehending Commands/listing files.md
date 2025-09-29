# Listing Files
## Objective
to use the ls command to find out the flag
## my solve
**flag:** `pwn.college{s6Z_67jhWH1PXNzUAacHKkZXJ4K.QX4IDO0wSN5AzNzEzW}`

 I used ls on challenge to find out the files in it then i changed cwd to challenge and then accessed the only other file beside DESCRIPTION.
 
```bash

hacker@commands~listing-files:~$ ls /challenge
367-renamed-run-11464  DESCRIPTION.md
hacker@commands~listing-files:~$ cd /challenge
hacker@commands~listing-files:/challenge$ ./367-renamed-run-11464
Yahaha, you found me! Here is your flag:
pwn.college{s6Z_67jhWH1PXNzUAacHKkZXJ4K.QX4IDO0wSN5AzNzEzW}
```
## Tangents I went on
I initially tried to use cat to list the contents in the random named file, and I kept getting the message
```bash
hacker@commands~listing-files:/challenge$ cat 367-renamed-run-11464
#!/opt/pwn.college/bash

echo "Yahaha, you found me! Here is your flag:"
cat /flag
```
I later realized that I needed to access it using ./  .
## What i learned
what is ls and how to use it to list files or subdiirectories within directories within Linux.
## references
none.
