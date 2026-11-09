1] Program Start
-eax is loaded with 0x11223344.
-ebx is loaded with 0x1234.
-The stack pointer (esp) is in its initial position.

2] Pushing Values onto the Stack
-push eax stores the value in eax.
-esp decreases by 4 bytes.
-push ebx stores the value in ebx.
-esp decreases by another 4 bytes.

3] Popping Values from the Stack
-pop ebx restores the value 0x1234.
-esp increases by 4 bytes.
-pop eax restores the original value in eax.
esp increases by another 4 bytes.

4] Following the LIFO Rule
-The last value pushed is the first value removed.
-This ensures register values are restored correctly.