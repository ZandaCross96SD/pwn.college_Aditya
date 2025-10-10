# Translating Characters
The objective of this challenge is to use tr comd to get the flag.

## My solve
**Flag:** `pwn.college{c3Cr5-ziIjin8gfPxY6DxoBdZBi.01MxEzNxwSN5AzNzEzW}`

In this challenge I created two strings conating all the alphabets in small and upper case and then in the next strring swapped their places to get the flag.
```bash
hacker@data~translating-characters:~$ /challenge/run | tr abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghi
jklmnopqrstuvwxyz
yOUR CASE-SWAPPED FLAG:
pwn.college{c3Cr5-ziIjin8gfPxY6DxoBdZBi.01MxEzNxwSN5AzNzEzW}
```

## What I learned
I learned about tr command.

## References 
None.
