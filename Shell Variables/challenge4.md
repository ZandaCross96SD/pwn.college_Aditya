# Exporting Variables
The objective for this challenge is to export a variabel and then run a program using it.

## My solve
**Flag:** `pwn.college{sN5A2jnkxpCswNh0kg7MPD8HQM0.QXyYTN0wSN5AzNzEzW}`

In this challenge i first exported PWN variable set to value COLLEGE and then set COLLEGE to value PWN w/o exporting it, I then invoked the program /challenge/run with PWN to get the flag.
```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run PWN
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{sN5A2jnkxpCswNh0kg7MPD8HQM0.QXyYTN0wSN5AzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

## What I learned
explain what you learned

## References 
None.
