# Extracting specific sections of text
The objective of this challenge is to use cut command to get the seconds column of the output along with piping to get the output into the same line to get the flag.

## My solve
**Flag:** `pwn.college{gHLSLCkFwZELBFR8ypLAYGwVZIc.01NxEzNxwSN5AzNzEzW}`

In this challenge I first ran the given command to get an idea on how the flag characterss were seperated and in whcih column they were then i gave the command similar in the explainatino to get the flag.
```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run
23962 p
25468 w
25569 n
27335 .
16434 c
16513 o
26538 l
21461 l
29804 e
29032 g
7068 e
24498 {
10514 g
5028 H
6276 L
16234 S
23397 L
28189 C
17011 k
15600 F
26392 w
26411 Z
17810 E
10924 L
14839 B
3682 F
32050 R
3994 8
27696 y
20004 p
15775 L
21096 A
12930 Y
5474 G
30370 w
13384 V
5273 Z
743 I
13165 c
14885 .
22061 0
16967 1
29402 N
24868 x
4654 E
16614 z
31704 N
21132 x
32575 w
11512 S
2855 N
20315 5
5111 A
29759 z
28609 N
1021 z
5493 E
28798 z
8339 W
5094 }
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{gHLSLCkFwZELBFR8ypLAYGwVZIc.01NxEzNxwSN5AzNzEzW}
```

## What I learned
I learned about cut command and how to use it to extract specific section of data along with its attributes -d -f.

## References 
None.
