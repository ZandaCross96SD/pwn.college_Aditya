# scripting with multiple conditions
the objective for this challenge is to use multiple condiotonals using elif along with if to get the flag.

## My solve
**Flag:** `pwn.college{IKYsPFte0V6Y54-zJm1y3RG143g.0FOzMDOxwSN5AzNzEzW}`

in this challenge i made the script file as follows and then ran the said command to get the flag.
```
#!/bin/bash
if [ "$1" == "hack" ]
then
    echo "the planet"
elif [ "$1" == "pwn" ]
then
    echo "college"
elif [ "$1" == "learn" ]
then
    echo "linux"
else
    echo "unknown"
fi
```
```bash
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{IKYsPFte0V6Y54-zJm1y3RG143g.0FOzMDOxwSN5AzNzEzW}
```

## What I learned
i learned about how to incorporrate multiple conditions in if using elif in a script.

## References 
None.
