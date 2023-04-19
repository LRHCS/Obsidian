 #R    
## Matrix
### Create a Matrix
```R
# Create a matrix  
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)  
  
# Print the matrix  
thismatrix
```
we can also make a Matrix with strings
```R
thismatrix <- matrix(c("apple", "banana", "cherry", "orange"), nrow = 2, ncol = 2)  
  
thismatrix[1, 2]
```
```R
thismatrix <- matrix(c("apple", "banana", "cherry", "orange"), nrow = 2, ncol = 2)  

thismatrix[2,]
```
with no number after comma it will return a row
```R
  
thismatrix <- matrix(c("apple", "banana", "cherry", "orange"), nrow = 2, ncol = 2)  
  
thismatrix[,2]
```
this will return whole column
### Add row and column
with cbind() it will add a addtional column
```R
thismatrix <- matrix(c("apple", "banana", "cherry", "orange","grape", "pineapple", "pear", "melon", "fig"), nrow = 3, ncol = 3)  
  
newmatrix <- cbind(thismatrix, c("strawberry", "blueberry", "raspberry"))  
  
# Print the new matrix  
newmatrix
```
with rbind() it will add a additional row
```R
thismatrix <- matrix(c("apple", "banana", "cherry", "orange","grape", "pineapple", "pear", "melon", "fig"), nrow = 3, ncol = 3)  
  
newmatrix <- rbind(thismatrix, c("strawberry", "blueberry", "raspberry"))  
  
# Print the new matrix  
newmatrix
```
### number of row and column
with dim()
```R
thismatrix <- matrix(c("apple", "banana", "cherry", "orange"), nrow = 2, ncol = 2)  
  
dim(thismatrix)
```