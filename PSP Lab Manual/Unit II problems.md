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

$
\text{ Distance } = \sqrt{(x_2 -x_1)^2 + (y_2- y_1)^2}
$
