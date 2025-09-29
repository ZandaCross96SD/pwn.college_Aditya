# moving files
## Objective
This challenge wants me to use the mv command in linux to move the file /flag into /temp/hack-the-panet.
## my solve
**flag:** `pwn.college{EfDHgWBV5MKX9KTmyjXqWfVawbx.0VOxEzNxwSN5AzNzEzW}`

 I moved the file with mv command from and to the mentioned directories and then i ran the check command in challeenge to get the flag
```bash

hacker@commands~moving-files:/$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:/$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{EfDHgWBV5MKX9KTmyjXqWfVawbx.0VOxEzNxwSN5AzNzEzW}

```
## What i learned
I learned the mv command and how it can be used to move files in linux.
## references
none.
