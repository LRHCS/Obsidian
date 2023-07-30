A Pandas DataFrame is a 2 dimensional data structure, like a 2 dimensional array, or a table with rows and columns.

```python
import pandas as pd

data = {  
  "calories": [420, 380, 390],  
  "duration": [50, 40, 45]  
}

a = pd.DataFrame(data)
```

- loc()


```python
import pandas as pd

data = {  
  "calories": [420, 380, 390],  
  "duration": [50, 40, 45]  
}

df = pd.DataFrame(data)

a = df.loc[0]
```