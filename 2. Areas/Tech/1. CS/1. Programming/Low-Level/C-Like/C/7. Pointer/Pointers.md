#C  #pointers   
## Example
```C
int myAge = 43; // an int variable  
  
printf("%d", myAge);  // Outputs the value of myAge (43)  
printf("%p", &myAge); // Outputs the memory address of myAge (0x7ffe5367e044)
```


In the example above, `&myAge` is also known as a **pointer**.

A **pointer** is a variable that stores the memory address of another variable as its value.

A **pointer variable** **points to a data type** (like `int`) of the same type, and is created with the `*` operator. The address of the variable you're working with is assigned to the pointer:

```C
int myAge = 43;     // An int variable  
**int* ptr = &myAge;**  // A pointer variable, with the name ptr, that stores the address of myAge  
  
// Output the value of myAge (43)  
printf("%d\n", myAge);  
  
// Output the memory address of myAge (0x7ffe5367e044)  
printf("%p\n", &myAge);  
  
// Output the memory address of myAge with the pointer (0x7ffe5367e044)  
printf("%p\n", ptr);
```

  
In the example above, we used the pointer variable to get the memory address of a variable (used together with the `&` **reference** operator).

However, you can also get the value of the variable the pointer points to, by using the `*` operator (the **dereference** operator):

### Example
```C
int myAge = 43;     // Variable declaration  
int* ptr = &myAge;  // Pointer declaration  
  
// Reference: Output the memory address of myAge with the pointer (0x7ffe5367e044)  
printf("%p\n", ptr);  
  
// Dereference: Output the value of myAge with the pointer (43)  
printf("%d\n", *ptr);
```