# Deleteing Characters
The objective for this challenge is to use ttr commands to delete characters from a string output.

## My solve
**Flag:** `pwn.college{IXSeQRrv_X9OBA55T5Z8ESBBdoV.0FNxEzNxwSN5AzNzEzW}`

In this challenge I used the -d argument and gave it values ^% to get the flag.
```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{IXSeQRrv_X9OBA55T5Z8ESBBdoV.0FNxEzNxwSN5AzNzEzW}
```

## What I learned
I learned about tr command and its -d attribute.

## References 
None.
