 #R   
A list in R can contain many different data types inside it. A list is a collection of data which is ordered and changeable.
```R
  
# List of strings  
thislist <- list("apple", "banana", "cherry")  
  
# Print the list  
thislist
```
with [] you can access the element in this list, but other than other languages, the index begins with 1.
```R
thislist <- list("apple", "banana", "cherry")  
  
thislist[1]
```
return the length of the list
```R
thislist <- list("apple", "banana", "cherry")  
  
length(thislist)
```
check if the element exist in this list
```R
thislist <- list("apple", "banana", "cherry")  
  
"apple" %in% thislist
```
add element
```R
  
thislist <- list("apple", "banana", "cherry")  
  
append(thislist, "orange")
```
add the element in a specific position
```R
thislist <- list("apple", "banana", "cherry")  
  
append(thislist, "orange", after = 2)
```
join to list together
```R
  
list1 <- list("a", "b", "c")  
list2 <- list(1,2,3)  
list3 <- c(list1,list2)  
  
list3
```
loop through
```R
thislist <- list("apple", "banana", "cherry")  
  
for (x in thislist) {  
  print(x)  
}
```