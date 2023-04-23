 #R #if_else   
## If-else
the if else in R is as same as in other languages
```R
a <- 200  
b <- 33  
  
if (b > a) {  
  print("b is greater than a")  
} else if (a == b) {  
  print("a and b are equal")  
} else {  
  print("a is greater than b")  
}
```

## And
there is also and represented with &
```R
a <- 200  
b <- 33  
c <- 500  
  
if (a > b & c > a){  
  print("Both conditions are true")  
}
```
## Or
there is also or represented with |
```R
a<- 200  
b <- 33  
c <- 500  
  
if (a > b | a > c){  
  print("At least one of the conditions is true")  
}

```
