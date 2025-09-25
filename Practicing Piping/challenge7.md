# Grepping Live Output
The objective of this challenge is to use pipe operator to simultaneously link the output of a command to the input of a command, and hence get the flag.

## My solve
**Flag:** `pwn.college{8rxqotqanUc5GJAlqFUGbTYeMQ9.QX5EDO0wSN5AzNzEzW}`

In this challenge I used the pipe operator to link the output of /challenge/run as an argument to grep to look for keyword pwn in the file which resulted in 5 matches teh second of which was teh flag.
```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn
pwn.college{8rxqotqanUc5GJAlqFUGbTYeMQ9.QX5EDO0wSN5AzNzEzW}
pwned
pwning
pwns
```

## What I learned
I learned about the pipe operator and how one can use it to avoid the usage of middle storage file.

## References 
None.
