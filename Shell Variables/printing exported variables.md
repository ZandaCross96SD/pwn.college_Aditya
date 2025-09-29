# Printing Exported Variables
The objective for this challenge is to print the value of a variable using env.

## My solve
**Flag:** `pwn.college{Q6isGWZOZrb8lkywYw58rPohbnk.QX4UTN0wSN5AzNzEzW}`

In this challenge I grepped the FLAG from the output of env command to get the flag.
```bash
hacker@variables~printing-exported-variables:~$ grep FLAG <(env)
FLAG=pwn.college{Q6isGWZOZrb8lkywYw58rPohbnk.QX4UTN0wSN5AzNzEzW}
```

## What I learned
I learned about env command and how it can be used to print every exported variable in the shell.

## References 
None.
