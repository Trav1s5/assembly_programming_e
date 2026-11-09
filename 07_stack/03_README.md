-the program start at _start
-`rax` is loaded with 10
-the stack remains unchanged.

-call calculate is executed
-the CPU automatically pushes the return address onto the stack
-`rsp` decreases by 8 bytes
-then the execution jumps to the calculate function.

-add rax, 5 is executed.
-rax changes from 10 to 15.
-No values are pushed or popped.
-No stack frame is created.
-rsp remains pointing to the return address.
-ret removes the return address from the stack and rsp increases by 8 bytes.

observations
-he program exits successfully.
While testing, I noticed that function calls use the stack automatically even when no local variables exist.
This example helped me understand that the stack is important for controlling program flow, not just storing data.