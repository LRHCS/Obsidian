 #R   
## Normal String
```R
"Hello World"
```
## Strings with multiple lines
At Normal, we print this normal with print() or with none, but in r, we need to use cat() for it, otherwise it will be / between the words
```R
str <- "Lorem ipsum dolor sit amet,  
consectetur adipiscing elit,  
sed do eiusmod tempor incididunt  
ut labore et dolore magna aliqua."  
  
cat(str)
```
## Length
```R
str <- "Hello World!"  
  
nchar(str)
```
## Check if a char or a word exist in a str
```R
str <- "Hello World!"  
  
grepl("H", str)  
grepl("Hello", str)  
grepl("X", str)
```
