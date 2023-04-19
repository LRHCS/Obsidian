copy is a copy of an array, when you change the data in the original array, the data of the copy **will not change**, the copy **owns the data**
```python
import numpy as np  
  
arr = np.array([1, 2, 3, 4, 5])  
x = arr.copy()  
arr[0] = 42  
  
print(arr)  
print(x)
```
view is also a type of a copy, but when you change the data in the original array, the data of the copy **will change**, the copy **dont own the data, it shares with the original array**
```python
import numpy as np  
  
arr = np.array([1, 2, 3, 4, 5])  
x = arr.view()  
arr[0] = 42  
  
print(arr)  
print(x)
```
check as if it owns it or not
```python
print(a.base) # copy will return none
print(b.base) # view will return the base array
```