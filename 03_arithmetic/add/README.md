This will have my ADD operations

1]  add1
120 + 10 
mov al, [num1]   |  add al, [num2] 
thus AL =130

Flags:
Sign FLag = 1 = since the MSB is 1 (130 in binary in 10000010)
Zero Flag = 0 = since the resulting sum is not 0
Parity FLag = 1 = the number of 1s is even 10000010
Carry Flag = 0 = the unsigned addition of 120 +c10 = 130, since an 8-bit register can hold up to 255 there is no carry out of the msb.
Overflow Flag = 1 = the result we got 10000010 with 1 as an overflow.

2]  add3
-> first we add ax[num2]
carry flag = 1 =  1 + 65535 = 65536 this requires a 17th bit causing a carry from the msb.
zero flag = 1 = the 16 bit rolls over to exactly 0
overflow flag = 0 = 0xFFFF is -1 adding 1 results in  0 thus there was no overflow
-> second adc ax, 0
carry flag = 0 the cpu adds ax 0 + 0 + 1 = 1 generating no new carry.
zero flag = 0 the result becomes a 1
