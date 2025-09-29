# Grepping Stored results
The objective of this challenge is to rdirect output of /challenge/run to a txt file and then search for the flag using grep inside it.

## My solve
**Flag:** `pwn.college{AFKozQ4ArrclX1yHaOTn8g7rXLr.QX4EDO0wSN5AzNzEzW}`

In this challenge I first redirected the output to the data.txt file and then using grep searched for teh keyword pwn in it to get the flag , in the first attempt i searched for flag keyword whihc resulted in a lot of matfches but not the flag.
```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn /tmp/data.txt
pwned
pwning
pwns
pwn
pwn.college{AFKozQ4ArrclX1yHaOTn8g7rXLr.QX4EDO0wSN5AzNzEzW}
```

## What I learned
I revisited previously lelarned concepts.

## References 
None.
