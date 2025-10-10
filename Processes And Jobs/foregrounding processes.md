# froegrounding processes
the objective for this challenge is to use fg and bg together to background a process and tehn bring it to the foreground again to get the flag.

## My solve
**Flag:** `pwn.college{EaUmJ3iqA1t6HG4J_-rd3Fu_Js-.QX4QDO0wSN5AzNzEzW}`

in this process i frist ran the process suspended it then backgrounded it and then used fg to bring it to froeground again to get teh flag.
```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{EaUmJ3iqA1t6HG4J_-rd3Fu_Js-.QX4QDO0wSN5AzNzEzW}
```

## What I learned
i learned more about the usage of bg and fg.

## References 
None.
