Command line used to find this crash:

afl-fuzz -i input -o output -M jbfmgr-1 ./jbfmgr list @@

If you can't reproduce a bug outside of afl-fuzz, be sure to set the same
memory limit. The limit used for this fuzzing session was 50.0 MB.

id:000000,sig:11,src:000003,op:havoc,rep:128

```
#0  tcfdbnextid (id=256, fdb=0x560345560010) at /root/ejdb/src/tcfdb/tcfdb.c:2130
#1  tcfdbiternextimpl (fdb=0x560345560010) at /root/ejdb/src/tcfdb/tcfdb.c:2591
#2  tcfdbiternext (fdb=0x560345560010) at /root/ejdb/src/tcfdb/tcfdb.c:659
#3  0x000056034417769c in proclist (ristr=<optimized out>, rustr=0x0, rlstr=<optimized out>, px=<optimized out>, pv=false, max=-1, omode=<optimized out>,
    path=0x7ffe21189df2 "output/jbfmgr-1/crashes/id:000000,sig:11,src:000003,op:havoc,rep:128") at /root/ejdb/src/tcfdb/tools/jbfmgr.c:679
#4  runlist (argv=<optimized out>, argc=<optimized out>) at /root/ejdb/src/tcfdb/tools/jbfmgr.c:390
#5  main (argc=<optimized out>, argv=<optimized out>) at /root/ejdb/src/tcfdb/tools/jbfmgr.c:80
```




id:000002,sig:06,src:000009,op:flip1,pos:87

```
#0  __GI_raise (sig=sig@entry=6) at ../sysdeps/unix/sysv/linux/raise.c:51
#1  0x00007f28870cc3fa in __GI_abort () at abort.c:89
#2  0x00007f28870c3e37 in __assert_fail_base (fmt=<optimized out>, assertion=assertion@entry=0x55dfc63c3a9d "fdb && id >= 0",
    file=file@entry=0x55dfc63c3a80 "/root/ejdb/src/tcfdb/tcfdb.c", line=line@entry=2111,
    function=function@entry=0x55dfc63c46d0 <__PRETTY_FUNCTION__.8963> "tcfdbnextid") at assert.c:92
#3  0x00007f28870c3ee2 in __GI___assert_fail (assertion=assertion@entry=0x55dfc63c3a9d "fdb && id >= 0",
    file=file@entry=0x55dfc63c3a80 "/root/ejdb/src/tcfdb/tcfdb.c", line=line@entry=2111,
    function=function@entry=0x55dfc63c46d0 <__PRETTY_FUNCTION__.8963> "tcfdbnextid") at assert.c:101
#4  0x000055dfc636dbff in tcfdbnextid (id=-9223372036586340352, fdb=0x55dfc6788010) at /root/ejdb/src/tcfdb/tcfdb.c:2111
#5  tcfdbiternextimpl (fdb=0x55dfc6788010) at /root/ejdb/src/tcfdb/tcfdb.c:2591
#6  tcfdbiternext (fdb=0x55dfc6788010) at /root/ejdb/src/tcfdb/tcfdb.c:659
#7  0x000055dfc629469c in proclist (ristr=<optimized out>, rustr=0x0, rlstr=<optimized out>, px=<optimized out>, pv=false, max=-1, omode=<optimized out>,
    path=0x7ffd77beddf3 "output/jbfmgr-1/crashes/id:000002,sig:06,src:000009,op:flip1,pos:87") at /root/ejdb/src/tcfdb/tools/jbfmgr.c:679
#8  runlist (argv=<optimized out>, argc=<optimized out>) at /root/ejdb/src/tcfdb/tools/jbfmgr.c:390
#9  main (argc=<optimized out>, argv=<optimized out>) at /root/ejdb/src/tcfdb/tools/jbfmgr.c:80
```
