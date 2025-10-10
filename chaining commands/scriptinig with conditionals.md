# scripting with conditionals
the objective for this challenge is to use if then fi statements in your script to get the flag.

## My solve
**Flag:** `pwn.college{8rGONdkkIbLeX7Hy4_ihEtal3Oz.0lNzMDOxwSN5AzNzEzW}`

in this challenge i made the solve.sh file as follows and then ran the command to get the flag.
```
#!/bin/bash
if [ "$1" == "pwn" ]
then
    echo "college"
fi
```
```bash
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{8rGONdkkIbLeX7Hy4_ihEtal3Oz.0lNzMDOxwSN5AzNzEzW}
```

## What I learned
i learned about if conditional in bash scripts.

## References 
None.
