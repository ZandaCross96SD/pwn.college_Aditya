# removing files
The objective of this challenge is to use the rm command to delete a file named delete_me that has been created in your home directory. A check will then verify that the file is gone.

## My solve
**Flag:** `pwn.college{o0DjktObC5b5dZ8LP8w5x40wy2e.QX2kDM1wSN5AzNzEzW}`

 This is the opposite of the touch challenge. The goal is to remove a file. The challenge explicitly mentions the rm command and the file's name, delete_me. I'll use ls first to confirm the file's presence and then rm to remove it.
 
```bash
hacker@commands~removing-files:~$ ls
 delete_me  '~'
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{o0DjktObC5b5dZ8LP8w5x40wy2e.QX2kDM1wSN5AzNzEzW}
```
## Tangents I went On
None.

## What I learned
I learned how to use the rm command to remove files from the filesystem. This is a powerful command and I need to be cautious with it, as it permanently deletes files without a "recycle bin" or "trash" like in a graphical environment.

## References 
None.
