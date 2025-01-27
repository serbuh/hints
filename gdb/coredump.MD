## Core dump
Enable core dump
```
ulimit -c unlimited
```
Run a program
```
./prog
```
analyze core dump
```
gdb ./prog core
```
