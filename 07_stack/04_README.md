04.asm
-call work is executed.
-the return address is pushed onto the stack.
and since it is a 32-bit program esp decreases by 4 bytes.

-push ebp saves the old base pointer
-esp decrease by 4 bytes
-move ebp esp creates the new stack frame
-sub esp , 8 reserves space for local variables 
-esp moves down by 8 more bytes.

-mov dword [ebp - 4], 100 stores the first value.
-mov dword [ebp - 8], 200 stores the second value.
-These values are stored in the stack frame.
-esp and ebp do not change while accessing the variables.

-mov esp, ebp removes the local variable space.
-pop ebp restores the previous base pointer
- and esp inccreases it by 4 bytes

-ret removes the return address from the stack

observation
-The program exits using int 0x80.
-During testing, I observed that all stack movements happened in 4-byte steps instead of 8-byte steps.
-This made it easy to see the difference between 32-bit and 64-bit stack behavior.