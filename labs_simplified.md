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
Lab 6: using reduce
```python
from functools import reduce
def get_maxnumber(numbers):
    return reduce(max_of_two,numbers)

def max_of_two(x,y):
    return x if x > y else y
```    


Lab 6: using lambda function
```python
from functools import reduce
def get_maxnumber(numbers):
    return reduce(lambda x, y: x if x > y else y, numbers)
```    

Lab 7: pythonic way
```python
def remove_duplicates(L):
	return list(set(L))
```
Note: it returns the sorted list without duplicates.

Lab 12: Most frequent word
```python
import sys
def frequent(f):
    words = f.read().strip().split()
    count = {}    
    maxCount = 0                               
    for word in words:
        if word in count:
            count[word] += 1                                                       
        else:
            count[word] = 1
        if count[word] > maxCount:
            maxWord = word
            maxCount = count[word]                                   
    return maxWord, maxCount


file = sys.argv[1]
if file:
    word, frequency = frequent(open(file))
    print(file + ',', '"' + word + '"', frequency)   
```

Output:
```
python frequent.py file1.txt -> file1.txt, "the" 12
```
