
```python
import numpy as np

# 1 dimension
arr = np.array([1,2,3])

arr = np.arange(10) # return a ndarray fill from 0 to 10
# 2 dimension
arr2 = np.array([[1,2,3],[1,2,3]])
# 3 dimension
arr3 = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])
# Check dimensions
arr.ndim
arr2.ndim
arr3.ndim
```