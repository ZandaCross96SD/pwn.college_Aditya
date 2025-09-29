# Searching Manuals
The objective of this challenge is to search through the manual to get the argument that gets you the flag

## My solve
**Flag:** `pwn.college{UBbZ5x-SvL1-SuhNRuO1KEavApQ.QX1EDO0wSN5AzNzEzW}`

In this challenge i accessed the manual using the man like in the previous challenge and then used [ / ] to search within the manyual page the keyword flag , the first result i got was not thte correct one so i moved to the second one with n which gave me the correct argument.
```bash
hacker@man~searching-manuals:~$ man challenge

gzip: stdout: Broken pipe
hacker@man~searching-manuals:~$ /challenge/challenge --zwl
Initializing...
Correct usage! Your flag: pwn.college{UBbZ5x-SvL1-SuhNRuO1KEavApQ.QX1EDO0wSN5AzNzEzW}
```

## What I learned
I learned how to make searching through manuals easier by using [ / ] and n , N to navigate throught the manual.

## References 
None.
