 #R #loops   
## While
the while loop is also almost the same as other languages, but there is still 1 difference, in other languages we use i += 1 to represent i = 1+1, but in R they use i <- i+1, there is no simplify way to write it
```R
i <- 1  
while (i < 6) {  
  print(i)  
  i <- i + 1  
}
```