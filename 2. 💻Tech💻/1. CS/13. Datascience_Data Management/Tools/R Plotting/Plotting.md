#R     

# Plot
```R
plot(1, 3)
```
output:
![[Pasted image 20220611154159.png]]

multiple points
```R
plot(c(1, 8), c(3, 10))
```
output:
![[Pasted image 20220611154231.png]]
```R
x <- c(1, 2, 3, 4, 5)  
y <- c(3, 7, 8, 9, 12)  
  
plot(x, y)
```
output:
![[Pasted image 20220611154354.png]]

you can also output sequence of points
```R
plot(1:10)
```
![[Pasted image 20220611154428.png]]
Compare between two things, use points()
```R
# day one, the age and speed of 12 cars:  
x1 <- c(5,7,8,7,2,2,9,4,11,12,9,6)  
y1 <- c(99,86,87,88,111,103,87,94,78,77,85,86)  
  
# day two, the age and speed of 15 cars:  
x2 <- c(2,2,8,1,15,8,12,9,7,3,11,4,7,14,12)  
y2 <- c(100,105,84,105,90,99,90,95,94,100,79,112,91,80,85)  
  
plot(x1, y1, main="Observation of Cars", xlab="Car age", ylab="Car speed", col="red", cex=2)  
points(x2, y2, col="blue", cex=2)
```
## Line
```R
plot(1:10, type="l")
```
width
```R
plot(1:10, type="l", lwd=2)
```
style
```R
plot(1:10, type="l", lwd=5, lty=3)
```
-   `0` removes the line
-   `1` displays a solid line
-   `2` displays a dashed line
-   `3` displays a dotted line
-   `4` displays a "dot dashed" line
-   `5` displays a "long dashed" line
-   `6` displays a "two dashed" line

multiple lines
```R
line1 <- c(1,2,3,4,5,10)  
line2 <- c(2,5,7,8,9,10)  
  
plot(line1, type = "l", col = "blue")  
lines(line2, type="l", col = "red")
```
## Label
```R
# main is the title, xlab and ylab is the title for each axis
plot(1:10, main="My Graph", xlab="The x-axis", ylab="The y axis")
```
change the color 
```R
plot(1:10, col="red")
```
size
```R
plot(1:10, cex=2)
```
shape
```R
plot(1:10, pch=25, cex=2)
```
different shapes
![[Pasted image 20220611154737.png]]
with all parameter
```R
plot(1:10, xlab="x", ylab="y", main = "title", cex=2, pch=24,col="red")
```
![[Pasted image 20220611155026.png]]