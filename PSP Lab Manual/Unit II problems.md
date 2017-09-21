1. GCD
2. Palindrome
3. Exchange of two variables
4. Circulate the values of n variables
5. Distance between two points
6. Celsius to Fahrenheit and vice-versa
7. Lamda function
8. modules and functions
9. tuple illustration
10. Recursive function
11. global vs local
12. default vs keyword arguments
13. map, filter, reduce
14. type casting vs type coersion


# 1. GCD

### using iteration

```python
def gcd(a, b):
  while b != 0:
    a, b = b, a % b
  return a
```  
### using recursion
```python
def gcd(a, b):
  if b == 0:
    return a
  return gcd(b, a % b)
```

# 2. Palindrome number
### using iteration
```python
def palindrome(number):
  reverse = 0
  given = number
  while number > 0:
    reverse = reverse * 10 + number % 10
    number = number // 10
  return given == reverse
```

# 3. Exchange two values
```python
a = 10
b = 20
temp = b
b = a
a = temp
print(a, b)
(20, 10)
```  
# 4. Circulate N values
```python
N = [2, 3, 4, 5, 6]
last = len(N)-1
temp = N[last]
for index in range(last, 1, -1):
  N[index] = N[index-1]
N[0] = temp
print(N)
[6, 3, 3, 4, 5]
```

# 5. Distance between two points

![graph](http://www.mathwarehouse.com/algebra/distance_formula/images/distance-formula-picture.jpg)

<a href="https://www.codecogs.com/eqnedit.php?latex=$&space;\text{&space;Distance&space;}&space;=&space;\sqrt{(x_2&space;-x_1)^2&space;&plus;&space;(y_2-&space;y_1)^2}&space;$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$&space;\text{&space;Distance&space;}&space;=&space;\sqrt{(x_2&space;-x_1)^2&space;&plus;&space;(y_2-&space;y_1)^2}&space;$" title="$ \text{ Distance } = \sqrt{(x_2 -x_1)^2 + (y_2- y_1)^2} $" /></a>

```python
from math import sqrt
(X1, Y1) = (1, 2)
(X2, Y2) = (4, 6)
Distance = sqrt((X2 -X1)**2 + (Y2- Y1)**2)
print(Distance)
5.0
```

# 6. Celsius to Fahrenheit and vice-versa

### Fahrenheit to Celsius
<a href="https://www.codecogs.com/eqnedit.php?latex=F&space;=&space;\frac{9}{5}C&space;&plus;&space;32" target="_blank"><img src="https://latex.codecogs.com/gif.latex?F&space;=&space;\frac{9}{5}C&space;&plus;&space;32" title="F = \frac{9}{5}C + 32" /></a>

```python
C = 35 
F = 9/5*C + 32
print(F)
95.0
```
### Celsius to Fahrenheit
<a href="https://www.codecogs.com/eqnedit.php?latex=C&space;=&space;(F-32)\frac{5}{9}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?C&space;=&space;(F-32)\frac{5}{9}" title="C = (F-32)\frac{5}{9}" /></a>

```python
F = 95.0
C = (F-32)*(5/9)
print(C)
35.0
```

# 7. Lamda Function
```python
mul = lambda x,y: x*y
print(mul(3,4))
12
```

# 13. map, filter, reduce
### filter
```python
N = [2, 3, 4, 7, 8, 10]
even = lambda x: x % 2 == 0
result = list(filter(even, N))
print(result)
[2, 4, 8, 10]
```
### map
```python
N = [2, 3, 4, 7, 8, 10]
double = lambda x: x*2
result = list(map(double, N))
[4, 6, 8, 14, 16, 20]
```

### reduce
```python
N = [2, 3, 4, 7, 8, 10]
add = lambda x,y: x+y
from functools import reduce
result = reduce(add, N)
print(result)
34
```

# 8. modules and functions
```python
import math
dir(math)  # Functions in the math module
['acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'pi', 'pow', 'radians', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']
math.sqrt(2)
1.4142135623730951
math.gcd(12,18)
6
```
# 9. tuple illustration
```python
T = (2, 3, 4, 5, 6)
max(T) # maximum in T   6
min(T) # minimum in T   2
A = T  # duplicate T
T[1:4] # (3, 4, 5)
L = list(T) # convert tuple to a list
[2, 3, 4, 5, 6]
```

# 10. Recursive function
```python
def gcd(a, b):
  if b == 0:
    return a
  return gcd(b, a % b)
```

# 11. global vs local
```python
a = 10 # global

def add20(num):
  a = 20 # local
  return num + a

def add10(num):
  global a
  return num + a

print(add20(5))
25
print(add10(5))
15
```
