# killing misbehaving processes
the objective for this challenge is to use kill and ps together to find the decoy process kill it and then run the original program to get the flag.

## My solve
**Flag:** `pwn.college{s2WZUUQDR4_WP81yXSZqP6C07XB.0FNzMDOxwSN5AzNzEzW}`

in this challenge i first listed the processes and then killed the decoy process after which i ran the /challenge/run program which sent the flags to the fifo file i interrupted the process in between because as explained it was also sending a lot of decoys still in the pipe when used cat to get the flag it showed a lot of decoys i then again ran the comd /challenge/run and then cat the original file which gave me the original flag.
```bash
hacker@processes~killing-misbehaving-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 11:27 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 11:27 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 11:27 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 11:27 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 11:27 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140     138  0 11:27 ?        00:00:00 sleep 6h
root         141     137  0 11:27 ?        00:00:00 sleep 6h
hacker       142     139  0 11:27 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       153       1  0 11:27 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.
hacker       177     153  0 11:27 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       188     177  0 11:27 pts/0    00:00:00 ps -ef
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
^C
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{YfYDSm.QEgdXHimXCkXM1nnTDckRT6p3GvtvQ5Ac6XPGeki}
pwn.college{znX9-WV2hkrqwoRODL0vT1LUVaYxkUZConPUcy47A7SiT.q}
pwn.college{byqb49GpZ90H43TL5xOmoTt25527stXTZqMPytHF4DpEbBR}
pwn.college{4864tKAYo2CG2aSasgmxMpy3T3RlcgCmuQqfrYHRONvXrp-}
pwn.college{TiEl6lcP4g5QedK5I3sAYXj4f52-KqPEnYkGMG6QNoqcy88}
pwn.college{kO-nJvBOjbd4MYB2ByMbEYBkB-seIL4vaS6-56VZzzAtOOv}
pwn.college{bvJzOd5W-LCr1sF97Cnm8zu1ZA1E8kOmQUdFxO2waQ7Av.Y}
pwn.college{Xz.nNxj7e53v16V8oQfTa1fywl4-uxNNy3ksH00Qrjnl7Pd}
pwn.college{nprerMYfQoy8Z5TZDxtRKrP76mBqA8BBZtVWr9jc5-H-3mn}
pwn.college{YHwQCaNC3jeFiLiwh34m4dWIqfVwacoS3wnpSF2hhhLIYZ.}
pwn.college{ODxNASLe2oWvQZsysYHHB10mPURcUzbNICuWlbU3yV-jNri}
pwn.college{C1OtQA1TMULq-TxYyju8RodbpdBzAugaPnCX8Heh4xC494y}
pwn.college{.7c1rstWzpKVmytqhBBxuSXNLTghbSbug3g54LKUdQ9uhPK}
pwn.college{YYEWfDjEQtavY4-sbHa3eVtbR6vfmdFtlFTz3NRzxaCrnSA}
pwn.college{1u1POOyUOSM5wvGta05Ks19Rl3lfizNnuhYLrirkXqJdiL0}
pwn.college{-aufMat3ld-K8tyYztwvM8X74DqwFLfNb6RIF-J710RPo1z}
pwn.college{onH.usoGRpptPRlCozAaz-PLHoyicfVa5BGaSRf0Zg.iFs.}
pwn.college{irUzc9NI.n2-WtYbbhPyg0b2JSCcmtSvLOJ6YdZrZSKJ-uV}
pwn.college{5l3C8-s0kqCrd94bVZoUxBiA3-VGq2G3FP2exzdzpJID4Cm}
pwn.college{k3Mn9FfV9sFToOZ8k3-zhjc4V.AdbYm52Q6xMPxAHp6fmr4}
pwn.college{qF1qWbG-rd7JS9Lr5o06LBN1mtfsV8.61Q6OwwCDZRSbPIJ}
pwn.college{S09B3NI98z5CRbhJQKaGhryCePGCdRCjyao18NLH.vy09Fo}
pwn.college{e8OpZS-TfvQzfMJBMUWujPvw.E8bs2X0HkJMzgP0uIY2HjE}
pwn.college{GzOJLonX5lYSkfHYAYyMmp3-F3Pk1puuGhj.mbMeISKGYdc}
pwn.college{BQkd.bQpWjjSHObrNJk0LgJClaxCZHWCEEBQTPOGsZ7jJrt}
pwn.college{uGXZWNh88JF3J2zBK.ReK2n8U7E1rpFQBfCv1-mwXuugL2p}
pwn.college{jD8QUFhUz0e9JgCDlQj68OV9aHOtuvQVx0Ka7X6rAQazMzZ}
pwn.college{hNBLxJ.XWB0KJQbcmc8LWf0loglFKAMf-HkYEU-jd1SIPGj}
pwn.college{Bz.8ww8cIale8X5l-RtGYQ0Ly7tkqqFmn7YYF2NnjlJMvHI}
pwn.college{Ns3yQsdko0SIyQqkRR8PQSGD8qYJsWafd.zjba-SNFnBGf4}
pwn.college{iP..-6PaDkR-rf7SJMbi6Gf2FaTngdslUDMsDqGwYRt9ZcB}
pwn.college{sGHJkJNPPXxTH8q2AiiB4mMBkd1EnkaIMi2YBhGhob0GxLX}
pwn.college{bQyRoZVnpse0V2gR9pJ5sjBUu32dY97MD4XkDUOuYQkgq-6}
pwn.college{9eUFo5fXYPfVfoMCbm7oIYJZ3FQdB-i19L4-2dbgNkO27C0}
pwn.college{nrt2VvfZ9uVggvOEZ277A7Nh8-P-DrP4Ew7wYm0mg-vuRBA}
pwn.college{ioCp86JgvgwxJ21fBBx5yPMXI8K3TQyTqBrILIVb.E103eI}
pwn.college{mS6jRo7rGLa9ZzuX8MBI477SLaCOQc6fJWqpZgXjvX9EPJv}
pwn.college{-Dskq5yAWcoLy3rTpFxrD-yOITioHoPJLdDNEBYxS1GOMSY}
pwn.college{b0d6MoroIhjGCAhaL7TflvATscHDbOgi1wv2mqJ5j8u0ISl}
pwn.college{WP6w3Bc5CbEKCVuIyGXdqUyazX3P9syl52gQ.SzJ6s8hE9O}
pwn.college{l1OIQKD27iKRq6Vv6wTDA0bC-CSMkohy93-MSoj9D2.AeJR}
pwn.college{0uKHNqDMwV1cMFOmDHSva9Ten3uydQAduHzSit7W-hlznMS}
pwn.college{Cj70Tsj9uCtsYgCsxL9HyzyYaFKBnboRSK93ufzZR1gT03H}
pwn.college{j4ZBrEhMthG64VRztlXyjFPhhT5vDpYQfSNEZZjIMGYgXZW}
pwn.college{GP9pwqsUCtf-s-wgAD8EDFPrvc3zslYHfTk8tamuvyFXLdg}
pwn.college{r5Awu2wt8MNvRYU5KrrR3-7At6QfVw5TPOXKsVO8GyfK.qc}
pwn.college{p9jCVVVqLt1o1Rkmq0hq2m2jcdUIHPlNT6uknsG-nEYbyCe}
pwn.college{K3EYZoXN-KhCQ.UTsWtRtz2skwTNnbVHh-a-xN0sMln-n9c}
pwn.college{D98gdq3BI-oaZuCyxmWNicyPww38SsbnMKmo-m46aDgqkvW}
pwn.college{HI0NUbNFj7setUUT152LL5nq.0uNzfzgdTERJVmS1D9djhk}
pwn.college{zXf3C0jBIB44yd.vlKeEtsyNuckR434f5WzXGpW.rPslG1N}
pwn.college{j8EC2IgcZpN1IkHef9V9bW7liB4YRwB7Yn.LXtWiSyNEu9j}
pwn.college{bB4TWvv3LqYTpcAg3mzFlnPHZYNgc65ngzQfvhqZwRMeiAz}
pwn.college{GJT5jY7GgJZN4pakwvkgRm11ln3BO98x-eZWwC5cU3bKtBD}
pwn.college{KS4aAnAkPt7Tmh.vWkg..CwFS8EgD5WQi9L85AvUuxepWiN}
pwn.college{Pt23kV9GOWG0OkgXq5dVAdkHbiDmc9dKIxIKPBnKrgQ-2R0}
pwn.college{nfgrYeDQIM8.oG0Q4uHq4pepM0Gb9G-uDxoD230oKNmBAg7}
pwn.college{U8nBn7f66XtUWIif1rAoK63.eLBbh4f7W.pdym4TkOtvi5l}
pwn.college{Ffh7CcLS3dniol9MMkmTNkYHZmetcyw3QC0LeBoJDGNtzO5}
pwn.college{aE6yXDxv.Lj8te.H2sJpD3zGSa1sIddsQcENuXjcAQ1VWV3}
pwn.college{HWmjVZru97HAhLAC3LWliyNrdMpktJJ373X3tvgSNGaw1lY}
pwn.college{1.pMMw00rSdML9.1EzGPTS6EBrRnsjpza3HmR2MwFOYbTRm}
pwn.college{DacrJFm2VF9FUtwYiAZMXXS5q080cvtWI.71U.FPwTy7f3Z}
pwn.college{tpCSlUlvzKYULGrTlaXXHWexyxQMtLIqU5bIkxCYf9i9sMU}
pwn.college{gIXv06lwOIfeTGbtGXD3v1x39y-1alKia.5VwuMPF.fT3m-}
pwn.college{CPDcK2NObeDnXpiFuqjmhvV9WcrG-wmEvaoLGkI9OgluIYS}
pwn.college{Qn56fjDStjVVPj-fDdDzvGZrPLX7W7H-E0G3Ws8AL3Yysij}
pwn.college{6bdvj153wWsT0RBkSj73EFklKr2.0uk66U9jyWFglaVNEoK}
pwn.college{3KkZgZqrPZjPaWByHuM29EUlG4gtweJcmTXN-hYPHbNm2wv}
pwn.college{BrggkwW-cdNHvf9qDnwAhDOY34LIU.mYLZwDpEVJZ0M.s9h}
pwn.college{HO4tQsQzmwGdlPyZUkX3yH4Db61uO0hhUPOzCOQuZxxoG-3}
pwn.college{bxE6zv7HhLTFKiVxGVCq-IoePkLU6k25KtjyHfVJmOabQXq}
pwn.college{-tamKoTKiR0g6YAAICCnh5frEi8BPL0WLI7c3WQUMxsTJ6n}
pwn.college{6geUWKOJ6jrQ8jc41LKF-lLUG3MeAzQ.2u2M5rAx8MvhCDP}
pwn.college{FgbGGiknL2KjJoYmWT.QYeoIuJrnUUU4dHhEXqNKFM9rmFa}
pwn.college{i-oSlhIVYDl9yRSs4xja6Vwt3-BNwhZJ8fVKLG-7Knut20D}
pwn.college{4fMJC0bGwO3jaZWef..NZQbL9ZuLktsw5gJnkG9qs6.a40q}
pwn.college{VHYQ.4CdxSwlymnKmYOWqigDB5WKpIqnPlYhq2EpcHc9WWK}
pwn.college{ZLoTber3VSdAensr5Iz6kicyXXo0y2QWpfZpD.Pd5a3os.f}
pwn.college{Ke7OCYze1aq3CWARCAp9or639zdocNb0tmFvHpoZoiSiWPW}
pwn.college{-i7dbtoEQl7Z76qAfk6B5LNooiKJpOJBqZPESBwJN0vFr-o}
pwn.college{A98E42.HnhvuIFIG8WuSBwOIp7jpIyGzYiTyKPhqTh2LRZ3}
pwn.college{0fSkWbW8vOz0jQp3Sz40Xnw-9OBGNm5KHMivQILBHD2BH8Y}
pwn.college{SANrvf6OIULozolP2slqiJt6AHeeVXtYtQXSObFahSohupg}
pwn.college{NzL2DFkH.UlTJSRO1lT8wKzQllkHc9QBrjY.eQs8GEOhfDi}
pwn.college{Sz5FxpI9Fm1gWHHXb2yy0l4rhcrq05jpIUYab4Nn1Ca9JKm}
pwn.college{sgZi1cTfGmCKkWWdjzdAymPYsxgujdHXFAsgBSZnylUA-Qq}
pwn.college{d7bi1ZXcNF8-broRh34Qvkc6KxDO1bTPtALoQgKZVsMugSw}
pwn.college{jLXun5LRzX2fqzdW56-qRaf2L6eHXtkAAf9QZ8nNKi9fjr5}
pwn.college{fkb8YExl1dsUk8---LuyhdKt7efJt97dvI0O306rTmoP1w1}
pwn.college{-wbbrm-AeiJT1TbrZbdlc1BTwOjfZmvJL0jOPgfFVD2Jo3j}
pwn.college{N-BryQ3KyCVwrIezDneEyxjS-PDivgO0akyMDqzBoCugSHQ}
pwn.college{W2mMR7pUzfvmU3Y9mc3CzlbOKOou258zR8GejaF.KM47EHb}
pwn.college{nN7lGVGaHKrc05lAUcrVodTNIyZCR.a45bDx-70U.AGi531}
pwn.college{8xikhm5XxXU0cR6MqPEJuplyVW1.hzCWWiCA5aHphnlV8HB}
pwn.college{NzMB.N3NCTTr6nlJkzVGytj8zgBOg2NzXlij9VUhioIk6JA}
pwn.college{b4nzHSLZ2xsvWNiD-zLEnX.ui2zDymhhYhgVwn2.sKCL86X}
pwn.college{DZn0kqqr6VHaQVfUuCt3Udtc6-4driUwIzOUqG5oqgR0I6s}
pwn.college{d-y5aODMtStdJNUdiHMkLB7SfEm7fDivjkmHmtJQOJxycAb}
pwn.college{Xa2wu3wsntj8GMigmghkcJ-vAMq35KvJxbK7DCfh9sQAT85}
pwn.college{MGBtP6fCe7lkngB4HTV8jKC2kELzvduphR25me7n1GEuSqJ}
pwn.college{cszwzARjbW0LuS9OFQ5-zqAKBnFophX3zu5Oi8hJ.UbM8l5}
pwn.college{v3t4K.ga-hMh4Hc28ISoG4k6IkA-T01k3bdSAAhnK7nhIER}
pwn.college{O31TnnUVZe3LHRQ3ZlUF.BVcHnkRV-oHbIVmfB-qu0hb7Nm}
pwn.college{yBci5O.fFXhSzpL-.I7z0ABI0J4UTtUZVl9x7Lzc-LUMhcX}
pwn.college{26v4wL9B1oLBcQNVf897OzgARfXXoVkKLf4A9By6QRyawPo}
pwn.college{wr2dficdZIU9OlRNiUBydB1h2T10KKgqTSmfntKF4Dktirf}
pwn.college{vJs7rdzgjsf.JGLHTn8QXgBOACtTX0GDW2xsg1edW2wB96p}
pwn.college{JI1MyRu9-AJbpCvRuJlNaM-ktcw5iiYTRKXqfkNJatmQGNh}
pwn.college{cKs-7aZY8VMvzaD0hk-yAG-yDW7QAAyEaBdix-pnvJmmeld}
pwn.college{poqgNB18DY6WxhLkzaxq8bFwKqqb36UJa9kociQ8tG3HnXb}
pwn.college{hzV-smeueGufrINonsCvChcISrsZBLwaU-H5HxB2S-HGR2r}
pwn.college{HsqXFModX6PyqxpilBZFDvKKgnwIt-SMOj9xUQO-umLo3hg}
pwn.college{8JLCVHjQ7SPzwqIx.7qob4QsRafWHKPxQDQXxRJpSzrwaTz}
pwn.college{xdV-DFiRgyeXGc4g7K3Zi.v3meWf0n8J0a2EOpD77OJSz6-}
pwn.college{pZdUW6gPillF9KfqDpbZVWshG-FFWK9ifmG9XXc.5U.y6Y0}
pwn.college{TQwqhYr6wF2k.MJrdd3UWoQBMNw6C85h9wBwiCj9pR7aoh3}
pwn.college{fqBLe6uhrL6wX6NagsvDVAHZzkDq6bWm-9MCWi5RjQGJHWl}
pwn.college{Cqu-5MOhqIAIIT6JI03Tqtv23UPuvv-5qm2HjSCbFEsBir7}
pwn.college{a1FYA4Uag4WH6G.sxNIV8xsVnXH3kLWL5E.38VSGibevC68}
pwn.college{90pQmvCXAllhZwSvKF0khRX2NH86Zt3E5y-.qRyv-zqD9Eu}
pwn.college{insaGHZIm.L256anUUFBqvwfHTR04bIpIJFDiwgsQtdQrx9}
pwn.college{BWhzYu3IUFSJLwG4qGHWB6.ykprzwG3o0lvOSFGOr705Fxy}
pwn.college{lAVSGrMgQXmOLLfIsYkmP.9.RU62G-V6XiQ2ZvY-rJELaVT}
pwn.college{3sPoGUCiGtmaGv3mVTSEtr0GT4Amsrrg1bhhhrnQ6HnzRr.}
pwn.college{OEJTHw32jv6BqRb.6XjwmClfnArI6MHozqSiVFajT9D6P1U}
pwn.college{EPG29xtMlmrtKnERsw.oAlSmuXp0yR0cy6FF4D2NKuRHAPz}
pwn.college{jOpP9avU.laZ.-OeuQEM6mEZulhEMtyI4yDiwWzCci2Fv3a}
pwn.college{f-mqaU7IRcF-uvKlJWtBvm33PCM83bbVGE4w0SW7tr7Zi2N}
pwn.college{tuS0.rYrYLiyFn8-vTO98CvEcF9R.EM.sNkVOtbdoP3NaU4}
pwn.college{nxDUMwl3HzMG96mwztv-JPqqapR0IdcZzAEKGFD59jyDRUr}
pwn.college{BVIHADRce2VeVu.e1Sl4ZVJsOl.KQsuLteScMMQpfNx.BnM}
pwn.college{-Ys0RhU7AU7.4q4ITlLYQBF-gSUYSXiBTtobieO1y2K6x0X}
pwn.college{bVuPkUK1k8D6sBHX3gTCyHmPXoI1DX4Gdq2NwY8KwijLuHJ}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{s2WZUUQDR4_WP81yXSZqP6C07XB.0FNzMDOxwSN5AzNzEzW}
```

## What I learned
i learned about kill in more depth and the pipe stream when it removes a process.

## References 
None.
