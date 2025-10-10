# adding commands
the on=bjective for this challenge is to change the path variable to our commands paths and then run the given command to get the flag.

## My solve
**Flag:** `pwn.college{spozklFNfc6515sOblG3GEZ2Jam.QX2cjM1wSN5AzNzEzW}`

in this challenge i made a lot of errors due to the difficult problme statement, i first used which cat to find the cat directory which was /run/dojo/bin/cat i then made the win file with the following contents, i then set the path variable to ~ since the win file was in here but runnig /challenege/run kept giving errors later i realized i hadn't made win executable i used chmod to make it executable and then set the PATH again and ran the command to get the flag.
```bash
#!/bin/bash
/run/dojo/bin/cat /flag

terminal
hacker@path~adding-commands:~$ PATH=/home/hacker /challenge/run
Invoking 'win'....
/challenge/run: line 4: win: command not found
It looks like that did not work... Did you set PATH correctly?
hacker@path~adding-commands:~$ chmod a+x /home/hacker/win
hacker@path~adding-commands:~$ PATH=/home/hacker /challenge/run
Invoking 'win'....
pwn.college{spozklFNfc6515sOblG3GEZ2Jam.QX2cjM1wSN5AzNzEzW}
```

## What I learned
i learned how to add my own commands to the PATH variable to run them in the terminal.

## References 
None.
