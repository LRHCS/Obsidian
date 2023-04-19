 #C   

## Break
Break can be used for jumped out of a loop

```C
int i;  
  
for (i = 0; i < 10; i++) {  
  if (i == 4) {  
    break;  
  }  
  printf("%d\n", i);  
}
```

## Continue
The `continue` statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

```C
int i;  
  
for (i = 0; i < 10; i++) {  
  if (i == 4) {  
    continue;  
  }  
  printf("%d\n", i);  
}
```