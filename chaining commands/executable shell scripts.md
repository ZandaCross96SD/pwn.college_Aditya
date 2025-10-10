# executable shell scripts 
the objective for this challenge is to change the permissions of a script to run it without bash to get the flag.

## My solve
**Flag:** `pwn.college{om7ELe1D1pZI3gnGlOkCalKbdV2.QX0cjM1wSN5AzNzEzW}`

in this challenge i first made the file script.sh wiht the said command then listed its permissions after which i used chmod to make it executable to get the flag.
```bash
hacker@chaining~executable-shell-scripts:~$ ls -l script.sh
-rw-r--r-- 1 hacker hacker 16 Oct 10 15:05 script.sh
hacker@chaining~executable-shell-scripts:~$ chmod u+x script.sh
hacker@chaining~executable-shell-scripts:~$ script.sh
bash: script.sh: command not found
hacker@chaining~executable-shell-scripts:~$ ls
 COLLEGE   PWN   instructions   myflag         script.sh   the-flag  '~'
 Desktop   a     link           not-the-flag   the         x.sh
hacker@chaining~executable-shell-scripts:~$ ./script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{om7ELe1D1pZI3gnGlOkCalKbdV2.QX0cjM1wSN5AzNzEzW}
```

## What I learned
i learned hoe to make scripts executable.

## References 
None.
