1] sub1
50 -80 = -30

carry flag = 1 = the cpu borrows 1 from an imaginary place
overflow flag = 0 = the signal result is -30 and since -30 fits between -128 and 127 the is no signal overflow .
sign flag = 1 = the msb is 1 since it is a negative number.
zero flag 0 = since the result is not a 0
parity flag = 0 the reult 11100010b contains 3 1's.

2] sub3
0-1
a] step 1 sub ax = -1

carry flag = 1 subtracting 1 from 0 requires borrowing 1 from the msb
sign flag = 1 the msb is -1 
zero flag = 0 since the reuslt is -1 not o

b] step 2 sbb ax, 0
carry flag = 0 = subtracting 1 from 0xffff doesnt require another borrow
sign flag = 1 = the msb remains 1