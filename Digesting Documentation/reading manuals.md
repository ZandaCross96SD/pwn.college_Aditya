# Reading Manuals
This challenge asks us to use the man command to look up the manual for challenge/challenge and use the information in it to acquire teh flag.

## My solve
**Flag:** `pwn.college{MkNTB6xQ-ycl2hu_00oATONTkuD.QX0EDO0wSN5AzNzEzW}`

In this challenge i read the manual of the given command and used the argumentt kxyclh with argument 620 to get the flag.
```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --fortune
I was at this restaurant.  The sign said "Breakfast Anytime."  So I
ordered French Toast in the Rennaissance.
                -- Steven Wright
hacker@man~reading-manuals:~$ /challenge/challenge --kxyclh 620
Correct usage! Your flag: pwn.college{MkNTB6xQ-ycl2hu_00oATONTkuD.QX0EDO0wSN5AzNzEzW}
```

## What I learned
I learned how to access the manuals for different commands in linux through the man command and how to read the manual in the way it is formatted.

## References 
None.
