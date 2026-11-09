01.asm

this program is using LIFO behaviour -push /pop

-the program begins as the stack pointer points to the top of the stack set up by the operating system.

-  mov rax, 100 and mov rbx, 200 loads values into the register .

-push rax : the cpu subtracts 8 bytes from rsp then writes the values of rax = 100 to the memory address now stored in rsp.
-push rbx : CPU subtracts 8 bytes from rsp and writes the value of rbx = 200 to the new address at the top of the stack. the stack now has 200 on top and 100 below it

-pop rcx : CPU reads the current top 8 bytes value which is = 200 and places it in rcx then adds 8 bytes to rsp removing 200 of the stack and leaving 100 on the top.
-pop rdx :  here the CPU reads the top 8bytes which holds the value =100  and places it into rdx. then adds another 8 bytes in to rsp.

the program performs a standard system cal to exit cleanly

Runtime Observations
The program exits using the Linux exit system call.
While testing, I noticed that every push moved rsp down by 8 bytes and every pop moved it back up by 8 bytes.
This program clearly shows how the stack stores and retrieves data in reverse order.
