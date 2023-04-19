 #java #Array    
To declare an array, define the variable type with **square brackets**:

```java
String[] cars;
```

## Access the Elements of an Array

You access an array element by referring to the index number.

This statement accesses the value of the first element in cars:

### Example

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]);
// Outputs Volvo
```

## Loop through an Array

### Example

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (int i = 0; i < cars.length; i++) {
  System.out.println(cars[i]);
}
```

## Multidimension
### Example

```java
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
```


```java
public class Main {
  public static void main(String[] args) {
    int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
    for (int i = 0; i < myNumbers.length; ++i) {
      for(int j = 0; j < myNumbers[i].length; ++j) {
        System.out.println(myNumbers[i][j]);
      }    
    }
  }
}
```