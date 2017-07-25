`id:000000,sig:11,src:000000,op:flip1,pos:47`
```
#0  tchdbgetbucket (hdb=0x55c2e4d21140, bidx=731867856) at /root/ejdb/src/tchdb/tchdb.c:2477
#1  0x000055c2e43eb44b in tchdbgetintobuf (hdb=hdb@entry=0x55c2e4d21140, kbuf=kbuf@entry=0x7fff2dd3d940 "1", ksiz=ksiz@entry=1, bidx=bidx@entry=731867856,
    hash=192 '\300', vbuf=vbuf@entry=0x7fff2dd3d990 "", max=32768) at /root/ejdb/src/tchdb/tchdb.c:4605
#2  0x000055c2e4411504 in tchdbget3 (hdb=0x55c2e4d21140, kbuf=kbuf@entry=0x7fff2dd3d940, ksiz=ksiz@entry=1, vbuf=vbuf@entry=0x7fff2dd3d990, max=max@entry=32768)
    at /root/ejdb/src/tchdb/tchdb.c:792
#3  0x000055c2e43a8c58 in tcbdbleafload (bdb=bdb@entry=0x55c2e4d21030, id=<optimized out>) at /root/ejdb/src/tcbdb/tcbdb.c:1882
#4  0x000055c2e43bed73 in tcbdbgetimpl (bdb=bdb@entry=0x55c2e4d21030, kbuf=0x55c2e4d21010 "A", ksiz=ksiz@entry=1, sp=sp@entry=0x7fff2dd45aa0)
    at /root/ejdb/src/tcbdb/tcbdb.c:3137
#5  0x000055c2e43bf140 in tcbdbget (bdb=0x55c2e4d21030, kbuf=<optimized out>, ksiz=1, sp=0x7fff2dd45aa0) at /root/ejdb/src/tcbdb/tcbdb.c:469
#6  0x000055c2e42cb089 in procget (pz=false, px=false, omode=<optimized out>, cmp=0x0, ksiz=1, kbuf=0x55c2e4d21010 "A",
    path=0x7fff2dd47dc5 "output/jbbmgr-1/crashes/id:000000,sig:11,src:000000,op:flip1,pos:47") at /root/ejdb/src/tcbdb/tools/jbbmgr.c:792
#7  runget (argv=<optimized out>, argc=<optimized out>) at /root/ejdb/src/tcbdb/tools/jbbmgr.c:413
#8  main (argc=<optimized out>, argv=<optimized out>) at /root/ejdb/src/tcbdb/tools/jbbmgr.c:82
```


`id:000030,sig:11,src:000106,op:flip1,pos:4623`
```
#0  __memmove_sse2_unaligned_erms () at ../sysdeps/x86_64/multiarch/../multiarch/memmove-vec-unaligned-erms.S:515
515     ../sysdeps/x86_64/multiarch/../multiarch/memmove-vec-unaligned-erms.S: No such file or directory.
(gdb) bt
#0  __memmove_sse2_unaligned_erms () at ../sysdeps/x86_64/multiarch/../multiarch/memmove-vec-unaligned-erms.S:515
#1  0x000055877958894d in tcbsdecode (ptr=0x55877b521983 "", size=<optimized out>, sp=sp@entry=0x7ffdf2bb90cc) at /root/ejdb/src/tcutil/tcutil.c:10203
#2  0x00005587795edd9b in tchdbgetintobuf (hdb=hdb@entry=0x55877b51b140, kbuf=kbuf@entry=0x7ffdf2bbd210 "1", ksiz=ksiz@entry=1, bidx=bidx@entry=0, hash=192 '\300',
    vbuf=vbuf@entry=0x7ffdf2bbd260 "", max=32768) at /root/ejdb/src/tchdb/tchdb.c:4639
#3  0x0000558779613504 in tchdbget3 (hdb=0x55877b51b140, kbuf=kbuf@entry=0x7ffdf2bbd210, ksiz=ksiz@entry=1, vbuf=vbuf@entry=0x7ffdf2bbd260, max=max@entry=32768)
    at /root/ejdb/src/tchdb/tchdb.c:792
#4  0x00005587795aac58 in tcbdbleafload (bdb=bdb@entry=0x55877b51b030, id=<optimized out>) at /root/ejdb/src/tcbdb/tcbdb.c:1882
#5  0x00005587795c0d73 in tcbdbgetimpl (bdb=bdb@entry=0x55877b51b030, kbuf=0x55877b51b010 "A", ksiz=ksiz@entry=1, sp=sp@entry=0x7ffdf2bc5370)
    at /root/ejdb/src/tcbdb/tcbdb.c:3137
#6  0x00005587795c1140 in tcbdbget (bdb=0x55877b51b030, kbuf=<optimized out>, ksiz=1, sp=0x7ffdf2bc5370) at /root/ejdb/src/tcbdb/tcbdb.c:469
#7  0x00005587794cd089 in procget (pz=false, px=false, omode=<optimized out>, cmp=0x0, ksiz=1, kbuf=0x55877b51b010 "A",
    path=0x7ffdf2bc6dc3 "output/jbbmgr-1/crashes/id:000030,sig:11,src:000106,op:flip1,pos:4623") at /root/ejdb/src/tcbdb/tools/jbbmgr.c:792
#8  runget (argv=<optimized out>, argc=<optimized out>) at /root/ejdb/src/tcbdb/tools/jbbmgr.c:413
#9  main (argc=<optimized out>, argv=<optimized out>) at /root/ejdb/src/tcbdb/tools/jbbmgr.c:82
```


`id:000048,sig:11,src:000719,op:int16,pos:4643,val:-128`
```
#0  __memmove_sse2_unaligned_erms () at ../sysdeps/x86_64/multiarch/../multiarch/memmove-vec-unaligned-erms.S:364
364     ../sysdeps/x86_64/multiarch/../multiarch/memmove-vec-unaligned-erms.S: No such file or directory.
(gdb) bt
#0  __memmove_sse2_unaligned_erms () at ../sysdeps/x86_64/multiarch/../multiarch/memmove-vec-unaligned-erms.S:364
#1  0x0000562bfa453423 in tcbdbleafload (bdb=bdb@entry=0x562bfbb98030, id=<optimized out>) at /root/ejdb/src/tcbdb/tcbdb.c:1937
#2  0x0000562bfa468d73 in tcbdbgetimpl (bdb=bdb@entry=0x562bfbb98030, kbuf=0x562bfbb98010 "A", ksiz=ksiz@entry=1, sp=sp@entry=0x7ffd0eb019b0)
    at /root/ejdb/src/tcbdb/tcbdb.c:3137
#3  0x0000562bfa469140 in tcbdbget (bdb=0x562bfbb98030, kbuf=<optimized out>, ksiz=1, sp=0x7ffd0eb019b0) at /root/ejdb/src/tcbdb/tcbdb.c:469
#4  0x0000562bfa375089 in procget (pz=false, px=false, omode=<optimized out>, cmp=0x0, ksiz=1, kbuf=0x562bfbb98010 "A",
    path=0x7ffd0eb02dba "output/jbbmgr-1/crashes/id:000048,sig:11,src:000719,op:int16,pos:4643,val:-128") at /root/ejdb/src/tcbdb/tools/jbbmgr.c:792
#5  runget (argv=<optimized out>, argc=<optimized out>) at /root/ejdb/src/tcbdb/tools/jbbmgr.c:413
#6  main (argc=<optimized out>, argv=<optimized out>) at /root/ejdb/src/tcbdb/tools/jbbmgr.c:82
```
