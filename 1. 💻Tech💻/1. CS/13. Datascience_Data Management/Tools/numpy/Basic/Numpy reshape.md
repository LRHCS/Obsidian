```python
import numpy as np  
  
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])  
  
newarr = arr.reshape(4, 3)  # returns 4 1D arrays, in each there are 3 numbers
  
print(newarr)
```