[linux 下写汇编](https://www.ibm.com/developerworks/cn/linux/l-assembly/index.html)

CPU=寄存器+运算器+控制器+内部总线
## CPU寻址
## CPU地址加法器
CPU段地址,CPU偏移地址

物理地址 = 段地址x16 + 偏移地址

CS(代码段寄存器),IP(指令指针寄存器)

8086CPU工作过程可以简要描述如下。
1. 从CS:IP指向的内存单元读取指令,读取的指令进入指令缓冲器；
1. IP=IP+所读取指令的长度,从而指向下一条指令；
1. 执行指令。转到步骤（1），重复这个过务。

在8086CPU加电启动或复位后CS和IP被设置为CS=0xFFFF，IP=0x0000,
即在8086CPU机则启动时，CPU从内存0xFFFF0单元中读取指令执行，
0xFFFF0单元中的指令是8086CPU机开机后执行的第一条指令。


`jmp 段地址：偏移地址` 用指令中给出的段地址修改CS，偏移地址修改IP。

`jmp 某一合法寄存器` 用寄存器中的值修改IP。
