 #java #if_else    
# Syntax
```java
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```
## Example
```java
int time = 22;
if (time < 10) {
  System.out.println("Good morning.");
} else if (time < 20) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening."
```


# Short-Hand
## Syntax
```java
variable = (condition) ? expressionTrue :  expressionFalse;
```

## Example
```java
int time = 20; String result = (time < 18) ? "Good day." : "Good evening."; System.out.println(result);
```