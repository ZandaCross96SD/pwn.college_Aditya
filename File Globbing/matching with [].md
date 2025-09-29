# Matching with []
The objective for this challenge is to use [] as a placeholder to access set files.

## My solve
**Flag:** `pwn.college{IsdsTlTAEpwNg17S1FEGCyR5hE0.QXzIDO0wSN5AzNzEzW}`

In this challenge I first navigated to the said directory adn then used the placeholder [] with arguments absh to look for the said files.
```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ ls
file_a  file_c  file_e  file_g  file_i  file_k  file_m  file_o  file_q  file_s  file_u  file_w  file_y
file_b  file_d  file_f  file_h  file_j  file_l  file_n  file_p  file_r  file_t  file_v  file_x  file_z
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{IsdsTlTAEpwNg17S1FEGCyR5hE0.QXzIDO0wSN5AzNzEzW}
```

## What I learned
I learned how one can use [] to act as a specific case of ?.

## References 
None.
