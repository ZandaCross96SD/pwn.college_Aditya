# Storing Command Output
The objective of this challenge is to use command substituion to store the output of a command in a variable and access that variabe to fetch the value of flag.

## My solve
**Flag:** `pwn.college{EuWl6ScEtGvRKkdSB3g9dG7ax_P.QX1cDN1wSN5AzNzEzW}`

In this challenge I first assigned the output of command /challenge/run to PWN and then accessed it using cat to get the flag. I also tried to print using cat instead of echo to get the variables value, and the result was interesting.
```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ cat $PWN
cat: pwn.college{EuWl6ScEtGvRKkdSB3g9dG7ax_P.QX1cDN1wSN5AzNzEzW}: No such file or directory
```

## What I learned
In this challenge I learned about the method of Command substituion and how to use it to assign a commands' output to a variable.

## References 
None.
