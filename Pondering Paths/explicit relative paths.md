# EXPLICIT RELATIVE PATHS, FROM /
OBJECTIVE:TO USE RELATIVE AND ABSOLUTE PATHS TO ACCESS FILES.
## MY SOLVE
**Flag** `pwn.college{goGFbUVMo5RcOkELPv7QtRLDBQZ.QXwUTN0wSN5AzNzEzW}`\
I accessed the run directory within challenge diectory within the root using relative path(./_) or absolute path since the current directory is the root directory.
```bash
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
```
## Tangents I went on
Initially I kept on using _ls_ to look at each directories because i was unable to comprehend what the challenge was trying to ask.
Found out there is a challenge directory and inside it there is a run directory, looked at the explanation for relative paths again and arrived at teh soolution.

## What I Learned
How to use . and .. as current or parent directory respectively.
## References
pwn.college explaination videos
