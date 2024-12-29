## Attach to gdb remote
On debug target:
```
gdbserver:20000 /executable
```
On host:
```
gdb
(gdb) target remote address:20000
```

## View the assembly code
Enter assembly layout
```
(gdb) layout asm
```
Exit assembly layout
```
Ctrl+x a | exit assembly layout
```
Retrun to the current line:
```
(gdb) layout split
(gdb) layout asm
```

## Debug python
```
gdb python3
(gdb) r -c 'import pgs_python'
```


C | A
-|-
(gdb) bt | backtrace
(gdb) frame 0 | go to callstack frame 0