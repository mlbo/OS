# 0x1 编译链接
.c-->预编译（-E）-->.i-->编译（-S）-->.s-->汇编（-c）-->.o-->链接-->a.out

[tldr](https://github.com/tldr-pages/tldr) gcc
  - Compile multiple source files into executable:
    gcc source1.c source2.c -o executable

  - Allow warnings, debug symbols in output:
    gcc source.c -Wall -Og -o executable

  - Include libraries from a different path:
    gcc source.c -o executable -Iheader_path -Llibrary_path -llibrary_name

  - Compile source code into Assembler instructions:
    gcc -S source.c

  - Compile source code without linking:
    gcc -c source.c

objdump a.o

> **objdump**: displays information about one or more object files.  The options control what particular information to display.  This information is mostly useful to programmers who are working on the compilation tools, as opposed to programmers who just want their program to compile and work.

## 预编译

```
#include <stdio.h>
#include "stdio.h"
```