# finding files
the objective of this challenge is to use the find command with appropriate criteria to look up the flag file in the filesystem.

## My solve
**Flag:** `pwn.college{0kkL1xGOcw1xXc2EKTaqhcLfwya.QXyMDO0wSN5AzNzEzW}`

This challenge was tough as it involved a lot of trial and error for me I got the messsage while reading the run file that the file is hidden but readabel in the filesyustem but that alone didn't help. I had to go through 2 more directories before searching for flag inside usr which gave me two directories the first had a flag.py file which wasn't it the second one led me to the flag.
```bash
hacker@commands~finding-files:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~finding-files:/$ ls /challenge
DESCRIPTION.md  run
hacker@commands~finding-files:/$ cat /challenge/run
#!/bin/bash

fold -s <<< "The flag is hidden (and readable) somewhere on the filesystem. Go find it!"
hacker@commands~finding-files:/$ cd /challenge
hacker@commands~finding-files:/challenge$ ./run
The flag is hidden (and readable) somewhere on the filesystem. Go find it!
hacker@commands~finding-files:/challenge$ find ./run -name flag
hacker@commands~finding-files:/challenge$ cd ..
hacker@commands~finding-files:/$ find /tmp -name flag
find: ‘/tmp/tmp.TpSOPGOVKK’: Permission denied
hacker@commands~finding-files:/$ find /usr -name flag
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/share/locale/he/LC_MESSAGES/flag
hacker@commands~finding-files:/$ cd /usr/local/lib/python3.8/dist-packages/pwnlib
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib$ ls
__init__.py  atexception.py  data          filepointer.py     gdb_faketerminal.py  protocols        runner.py       ui.py
__pycache__  atexit.py       device.py     filesystem         internal             py2compat.py     shellcraft      update.py
abi.py       commandline     dynelf.py     flag               lexer.py             qemu.py          term            useragents.py
adb          config.py       elf           fmtstr.py          libcdb.py            regsort.py       testexample.py  util
args.py      constants       encoders      gdb.py             log.py               replacements.py  timeout.py      version.py
asm.py       context         exception.py  gdb_api_bridge.py  memleak.py           rop              tubes           windbg.py
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib$ cat flag
cat: flag: Is a directory
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib$ cd flag
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ ls
__init__.py  __pycache__  flag.py
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ ls -a
.  ..  __init__.py  __pycache__  flag.py
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ cd /usr/share/locale/he/LC_MESSAGES
hacker@commands~finding-files:/usr/share/locale/he/LC_MESSAGES$ ls
flag          iso_3166-1.mo  iso_3166-3.mo  iso_3166_2.mo  iso_639-3.mo  iso_639_3.mo
iso_15924.mo  iso_3166-2.mo  iso_3166.mo    iso_639-2.mo   iso_639.mo    sphinx.mo
hacker@commands~finding-files:/usr/share/locale/he/LC_MESSAGES$ cat flag
pwn.college{0kkL1xGOcw1xXc2EKTaqhcLfwya.QXyMDO0wSN5AzNzEzW}
```
## Tangents I went on
During solving this challenge i went to a lot of places includng flag.py files and crashing my browser while listing all members of bin directory utimately I was able to find the flag.
## What I learned
I learned how to use the find command to look up directories and files within directories and subdirectories and with names.

## References 
None.
