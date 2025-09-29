# Grepping Errors
The objective of this challenge is to pipe stderr stream into pipe stream whihc only takes stdouot using file descriptor redirection to get the flag.

## My solve
**Flag:** `pwn.college{kRSiUAnioxxFkBMD2WkHlTpsLEN.QX1ATO0wSN5AzNzEzW}`

In this cahllenge I got the flag by following the procedure and somwwhat understanding whats going on, but had to google and use geminis help to really understand what was going on here, so 2> redirects the standard error and &1 says to redirect it to the same location as file descriptor 1 standard output stream which is then used with pipe to grep the flag.
```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwning
pwn.college{kRSiUAnioxxFkBMD2WkHlTpsLEN.QX1ATO0wSN5AzNzEzW}
pwns
pwn
pwned
```

## What I learned
In this challenge, I learned about file descriptors in more depth, learned about & and how it can be used to get file locations, and how one can pipe stderr stream.

## References 
None.
