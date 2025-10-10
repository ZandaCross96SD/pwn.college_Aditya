# starting backgrounded processes
the objective for this challenge is to start the process backgrounded from the start using & to get teh flag.

## My solve
**Flag:** `pwn.college{sPr8DS01dQNyZs_R-sIY66iHept.QX5QDO0wSN5AzNzEzW}`

in thiss challenge i ran the process along with & to run it in the background to get the flag.
```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 146
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{sPr8DS01dQNyZs_R-sIY66iHept.QX5QDO0wSN5AzNzEzW}
^C
[1]+  Done                    /challenge/run
```

## What I learned
i leared how to use & to start processes in the background.

## References 
None.
