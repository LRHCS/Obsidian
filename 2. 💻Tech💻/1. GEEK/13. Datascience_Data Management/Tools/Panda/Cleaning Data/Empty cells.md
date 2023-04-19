
- dropna()
```python
import pandas as pd  
  
df = pd.read_csv('data.csv')  
  
new_df = df.dropna()  
  
print(new_df.to_string())
```

- fillna()
```python
import pandas as pd  
  
df = pd.read_csv('data.csv')  
  
df.fillna(130, inplace = True)
```