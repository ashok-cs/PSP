```python
(x1, y1) = (0, 0)
(x2, y2) = (4, 0)
# Distance between two points
D = abs(x1-x2)
print(D)
```

```python
from math import sqrt
(x1, y1) = (0, 0)
(x2, y2) = (4, 3)
# Distance between two points
D = sqrt((x1 - x2)**2  + (y1 - y2)**2)
print(D)
```

```python
def distance(x1, y1, x2, y2):
  D = sqrt((x1 - x2)**2  + (y1 - y2)**2)
  return D
```
