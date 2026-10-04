1] mul1
25 * 10
AX = 250
AL = 0xFA AH = 0x00

Carry Flag = 0 and OverflowFlag = 0 For a MUL instruction, the CPU checks the upper half of the resulting register. If the upper half AH is  0, the CPU clears both CarryFlag and Overflow Flag. Because 250 easily fits inside the lower 8 bits AL, AH remains zero, clearing the flags.

2] mul2
3000 * 200 =600000
carry flag = 1
overflow flag = 1 600,000 exeeds the 16 bit register capacity which is 65000 thus the cpu overflows the data to the upperhalf of the register.