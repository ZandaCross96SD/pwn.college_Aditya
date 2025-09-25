# Reading Files
The objective of this challenge is to redirect the input stream of /challenge/read_me into the variable PWN for the read command to get the flag.

## My solve
**Flag:** `pwn.college{cD8SjC1IRY_ZL7wEAHyN-WM6nt5.QXwIDO0wSN5AzNzEzW}`

In this challenge I redirected the input stream of the said file into PWN with read command to get the flag.
```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{cD8SjC1IRY_ZL7wEAHyN-WM6nt5.QXwIDO0wSN5AzNzEzW}
```

## What I learned
i learned how to read files into varibles in this challenge.

## References 
None.
