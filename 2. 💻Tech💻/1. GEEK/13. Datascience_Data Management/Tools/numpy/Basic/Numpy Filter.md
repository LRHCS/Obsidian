two ways
1. use for loops
```python
import numpy as np  
  
arr = np.array([1, 2, 3, 4, 5, 6, 7])  
  
# Create an empty list  
filter_arr = []  
  
# go through each element in arr  
for element in arr:  
  # if the element is completely divisble by 2, set the value to True, otherwise False  
  if element % 2 == 0:  
    filter_arr.append(True)  
  else:  
    filter_arr.append(False)  
  
newarr = arr[filter_arr]  
  
print(filter_arr)  
print(newarr)
```
2. Directly from the array
```python
import numpy as np  
  
arr = np.array([41, 42, 43, 44])  
  
filter_arr = arr > 42  
  
newarr = arr[filter_arr]  
  
print(filter_arr)  
print(newarr)
```

