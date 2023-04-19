.where, normal search
```python
import numpy as np  
  
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])  
  
x = np.where(arr%2 == 0)  
  
print(x)
```

There is a method called `searchsorted()` which performs a binary search in the array, and returns the index where the specified value would be inserted to maintain the search order.

```python
import numpy as np

arr = np.array([1, 3, 5, 7])

x = np.searchsorted(arr, [2, 4, 6], side="right")

print(x)
# [1 2 3]
```