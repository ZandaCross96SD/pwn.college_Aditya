# the suid bit
the objective for this cahllenge is to use chmod to set suid bit for /challenge/getroot to get root and then cat the flag.

## My solve
**Flag:** `pwn.college{UiYgvK9LKTDhMWrm0h6QglzUYk9.QXzEjN0wSN5AzNzEzW}`

in this challenge i first ran the said program nothing happended so i then set its suid using chmod to open root shell after which i read not-the-flag file to get the flag(the flag was in not-the-flag in a similar previous challenge.)
```bash
hacker@permissions~the-suid-bit:~$ /challenge/getroot
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# /flag
bash: /flag: Permission denied
root@permissions~the-suid-bit:~# chmod a=r /flag
This challenge restricts chmod to ONLY work on /challenge/getroot! You may not 
chmod any other file in this challenge.
root@permissions~the-suid-bit:~# ls
 COLLEGE   Desktop   PWN   a   instructions   link   myflag   not-the-flag   the   the-flag  '~'
root@permissions~the-suid-bit:~# cat not-the-flag
pwn.college{UiYgvK9LKTDhMWrm0h6QglzUYk9.QXzEjN0wSN5AzNzEzW}
```

## What I learned
i learned about suid and how to use chmod to set suid for a prpgram.

## References 
None.
