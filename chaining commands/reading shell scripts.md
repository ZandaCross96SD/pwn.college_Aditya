# reading shell scripts
the objective for this challenge is to read the given script adn tehn enter teh given passwd to get the flag.

## My solve
**Flag:** `pwn.college{0JnXUAn2LRCGcHDZqJAi8LaNvAV.0lMwgDOxwSN5AzNzEzW}`

in this challlenge i first catted the given scripts adn then antered the passwd written in guess to get the flag.
```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{0JnXUAn2LRCGcHDZqJAi8LaNvAV.0lMwgDOxwSN5AzNzEzW}
```

## What I learned
i learned how to reaad script files and how ti can be useful to get required data.

## References 
None.
