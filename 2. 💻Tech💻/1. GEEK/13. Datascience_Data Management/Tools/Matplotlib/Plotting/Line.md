```python
import matplotlib.pyplot as plt  
import numpy as np  
  
ypoints = np.array([3, 8, 1, 10, 5, 7]) # x is default 1,2,3,4...
  
plt.plot(ypoints)  
plt.show()
```

```python
import matplotlib.pyplot as plt  
import numpy as np  
  
xpoints = np.array([1, 2, 6, 8])  
ypoints = np.array([3, 8, 1, 10])  
  
plt.plot(xpoints, ypoints,"o") # with "o" is only show the points  
plt.show()
```

