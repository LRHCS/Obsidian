 #C #variable   
## Variable
In C you must first define the types of varible

![[Pasted image 20220531201846.png]]

```c
#include <stdio.h>  
//It defines a value PI, with define you can't change it
#define PI 3.147483647

  
  

int main(){
	// constant is also something you can't change same as define
	const int myNum = 22;
	// a variable i with the value 0
    int i= 0;
    
	// a float variable f with the value of PI 
    float f = 3.147483647;

    char c = 'a';

    char str[] = "Hello world";

    printf("%i, %f, %c, %s, %f",i,f ,c ,str, PI);

    return 0;

}
```