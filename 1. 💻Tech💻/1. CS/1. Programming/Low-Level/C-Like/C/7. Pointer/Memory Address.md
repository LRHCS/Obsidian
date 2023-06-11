#C  #pointers   
When a variable is created in C, a memory address is assigned to the variable.

The memory address is the location of where the variable is stored on the computer.

When we assign a value to the variable, it is stored in this memory address.

To access it, use the reference operator (`&`), and the result will represent where the variable is stored:

```C
int myAge = 43;  
printf("%p", &myAge); // Outputs 0x7ffe5367e044
```