# the ripper
objective: to extract the flag hidden in wordlist.
## mysolve
## flag:
```
citadel{fake_flag_4_fake_pl4y3rs}
```
the name ripper for the challenge was a hint oto use john the ripper tool to extract the flag\
since we were given the wordlist and the hash for the program we passed it to john to get the flag.
```
john --wordlist=wordlist.txt --rules hash.txt
```
