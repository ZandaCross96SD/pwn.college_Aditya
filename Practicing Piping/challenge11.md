# Process substitution for input
The objective for this challenge is to use process substitution to check the differenc between outputs of two programs and get the flag.

## My solve
**Flag:** `pwn.college{gcKnFvXt1r4ikdhBi_APLDiIVyG.0lNwMDOxwSN5AzNzEzW}`

In this challenge the error generated on my first attempt stumped me for a while after looking online I found out it was becasue of the spaces between < and ( after correcting the intial error I arrived at the flag.
```bash
hacker@piping~process-substitution-for-input:~$ diff < (/challenge/print_decoys_and_flag) < (/challenge/print_decoys)
bash: syntax error near unexpected token `('
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys_and_flag) <(/challenge/print_decoys)
56d55
< pwn.college{gcKnFvXt1r4ikdhBi_APLDiIVyG.0lNwMDOxwSN5AzNzEzW}
```

## What I learned
I learned about process substitution and revisited previouslly learned concepts.

## References 
None.
