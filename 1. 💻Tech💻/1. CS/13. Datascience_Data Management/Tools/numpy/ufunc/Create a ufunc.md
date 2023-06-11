```python
import numpy as np  
  
def myadd(x, y):  
  return x+y  
  
myadd = np.frompyfunc(myadd, 2, 1)  
  
print(myadd([1, 2, 3, 4], [5, 6, 7, 8]))
```

The `frompyfunc()` method takes the following arguments:

1.  `_function_` - the name of the function.
2.  `_inputs_` - the number of input arguments (arrays).
3.  `_outputs_` - the number of output arrays.