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
    return [num for num in range(min, max + 1) if isPrime(num)]

def isPrime(num):
    if num < 2:
        return False
    for i in range(2, num):
        if num % i == 0:
            return False
    return True
```

lab 4: 
```python
def linear_search(mylist, token):
    for elem in mylist:
        if elem is token:
            return True
    return False
```

Lab 4: 
```python
def linear_search(mylist, token):
    return (token in mylist)        
```
