# Searching For Manuals
The objective of this challenge is to read through the manual for man command and use the information in it to look up the manual for the /challenge program adn then get the flag.

## My solve
**Flag:** `pwn.college{0uLu8edBXIFkudryLQ2_mJAFMk5.QX2EDO0wSN5AzNzEzW}`

In this challenge I first read the manual for man command after which I initially searched for terms like flag , but then remembered that this is an independant command outside of this challenge so it wouldnt contain references to flag after that i just kept reading the commands until in the examples section there was a mention of k which searches manual description and names for strings in which i typed /challenge i got a random string of characters which i assumed to be the argument but that wasn't it i then looked up the manual for that string in which there was an argument to get the flag, that's how i arrived at the solution.
```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k /challenge
uuedkudrym (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man uuedkudrym
hacker@man~searching-for-manuals:~$ /challenge/challenge --uuedku 082
Correct usage! Your flag: pwn.college{0uLu8edBXIFkudryLQ2_mJAFMk5.QX2EDO0wSN5AzNzEzW}
```

## What I learned
I learned about you can use -k with man to search for keywords in manual descriptions along with few other arguments.

## References 
None.
