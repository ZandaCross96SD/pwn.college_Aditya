# process exit codes
the objective for this challenge is to get the error code for the given process using $? and then pass it as an argument to another function to get the flag.

## My solve
**Flag:** `pwn.college{A9dkYBNWi-FB1E2nr2dF7DVjndf.QX5YDO1wSN5AzNzEzW}`

below as you can see i first tried to pass the error and pipe it to echo $? to get the err code in hindsight and with the explaination i understood what part i got wrong about error codes i then ran the challenge and then got the error code i then passed the code as avlue to the said process to get the flag.
```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code | echo $?
0
ERROR!
It looks like you are redirecting my standard output! This is not how you save 
off the error code. The error code is not outputted anywhere; simply returned 
from this program as it exits. It will end up in the $? variable. Please 
re-launch this program without output redirection.
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
231
hacker@processes~process-exit-codes:~$ /challenge/submit-code 231
CORRECT! Here is your flag:
pwn.college{A9dkYBNWi-FB1E2nr2dF7DVjndf.QX5YDO1wSN5AzNzEzW}
```

## What I learned
i gained understanding of error codes and how to retriece them using $?.

## References 
None.
