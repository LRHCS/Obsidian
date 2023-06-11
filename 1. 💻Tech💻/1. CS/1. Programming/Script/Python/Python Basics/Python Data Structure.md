#python 

# Array
```python
x = [0,1,2,3,4]
# y is a copy of x, when change x, y will not be changed
y = list(x)
# if x be changed, z will also be changed
z = x
y.append(5)
for i in x:
     print(x[i])
```

---
comprehension syntax
```python
x = [x for x in range(1,100) if x%2!=0]
```
this is the same as
```python
lst = []
for i in range(1,100):
	if x%2!=0:
		lst.append(x)
```

---
- Slicing
array name [start : end : steps]
```python
lst = [1,2,3,4]
# print the list backward
print(lst[::-1])
# print from the first index to the third index
print(lst[0:2])
```

# Dictionary

 comprehension syntax
```python
{x: x*x for x in range(3,6)}
```



