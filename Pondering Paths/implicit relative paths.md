# IMPLICIT RELATIVE PATHS, FROM /
OBJECTIVE:TO USE RELATIVE PATH TO ACCESS A FILE.
## MY SOLVE
**Flag** `pwn.college{AEKHSNu2_d5CBn0ii_A-0h8gjbk.QX5QTN0wSN5AzNzEzW}`
In this challenge I first changed directory to the root and then using relative path accessed run from it to get the flag.
```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{AEKHSNu2_d5CBn0ii_A-0h8gjbk.QX5QTN0wSN5AzNzEzW}
```
## Tangents I went on
None.
## What I Learned
How to use relative paths and the difference between relative and absolute paths.
## References
pwn.college explaination videos
