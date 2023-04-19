#R     
# Bar
```R
# x-axis values  
x <- c("A", "B", "C", "D")  
  
# y-axis values  
y <- c(2, 4, 6, 8)  
  
barplot(y, names.arg = x)
```

density
```R
  
x <- c("A", "B", "C", "D")  
y <- c(2, 4, 6, 8)  
  
barplot(y, names.arg = x, density = 10)
```

width
```R
  
x <- c("A", "B", "C", "D")  
y <- c(2, 4, 6, 8)  
  
barplot(y, names.arg = x, width = c(1,2,3,4))
```

horizontal
```R
  
x <- c("A", "B", "C", "D")  
y <- c(2, 4, 6, 8)  
  
barplot(y, names.arg = x, horiz = TRUE)
```