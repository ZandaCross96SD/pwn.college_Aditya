# Multiple Options For Tab Completion
The objective of this challenge is to access the flag file using tab twice.

## My solve
**Flag:** `pwn.college{IthPje2XSCIfcroK9x2kPFIpRRl.0lN0EzNxwSN5AzNzEzW}`

I initially made the mistake of using cd instead of cat here to read the file other than that the process was as explained in the problem statement.
```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files/pwncollege-
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files/pwncollege-fla
pwncollege-flag      pwncollege-flamingo  
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files/pwncollege-flag
bash: cd: /challenge/files/pwncollege-flag: Not a directory
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{IthPje2XSCIfcroK9x2kPFIpRRl.0lN0EzNxwSN5AzNzEzW}
```

## What I learned
I learned how to use tab completion to list conflicting possibilities.

## References 
None.
