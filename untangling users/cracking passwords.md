# cracking passwords
the objective for tthis challenge is to use john to dehash the passwd in the given directory to get the passwd for zardus and then run the given cmd to get the flag.

## My solve
**Flag:** `pwn.college{AzQV_tjsrDiLjPSoWOFDEm1sG3I.QX3UDN1wSN5AzNzEzW}`

in this challenge i used john to get the passwd for zardus in the given directory after getting the passwd i then used it to switch to zardus to get the flag after running /challenge/run.
```bash
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:13 0% 2/3 0g/s 287.7p/s 287.7c/s 287.7C/s francine..me
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04962g/s 288.9p/s 288.9c/s 288.9C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{AzQV_tjsrDiLjPSoWOFDEm1sG3I.QX3UDN1wSN5AzNzEzW}
```

## What I learned
i learned about john and passwd one way encrypting and how to use john to decrypt the passwd.

## References 
None.
