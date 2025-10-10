# hijacking commands
the objective for this command is to change the rm definition by replacing PATH with out own rm to get the flag.

## My solve
**Flag:** `pwn.college{Ete_1FLRSJHmq_pcbajyyRk-g6U.QX3cjM1wSN5AzNzEzW}`

this challenge was also a head scratcher, i first knew that we had to change rm definition and replave it so that instead of deleting the argument passed to it, it prints it but there were many errors along the way in making the script after a little help online i made the script such that it parses through all of its arguments and then prints the flag if the argument is flag instead of deleting it i then made rm executable and after setting the path i ran the command to get the flag.
```bash
rm
#!/bin/sh
for arg in "$@"; do
  if [ "$arg" = "/flag" ] || [ "$arg" = "/flag/" ]; then
    /bin/cat /flag
  fi
done
terminal
hacker@path~hijacking-commands:~$ chmod +x ./rm
hacker@path~hijacking-commands:~$ PATH=/home/hacker /challenge/run
Trying to remove /flag...
pwn.college{Ete_1FLRSJHmq_pcbajyyRk-g6U.QX3cjM1wSN5AzNzEzW}
```

## What I learned
I gained a deeper understanding of path variables and scripting and how to use them to replave command defintions.

## References 
None.
