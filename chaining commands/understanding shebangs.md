# understanding shebangs
the objective for this challenge is to use #! in a file solve.sh and run the said command to get the flag.

## My solve
**Flag:** `pwn.college{ElLwMS3jGleWfQDKB9kRX-EUiu5.0VOzMDOxwSN5AzNzEzW}`

in this challenge i first made the solve.sh file with #!/bin/bash as the first line and the given cmd as the 2nd line i then changed it permission to executable and then rn the program to get the flag.
```bash
hacker@chaining~understanding-shebangs:~$ chmod a+x solve.sh
hacker@chaining~understanding-shebangs:~$ ./solve.sh
hack the planet
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{ElLwMS3jGleWfQDKB9kRX-EUiu5.0VOzMDOxwSN5AzNzEzW}
```

## What I learned
i learned about interpreter paths and interpreted programs and how to use shebang to execute them.

## References 
None.
