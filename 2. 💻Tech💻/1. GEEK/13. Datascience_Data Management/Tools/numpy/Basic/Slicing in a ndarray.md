[start:end] or [start:end:step]
If we don't pass start its considered 0

If we don't pass end its considered length of array in that dimension

If we don't pass step its considered 1
```python
import numpy as np  
  
arr = np.array([1, 2, 3, 4, 5, 6, 7])  
  
print(arr[1:5])

arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])  
  
print(arr[1, 1:4])

import numpy as np  
  
arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])  
  
print(arr[0:2, 1:4]) # [[2 3 4][7 8 9]]
```