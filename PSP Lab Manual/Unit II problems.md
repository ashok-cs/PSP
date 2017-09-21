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

