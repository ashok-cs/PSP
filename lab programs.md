```python
def bsearch(L, key):
    if not L:
        return False
    mid = len(L) // 2
    if L[mid] == key:
        return True
    elif L[mid] > key:
        return bsearch(L[:mid], key)
    else:
        return bsearch(L[mid+1:], key)
```
