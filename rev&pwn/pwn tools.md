## run gdb with pwntools 
 r =pwn.gdb.pwn
## set value and memory locations 
using set
example
set *(unsighned char *)$rsp =0xd

# disabling ASLR for local testing and disablig everything else
```
gcc vuln.c -o vuln_disable_all -fno-stack-protector -z execstack -no-pie

pwn.process("<file>", aslr=false)
to innitialize and control the process
p = pwn.process("./rop-example")

pwn.cyclic(<no of characters>, n=<size of one cycle>,)
pwn.cyclic_find("<cycle>" <n=<size of cycle>>)
```

