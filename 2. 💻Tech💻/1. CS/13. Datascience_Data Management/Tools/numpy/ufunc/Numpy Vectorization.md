Converting iterative statements into a [[Vektoren]] based operation is called vectorization.

```python
import numpy as np  
  
x = [1, 2, 3, 4]  
y = [4, 5, 6, 7]  
z = np.add(x, y)  
z = np.substract(x, y)
z = np.multiply(x, y)
z = np.divide(x, y)
z = np.power(x, y)
z = np.mod(x, y)
z = np.divmod(x, y)

z = np.sum(x, y)
z = np.prod(x, y)
z = np.diff(x, y)

z = np.lcm(x) # ## Lowest Common Multiple
z = np.gcd(x) # ## Greatest Common Denominator

print(z)
```