# linking files
This challenge asks us to use the symbolic link [ln -s _] command to trick the challenge/catflag program into reading and displaying the flag.

## My solve
**Flag:** `pwn.college{Q-V0I8AzdaKnvdbU-BckQbzThl0.QX5ETN1wSN5AzNzEzW}`

In this problem I used the cat to read what was there in challenge/catflag it pointed to ~/not-the-flag so i deleted that file and created a new linked file with the same name that pointed to the /flag file after running the /challenge/catflag I got the flag.
```bash
hacker@commands~linking-files:~$ cat /challenge/catflag
#!/opt/pwn.college/bash

fold -s <<< "About to read out the /home/hacker/not-the-flag file!"
cat /home/hacker/not-the-flag
hacker@commands~linking-files:~$ rm not-the-flag
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{Q-V0I8AzdaKnvdbU-BckQbzThl0.QX5ETN1wSN5AzNzEzW}
```

## What I learned
I learned about linked files and how one can link them in linux. there are two ways in which files can be linked a soft link and a hard link; A hard link is just an alias or a different name fore the same file while the soft link is a different file that points to another files' paths.

## References 
None.
