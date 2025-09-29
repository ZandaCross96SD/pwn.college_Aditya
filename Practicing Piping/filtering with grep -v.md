# Filtering with grep -v
The objective of this challenge is to use grep -v to filter out the lines that contain DECOY to get the flag.

## My solve
**Flag:** `pwn.college{Qh4yRg3tic7LVncvX8X1fZMUQ4X.0FOxEzNxwSN5AzNzEzW}`

I piped the output of /challenge/run to grep and then using -v filtered out the word DECOY to get the flag
```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{Qh4yRg3tic7LVncvX8X1fZMUQ4X.0FOxEzNxwSN5AzNzEzW}
```

## What I learned
I learned about grep -v command ad how to use it to filter out keywords.

## References 
None.
