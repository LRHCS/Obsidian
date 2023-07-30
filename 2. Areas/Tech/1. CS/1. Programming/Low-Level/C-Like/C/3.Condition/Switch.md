#C    
## Syntax 
```C
switch(_expression_) {  
  case x:  
    _// code block_  
    break;  
  case y:  
    _// code block_  
    break;  
  default:  
    _// code block_  
}
```

## Example
```C
int day = 4;  
  
switch (day) {  
  case 1:  
    printf("Monday");  
    break;  
  case 2:  
    printf("Tuesday");  
    break;  
  case 3:  
    printf("Wednesday");  
    break;  
  case 4:  
    printf("Thursday");  
    break;  
  case 5:  
    printf("Friday");  
    break;  
  case 6:  
    printf("Saturday");  
    break;  
  case 7:  
    printf("Sunday");  
    break;  
  default:
	printf("Are you human?");
	break;
}
```

-   The `switch` expression is evaluated once
-   The value of the expression is compared with the values of each `case`
-   If there is a match, the associated block of code is executed
-   The `break` statement breaks out of the switch block and stops the execution
-   The `default` statement is optional, and specifies some code to run if there is no case match