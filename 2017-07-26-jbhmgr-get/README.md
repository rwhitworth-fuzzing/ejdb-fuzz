`afl-fuzz -i input -o output -M jbhmgr-1 ./jbhmgr get @@ A`

`id:000002,sig:11,src:000003,op:flip1,pos:47`
```
#0  tchdbgetbucket (hdb=0x56284a603030, bidx=731867872) at /root/ejdb/src/tchdb/tchdb.c:2477
#1  0x0000562849ab9c7b in tchdbgetimpl (hdb=hdb@entry=0x56284a603030, kbuf=kbuf@entry=0x56284a603010 "A", ksiz=ksiz@entry=1, bidx=bidx@entry=731867872,
    hash=176 '\260', sp=sp@entry=0x7ffd8cf69e70) at /root/ejdb/src/tchdb/tchdb.c:4414
#2  0x0000562849adebaa in tchdbget (hdb=0x56284a603030, kbuf=0x56284a603010, ksiz=1, sp=0x7ffd8cf69e70) at /root/ejdb/src/tchdb/tchdb.c:735
#3  0x00005628499e3387 in procget (pz=false, px=false, omode=<optimized out>, ksiz=1, kbuf=0x56284a603010 "A",
    path=0x7ffd8cf6bdff "min/id:000002,sig:11,src:000003,op:flip1,pos:47") at /root/ejdb/src/tchdb/tools/jbhmgr.c:676
#4  runget (argv=<optimized out>, argc=<optimized out>) at /root/ejdb/src/tchdb/tools/jbhmgr.c:361
#5  main (argc=<optimized out>, argv=<optimized out>) at /root/ejdb/src/tchdb/tools/jbhmgr.c:78
```

`id:000004,sig:11,src:000007,op:flip1,pos:528719`
```
#0  __memmove_sse2_unaligned_erms () at ../sysdeps/x86_64/multiarch/../multiarch/memmove-vec-unaligned-erms.S:512
#1  0x0000558eb3d89c6d in tcbsdecode (ptr=0x558eb46cb593 "", size=<optimized out>, sp=sp@entry=0x7ffc89ddcb7c) at /root/ejdb/src/tcutil/tcutil.c:10203
#2  0x0000558eb3da75bf in tchdbgetimpl (hdb=hdb@entry=0x558eb46cb030, kbuf=kbuf@entry=0x558eb46cb010 "A", ksiz=ksiz@entry=1, bidx=bidx@entry=98479, hash=176 '\260',
    sp=sp@entry=0x7ffc89de0cb0) at /root/ejdb/src/tchdb/tchdb.c:4448
#3  0x0000558eb3dcbbaa in tchdbget (hdb=0x558eb46cb030, kbuf=0x558eb46cb010, ksiz=1, sp=0x7ffc89de0cb0) at /root/ejdb/src/tchdb/tchdb.c:735
#4  0x0000558eb3cd0387 in procget (pz=false, px=false, omode=<optimized out>, ksiz=1, kbuf=0x558eb46cb010 "A",
    path=0x7ffc89de1dfb "min/id:000004,sig:11,src:000007,op:flip1,pos:528719") at /root/ejdb/src/tchdb/tools/jbhmgr.c:676
#5  runget (argv=<optimized out>, argc=<optimized out>) at /root/ejdb/src/tchdb/tools/jbhmgr.c:361
#6  main (argc=<optimized out>, argv=<optimized out>) at /root/ejdb/src/tchdb/tools/jbhmgr.c:78
```

