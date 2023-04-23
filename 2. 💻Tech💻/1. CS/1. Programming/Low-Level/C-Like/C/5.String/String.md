 #C #String   
## Syntax
```C
char greetings[] = "Hello World!";
printf("%s", greetings);
```
## Access
The Strings in C is store as an array, so you can access a string as same as an array
```C
char greetings[] = "Hello World!"; 
// Output will be H
printf("%c", greetings[0]);
```
## Modify Strings
```C
char greetings[] = "Hello World!";  
greetings[0] = 'J';  
printf("%s", greetings);  
// Outputs Jello World! instead of Hello World!
```