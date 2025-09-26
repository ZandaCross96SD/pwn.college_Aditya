# Writing to multiple programs
The objective for this challenge is to redirect the output of a command as input into two commands using piping and tee.

## My solve
**Flag:** `pwn.college{8IMazGSj8QZS4KVsj53NwOcffbt.QXwgDN1wSN5AzNzEzW}`

In this challenge I was stuck for a while trying to grasp what was going on , after a some thinking about how a tee command copies the pipe stream into files or programs and how piping works I arrived at this solution, in which I am first getting the output for the first command and then using pipe to redirect it to tee which then copies it to the two given commands to get the flag.
```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
167172050231138545
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{8IMazGSj8QZS4KVsj53NwOcffbt.QXwgDN1wSN5AzNzEzW}
```

## What I learned
I gained better understanding of piping and tee command.

## References 
None.
