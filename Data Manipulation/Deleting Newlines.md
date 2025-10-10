# Deleting Lines
The objective for this challenge is to delete newlines using tr command.

## My solve
**Flag:** `pwn.college{4rYaKh0tCwKB6k6BQi0asilT_h_.0VNxEzNxwSN5AzNzEzW}`

In this challenge I used -d attribute of tr and gave it value "\n" to delete the newlines in the output and get the flag.
```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{4rYaKh0tCwKB6k6BQi0asilT_h_.0VNxEzNxwSN5AzNzEzW}
```

## What I learned
I learned how to use escape sequences to delete special characters.

## References 
None.
