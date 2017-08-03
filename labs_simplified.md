Lab1:

```python
def gcd(number1, number2):
    while number2:
	        (number1, number2) = (number2, number1 % number2)
    return number1
```

Lab 5:
```python
def generate_primes(min, max):    
    return [num for num in range(min, max + 1)if isPrime(num)]

def isPrime(num):
    if num < 2:
        return False
    for i in range(2, num):
        if num % i == 0:
            return False
    return True
```
