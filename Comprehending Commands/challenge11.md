# An epic filesystem quest
THe objective of this challenge is to use the ls,cd,and cat commands learned previously to navigate through various directories in the filesystem following the clues hidden.

## My solve
**Flag:** `pwn.college{oxG_MnlZtuAxbe593BX-BkqQvWF.QX5IDO0wSN5AzNzEzW}`

This challenge was more tedious than hard compared to teh previous challenges I actively followed teh given clues hidden and used appropriate commands so as to not destroy trapped clues, tehn tehrer were delayed and hidden clues which required the use of appropriate commands the bash file for this might be too big but here it is. 
```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
EVIDENCE  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin       challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.   .dockerenv  bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
..  EVIDENCE    boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@commands~an-epic-filesystem-quest:/$ /EVIDENCE
bash: /EVIDENCE: Permission denied
hacker@commands~an-epic-filesystem-quest:/$ cat /EVIDENCE
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/drivers/mtd/devices

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/drivers/mtd/devices
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/mtd/devices$ ls -a
.           Kconfig          bcm47xxsflash.h  docg3.h       ms02-nv.c        mtdram.c  powernv_flash.c      spear_smi.c
..          Makefile         block2mtd.c      lart.c        ms02-nv.h        phram.c   serial_flash_cmds.h  sst25l.c
.BLUEPRINT  bcm47xxsflash.c  docg3.c          mchp23k256.c  mtd_dataflash.c  pmc551.c  slram.c              st_spi_fsm.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/mtd/devices$ cat ./.BLUEPRINT
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/drivers/pci/switch

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/mtd/devices$ cd ../..
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers$ cd ./pci/switch
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/switch$ ls
Kconfig  MESSAGE  Makefile  built-in.a  switchtec.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/switch$ ls -a
.  ..  .built-in.a.cmd  Kconfig  MESSAGE  Makefile  built-in.a  switchtec.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/switch$ cat MESSAGE
Great sleuthing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/chardet

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/switch$ ls ~/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/chardet
ls: cannot access '/home/hacker/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/chardet': No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/switch$ ls /usr/local/lib/python3.8/dist-packages/jedi/third_party/types
hed/third_party/2and3/chardet
SNIPPET-TRAPPED  enums.pyi               langcyrillicmodel.pyi  langhebrewmodel.pyi     langthaimodel.pyi     universaldetector.pyi
__init__.pyi     langbulgarianmodel.pyi  langgreekmodel.pyi     langhungarianmodel.pyi  langturkishmodel.pyi  version.pyi
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/switch$ cat /usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/chardet/SNIPPET-TRAPPED
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/sympy/parsing/autolev

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/switch$ cd /
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/local/lib/python3.8/dist-packages/sympy/parsing/autolev
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/parsing/autolev$ ls
Autolev.g4  CUE  __init__.py  __pycache__  _antlr  _build_autolev_antlr.py  _listener_autolev_antlr.py  _parse_autolev_antlr.py  test-examples
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/parsing/autolev$ cat CUE
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/tools/arch/microblaze

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/parsing/autolev$ cd /opt/linux/linux-5.4/tools/arch/microblaze
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/tools/arch/microblaze$ ls
DOSSIER  include
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/tools/arch/microblaze$ cat DOSSIER
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/bridge
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/tools/arch/microblaze$ cd /opt/linux/linux-5.4/drivers/gpu/drm/bridge
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/bridge$ ls
BRIEF     analogix            cdns-dsi.c                         nxp-ptn3460.c    sii902x.c      synopsys        ti-sn65dsi86.c
Kconfig   analogix-anx78xx.c  dumb-vga-dac.c                     panel.c          sii9234.c      tc358764.c      ti-tfp410.c
Makefile  analogix-anx78xx.h  lvds-encoder.c                     panel.o          sil-sii8620.c  tc358767.c
adv7511   built-in.a          megachips-stdpxxxx-ge-b850v3-fw.c  parade-ps8622.c  sil-sii8620.h  thc63lvd1024.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/bridge$ cat BRIEF
Tubular find!
The next clue is in: /usr/lib/python3/dist-packages/sage/plot/plot3d

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/bridge$ ls /usr/lib/python3/dist-packages/sage/plot/plot3d
ALERT-TRAPPED                                    index_face_set.pyx                                 shapes.cpython-38-x86_64-linux-gnu.so
__init__.py                                      introduction.py                                    shapes.pxd
__pycache__                                      list_plot3d.py                                     shapes.pyx
all.py                                           parametric_plot3d.py                               shapes2.py
base.cpython-38-x86_64-linux-gnu.so              parametric_surface.cpython-38-x86_64-linux-gnu.so  tachyon.py
base.pxd                                         parametric_surface.pxd                             texture.py
base.pyx                                         parametric_surface.pyx                             transform.cpython-38-x86_64-linux-gnu.so
implicit_plot3d.py                               platonic.py                                        transform.pxd
implicit_surface.cpython-38-x86_64-linux-gnu.so  plot3d.py                                          transform.pyx
implicit_surface.pyx                             plot_field3d.py                                    tri_plot.py
index_face_set.cpython-38-x86_64-linux-gnu.so    point_c.pxi
index_face_set.pxd                               revolution_plot3d.py
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/bridge$ cat /usr/lib/python3/dist-packages/sage/plot/plot3d/ALERT-TRAPPED
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/include/config/crc

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/bridge$ cd ../../../..
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4$ cd ./include/config/crc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/crc$ ls -a
.  ..  .SECRET  ccitt.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/crc$ cat .SECRET
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{oxG_MnlZtuAxbe593BX-BkqQvWF.QX5IDO0wSN5AzNzEzW}
```

## What I learned
I revised previously learned concepts and gained a better understanding of them.

## References 
None.
