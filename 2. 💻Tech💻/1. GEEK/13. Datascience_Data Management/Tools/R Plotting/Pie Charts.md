#R     

## Pie
```R
# Create a vector of pies  
x <- c(10,20,30,40)  
  
# Display the pie chart  
pie(x)
```
start angel
```R
# Create a vector of pies  
x <- c(10,20,30,40)  
  
# Display the pie chart and start the first pie at 90 degrees  
pie(x, init.angle = 90)
```
label for each part of the pie
```R
# Create a vector of pies  
x <- c(10,20,30,40)  
  
# Create a vector of labels  
mylabel <- c("Apples", "Bananas", "Cherries", "Dates")  
  
# Display the pie chart with labels  
pie(x, label = mylabel, main = "Fruits")
```
personlize the colors of the pie
```R
  
# Create a vector of colors  
colors <- c("blue", "yellow", "green", "black")  
  
# Display the pie chart with colors  
pie(x, label = mylabel, main = "Fruits", col = colors)
```
Legend
```R
  
# Create a vector of labels  
mylabel <- c("Apples", "Bananas", "Cherries", "Dates")  
  
# Create a vector of colors  
colors <- c("blue", "yellow", "green", "black")  
  
# Display the pie chart with colors  
pie(x, label = mylabel, main = "Pie Chart", col = colors)  
  
# Display the explanation box  
legend("bottomright", mylabel, fill = colors)
```
the position
`bottomright`, `bottom`, `bottomleft`, `left`, `topleft`, `top`, `topright`, `right`, `center`