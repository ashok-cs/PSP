```python
def fibo(n):
    if n <= 1:
        return n
    else:
        return fibo(n-1) + fibo(n-2)




def linear_fibo(n):    
    if (n <= 1):
        return (n,n-1)
    else:
        a,b= linear_fibo(n-1)
        return (a+b,a)

    
for n in range(10):
    fn, _ = linear_fibo(n)
    print(n, fn)
    
###  using cache   
cache={}
def fibo_cache(n):
    if n in cache:
        return cache[n]
    if n <= 1:
        cache[n] = n
        return n
    else:
        val= fibo_cache(n-1) + fibo_cache(n-2)
        cache[n] = val
        return val
    

###  using lru_cache
#lru - least recently used

from functools import lru_cache

@lru_cache(maxsize=1000)
def fibo_lru(n):
    if n <= 1:
        return n
    else:
        return fibo_lru(n-1) + fibo_lru(n-2)


for n in range(10):
    fn = fibo_lru(n)
    print(n, fn)     
```
