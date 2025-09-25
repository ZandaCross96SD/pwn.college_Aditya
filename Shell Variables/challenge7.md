# Reading Input
The objective for this challenge is to use user input using read command to set PWN to COLLEGE to get the flag.

## My solve
**Flag:** `pwn.college{YPuxem0_MuaFvQnhUYJaU4MKw1y.QX4cTN0wSN5AzNzEzW}`

In this challenge i used read command to input from user(me) into the variable PWN, the value COLLEGE, to get the flag.
```bash
hacker@variables~reading-input:~$ read -p "Enter : " PWN
Enter : COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{YPuxem0_MuaFvQnhUYJaU4MKw1y.QX4cTN0wSN5AzNzEzW}
```

## What I learned
I learned how to take user input using read command and how to specify its prompt message.

## References 
None.
