 #C  #Array   
## Syntax
Used to store multiple value in a single variable
```C
int myNumbers[] = {25, 50, 75, 100};
```
## Access
To access an array element, refer to its **index number**. The indexes start with 0

```C
int myNumbers[] = {25, 50, 75, 100};  
// so it would be 25
printf("%d", myNumbers[0]);
```
## Change
```C
int myNumbers[] = {25, 50, 75, 100};  
myNumbers[0] = 33;  
  
printf("%d", myNumbers[0]);  
  
// Now outputs 33 instead of 25
```
## Print Array with for loop
```C
int myNumbers[] = {25, 50, 75, 100};  
int i;  
  
for (i = 0; i < 4; i++) {  
  printf("%d\n", myNumbers[i]);  
}
```

Instead of type 4 in the loop, we can also use `sizeof(myNumbers)/sizeof(int)`, with this you don't need to change the number when you change the array.

```C
int main() {  
    int myNumbers[] = {25, 50, 75, 100};

    for (int i = 0; i < sizeof(myNumbers)/sizeof(int); i++) {

        printf("%d\n", myNumbers[i]);

    }

}
```

## Define the size of the array
We can also declare the size of an array
```C
int myNumbers[4];
```