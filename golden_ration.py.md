```python
# Continued fraction
# phi = 1+1/(1+phi)
# phi = 1+1/(1+1+1/(1+1+1/(1+1+1/(1+...

from fractions import Fraction

def phi(n):    
    if n == 1:
        return 1
    else:
        return Fraction(1+(1/phi(n-1)))


for n in range(1,10):
    print('%4d'%n,phi(n),end='\t')
    print(phi(n).__float__())
```

```
   1 1	1.0
   2 2	2.0
   3 3/2	1.5
   4 5/3	1.6666666666666667
   5 8/5	1.6
   6 13/8	1.625
   7 21/13	1.6153846153846154
   8 34/21	1.619047619047619
   9 55/34	1.6176470588235294
```
