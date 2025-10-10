# Sorting data
In this challenge THe objective is to sort 100 lines to get the flag using sort cmd.

## My solve
**Flag:** `pwn.college{oHwAKkEotv1MamMn-kr0rZ35QxA.0FM0MDOxwSN5AzNzEzW}`

In this challenge i used sort cmd along with -r to sort data alphabetically since it was menttioned flag would be at last i used head to get the first line since the data here is sorted in reverse order.
```bash
hacker@data~sorting-data:~$ sort /challenge/flags.txt -r | head -n 1
pwn.college{oHwAKkEotv1MamMn-kr0rZ35QxA.0FM0MDOxwSN5AzNzEzW}
```

## What I learned
i learend about sort command and its variuous attributes -r -R -n -u.

## References 
None.
