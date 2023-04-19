#C   #function    
A function is a block of code which only runs when it is called.

You can pass data, known as parameters, into a function.

Functions are used to perform certain actions, and they are important for reusing code: Define the code once, and use it many times.

---

## Predefined Functions

So it turns out you already know what a function is. You have been using it the whole time while studying this tutorial!

For example, `main()` is a function, which is used to execute code, and `printf()` is a function; used to output/print text to the screen:

```C
int main() {  
  **printf(**"Hello World!"**)**;  
  return 0;  
}
```

## Create a function
  
To create (often referred to as _declare_) your own function, specify the name of the function, followed by parentheses `()` and curly brackets `{}`:
### Syntax
```C 
void _myFunction_() {  
  // code to be executed  
}
```

## Parameters
```C  
returnType_ _functionName_(_parameter1_, _parameter2_, _parameter3_) {  
  // code to be executed  
}
```

## Declaration
```C
// **Function declaration**  
void myFunction();  
  
// The main method  
int main() {  
  myFunction();  // **call** the function  
  return 0;  
}  
  
// **Function definition**  
void myFunction() {  
  printf("I just got executed!");  
}
```

## Recursion
Recursion is the technique of making a function call itself. This technique provides a way to break complicated problems down into simple problems which are easier to solve.
```C
int sum(int k);  
  
int main() {  
  int result = sum(10);  
  printf("%d", result);  
  return 0;  
}  
  
int sum(int k) {  
  if (k > 0) {  
    return k + sum(k - 1);  
  } else {  
    return 0;  
  }  
}
```