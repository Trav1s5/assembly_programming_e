05.asm

1] Program Start
-rax is loaded with 0x1122334455667788.
-rbx is loaded with 0x1234.
-rsp points to the top of the stack.

2]Saving Values with Push
-push rax stores the value in rax on the stack.
-rsp decreases by 8 bytes.
-push rbx stores the value in rbx.
-rsp decreases by another 8 bytes.

3]Restoring Values with Pop
-pop rbx restores the value 0x1234 into rbx.
-rsp increases by 8 bytes.
-pop rax restores the original value into rax.
-rsp increases by another 8 bytes.

Observations

-The program exits successfully.
-While testing, I saw that the stack can be used as temporary storage for register values.
