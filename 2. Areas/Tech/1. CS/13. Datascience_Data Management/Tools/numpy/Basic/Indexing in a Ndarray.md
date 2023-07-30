
```python
import numpy as np

arr = np.array([1,2,3])
print(arr[0]) # will output 1
arr1 = np.array([[1,2,3],[4,5,6]])
print(arr1[1,2]) # will output 6, second array, third number
arr2 =  np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])
print(arr2[1,1,2]) # will output 12, cause second pair of array, second array and the third number 
```