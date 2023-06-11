pd.read_csv("filename.csv")

```python
import pandas as pd  
  
pd.options.display.max_rows = 9999  # this line is only for the display all of the line, otherwise we need to write df.tostring(), or it will only output first and last 5 lines
  
df = pd.read_csv('data.csv')  
  
print(df)
```


pd.read_json("filename.json")