peda
====

PEDA - Python Exploit Development Assistance for GDB

## Key Features:
* Enhance the display of gdb: colorize and display disassembly codes, registers, memory information during debugging.
* Add commands to support debugging and exploit development (for a full list of commands use `peda help`):

| Command     | Description                                      | 描述                                                       |
| ---         | ---                                              | ---                                                        |
| aslr        | Show/set ASLR setting of GDB                     | 显示/设置 GDB 的地址空间布局随机化（ASLR）设置              |
| asmsearch   | Search for ASM instructions in memory            | 在内存中搜索汇编（ASM）指令                                 |
| assemble    | On the fly assemble and execute instructions using NASM | 使用 NASM 即时汇编和执行指令                          |
| breakrva    | Set breakpoint by Relative Virtual Address (RVA) | 按相对虚拟地址（RVA）设置断点                              |
| checksec    | Check for various security options of binary     | 检查二进制文件的各种安全选项                                |
| cmpmem      | Compare content of a memory region with a file   | 将内存区域的内容与文件进行比较                              |
| context     | Display various information of current execution context | 显示当前执行上下文的各种信息                        |
| context_code| Display nearby disassembly at $PC of current execution context | 显示当前执行上下文中 $PC 附近的反汇编代码         |
| context_register | Display register information of current execution context | 显示当前执行上下文的寄存器信息                     |
| context_stack   | Display stack of current execution context   | 显示当前执行上下文的堆栈信息                                |
| crashdump   | Display crashdump info and save to file          | 显示崩溃转储信息并保存到文件                                |
| deactive    | Bypass a function by ignoring its execution (eg sleep/alarm) | 通过忽略函数的执行来绕过该函数（例如 sleep/alarm） |
| distance    | Calculate distance between two addresses         | 计算两个地址之间的距离                                      |
| dumpargs    | Display arguments passed to a function when stopped at a call instruction | 在停止于调用指令时显示传递给函数的参数            |
| dumpmem     | Dump content of a memory region to raw binary file | 将内存区域的内容转储为原始二进制文件                 |
| dumprop     | Dump all ROP gadgets in specific memory range    | 在指定的内存范围内转储所有 ROP 小工具                      |
| eflags      | Display/set/clear/toggle value of eflags register | 显示/设置/清除/切换 eflags 寄存器的值               |
| elfheader   | Get headers information from debugged ELF file   | 获取调试 ELF 文件的头信息                                   |
| elfsymbol   | Get non-debugging symbol information from an ELF file | 获取 ELF 文件中的非调试符号信息                      |
| gennop      | Generate abitrary length NOP sled using given characters | 使用给定字符生成任意长度的 NOP sled               |
| getfile     | Get exec filename of current debugged process    | 获取当前调试进程的可执行文件名                              |
| getpid      | Get PID of current debugged process              | 获取当前调试进程的 PID                                      |
| goto        | Continue execution at an address                 | 在指定地址继续执行                                          |
| help        | Print the usage manual for PEDA commands         | 打印 PEDA 命令的使用手册                                    |
| hexdump     | Display hex/ascii dump of data in memory         | 显示内存中的十六进制/ASCII 转储数据                         |
| hexprint    | Display hexified of data in memory               | 显示内存中数据的十六进制表示                                |
| jmpcall     | Search for JMP/CALL instructions in memory       | 在内存中搜索 JMP/CALL 指令                                  |
| loadmem     | Load contents of a raw binary file to memory     | 将原始二进制文件的内容加载到内存中                          |
| lookup      | Search for all addresses/references to addresses which belong to a memory range | 搜索属于某个内存范围的所有地址/引用地址 |

## Installation

    git clone https://github.com/longld/peda.git ~/peda
    echo "source ~/peda/peda.py" >> ~/.gdbinit
    echo "DONE! debug your program with gdb and enjoy"

## Screenshot
![start](http://i.imgur.com/P1BF5mp.png)

![pattern arg](http://i.imgur.com/W97OWRC.png)

![patts](http://i.imgur.com/Br24IpC.png)
