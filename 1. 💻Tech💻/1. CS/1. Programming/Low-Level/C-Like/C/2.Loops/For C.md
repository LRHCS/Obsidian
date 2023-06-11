 #C #loops   
## Syntax
```C
for (_statement 1_; _statement 2_; _statement 3_) {  
  _// code block to be executed_  
}
```

**Statement 1** is executed (one time) before the execution of the code block.

**Statement 2** defines the condition for executing the code block.

**Statement 3** is executed (every time) after the code block has been executed.

The example below will print the numbers 0 to 4:
```C
int i;  
  
for (i = 0; i < 5; i++) {  
  printf("%d\n", i);  
}
```