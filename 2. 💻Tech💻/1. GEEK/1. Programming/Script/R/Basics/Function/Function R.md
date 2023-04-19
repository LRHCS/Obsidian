#R  #function   
## Function
```R
my_function <- function() {  
  print("Hello World!")  
}  
  
**my_function()** # call the function named my_function
```
## Argument
```R
my_function <- function(fname) {  
  paste(fname, "Griffin")  
}  
  
my_function("Peter")  
my_function("Lois")  
my_function("Stewie")
```
This function will print the fname with Griffin(Peter Griffin)
## Default Argument
This is special in R, There is Default Argument
```R
my_function <- function(country = "Norway") {  
  paste("I am from", country)  
}  
  
my_function("Sweden")  
my_function("India")  
my_function() # will get the default value, which is Norway  
my_function("USA")

[Try it Yourself »](https://www.w3schools.com/r/tryr.asp?filename=demo_function_default)
```