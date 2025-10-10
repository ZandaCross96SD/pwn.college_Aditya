# scripting with default cases
the objective forr this challenge is to use if conditional with else in your script to get the flag.

## My solve
**Flag:** `pwn.college{ske1yx7w1PwvQ1m50a97aAeTXZ6.01NzMDOxwSN5AzNzEzW}`

in this challenge i made the script as follows and then ran the command to get the output.
```
#!/bin/bash
if [ "$1" == "pwn" ]
then
    echo "college"
else
    echo "nope"
fi
```
```bash
hacker@chaining~scripting-with-default-cases:~$ ./solve.sh pwn
college
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{ske1yx7w1PwvQ1m50a97aAeTXZ6.01NzMDOxwSN5AzNzEzW}
```

## What I learned
i learned about else statemetnt and how to use it along with if in scripts to handle default case.

## References 
None.
