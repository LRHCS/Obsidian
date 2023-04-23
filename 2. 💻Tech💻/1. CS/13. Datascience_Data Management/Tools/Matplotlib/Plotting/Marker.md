...  
plt.plot(ypoints, marker = '*')  
...

![[Pasted image 20221106171814.png]]

```python
import matplotlib.pyplot as plt  
import numpy as np  
  
ypoints = np.array([3, 8, 1, 10])  
  
plt.plot(ypoints, 'o:r')  
plt.show()
```

![[Pasted image 20221106171928.png]]
![[Pasted image 20221106171934.png]]

```python
import matplotlib.pyplot as plt  
import numpy as np  
  
ypoints = np.array([3, 8, 1, 10])  
  
plt.plot(ypoints, marker = 'o', ms = 20)  # with ms you can specify the size of the marker
plt.show()
```