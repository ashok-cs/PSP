Lab1:
```python
def gcd(number1, number2):
    while number2:
	        (number1, number2) = (number2, number1 % number2)
    return number1
```

lab 4: linear search
```python
def linear_search(mylist, token):
    for elem in mylist:
        if elem is token:
            return True
    return False
```

Lab 4: pythonic search
```python
def linear_search(mylist, token):
    return (token in mylist)        
```

Lab 4: binary search
```python
def bsearch(mylist, token):
    if not mylist:
        return False
    mid = len(mylist)//2    
    if mylist[mid] is token:
        return True
    elif mylist[mid] > token:
        return bsearch(mylist[:mid], token)
    else:
        return bsearch(mylist[mid+1:], token)
```
Lab 5: using list comprehension
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

Lab 7: pythonic way
```python
def remove_duplicates(L):
	return list(set(L))
```
Note: it returns the sorted list without duplicates.

