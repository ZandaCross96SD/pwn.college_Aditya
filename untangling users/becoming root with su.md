# becoming root with su
the objective for this challenge is to use su cmd to gain access to root and then do some inspection to get the flag.

## My solve
**Flag:** `pwn.college{IEsqTHbPQmcKbVjp8jwcQYd9T4L.QX1UDN1wSN5AzNzEzW}`

in this challenge i first gained access to root with su cmd and then inputted the given pwd after which i listed the directories after catting some ffiles and failing i arrived at the correct not-the-flag file whch contained the real flag.
```bash
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# ls
 COLLEGE   Desktop   PWN   a   instructions   link   myflag   not-the-flag   the   the-flag  '~'
root@users~becoming-root-with-su:/home/hacker# cat the-flag
 | 
\|/ This is the first half:
 v 
pwn.college{EqYj-5u8yPJWBljuJP4Wx0FVYL_.QX3ATO0wSN5AzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
root@users~becoming-root-with-su:/home/hacker# ls PWN
PWN
root@users~becoming-root-with-su:/home/hacker# cat PWN
COLLEGE
root@users~becoming-root-with-su:/home/hacker# cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{070xr1ecp_rdJed0dkFryUEIgX2.QX3YTN0wSN5AzNzEzW}

root@users~becoming-root-with-su:/home/hacker# cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
root@users~becoming-root-with-su:/home/hacker# cat not-the-flag
pwn.college{IEsqTHbPQmcKbVjp8jwcQYd9T4L.QX1UDN1wSN5AzNzEzW}
root@users~becoming-root-with-su:/home/hacker# 
```

## What I learned
i learend about root user and differetn types of users also learned how to use su to gain access to root.

## References 
None.
