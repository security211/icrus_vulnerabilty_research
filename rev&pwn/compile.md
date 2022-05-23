gcc -S -masm=intel <file.c>

katai struct (ide.katai.io): file format parser 
nm: lists symbols used /provided
checksec (github.com/slimm609/checksec.sh)

static Dissemblers
angr managment
cutter -rev tool based from radare

binary ninja cloud

tracing tools

ltrace traces library calls 
strace traces system calls

## gdb scripting

## https://crackmes.one
site has crack me challanges

## bypass aslr by overitting page offsets

**Disable canary:**

```c
gcc vuln.c -o vuln_disable_canary -fno-stack-protector
```

**Disable DEP:**

```c
gcc vuln.c -o vuln_disable_dep -z execstack
```

**Disable PIE:**

```c
gcc vuln.c -o vuln_disable_pie -no-pie
```

**Disable all of protection mechanisms listed above (warning: for local testing only):**

```c
gcc fo.c -o vuln -fno-stack-protector -z execstack -no-pie
```

For 32-bit machines, you'll need to add the `-m32` parameter as well.



 
