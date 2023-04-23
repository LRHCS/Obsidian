It's like an column in a table, 1D array

```python
import pandas as pd
a = [1,2,3]
myvar = pd.Series(a, index=["x", "y", "z"])
print(myvar)
```