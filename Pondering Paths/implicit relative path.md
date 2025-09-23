# IMPLICIT RELATIVE PATH 
## OBJECTIVE 
to execute a program in the current directory, using . like in the previous levels
## MY SOLVE
**Flag:** `pwn.college{ID866EIv3URzjS3fSMEtEzrZeWF.QXxUTN0wSN5AzNzEzW}`

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
```
## What I Learned
I learned that Linux has a complex namespace where even though you are in the directory using a program in it need for it to be mentioned with relative path and not naked path
## Tangents I went on
None.
## References
None
