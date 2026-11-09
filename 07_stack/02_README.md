02.asm

the program starts

-the (call work)function-> the 'call' instruction executes in _start. The CPU automatically pushes the return address onto the stack and the rsp decreases by 8 bytes.

push rbh : is inside 'work' the original base pointer of the celler is saved onto the stack and the rsp decreases by 8 bytes.
-mov rbp,rsp - the base pointer is updated to mirror rhw current stack pointerrbp now acts as a fixed anchor for the new stack frame
-sub rsp,16 - the program lowers the stack pointer by 16 bytes which reserves space for two-eight byte local variables.

-mov qword [rbp - 8], 100 - the program writes 100 in the first slot 
-mov qword [rbp - 16], 200 - writes 200 in the second slot
-these values are then moved into rax and rbx. 

mov rsp, rbp`: The stack pointer is instantly snapped back to the base pointer, effectively instantly deallocating the 16 bytes of local variables.
-pop rbp: The caller's original Base Pointer is restored from the stack. `rsp` increases by 8 bytes and now points exactly at the return address.

-`ret` pops the return address off the stack into the instruction pointer (`rip`). `rsp` increases by 8 bytes, restoring the exact stack state from before the `call`.

Runtime Observations

When I followed the stack step by step, I could see how space was reserved for local variables and then released before returning.
This helped me understand why stack frames are important for keeping function data organized.
