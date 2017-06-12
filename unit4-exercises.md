## 4.1.1 LIST OPERATIONS

1. What is the output?
```python
>>> a = 10
>>> mylist = [a]*5
>>> mylist[3]
```
2.  What is the output?
```python
>>> mylist1 = ['In', 'python']
>>> mylist2 = ['explicit','is','better']
>>> mylist = mylist1 + mylist2
>>> mylist += ['than','implicit']
>>> mylist
```
## 4.1.2 LIST SLICES
1. What is the output?
```python
>>> mylist = [12, 48, 34, 72, 56]
>>> mylist = mylist[1:-2]*2
```
2. What is the output?
```python
>>> mylist =  [12, 48, 34, 72, 56]
>>> mylist = mylist[::2] + mylist[-1::-2]
```

## 4.1.3 LIST METHODS
1. What is the error?
```python
>>> mylist =  [12, 48, 34, 72, 56]
>>> mylist.pop(2)
>>> mylist.append(mylist.index(34))
```
2. What is the output?
```python
>>> mylist =  [12, 48, 34, 72, 56]
>>> mylist.remove(34)
>>> mylist.insert(2,2)
>>> mylist.sort()
>>> mylist.reverse()
>>> mylist.append(mylist.count(2))
>>> mylist
```

## 4.1.4 LIST LOOP
1.	Write a function to find the factorial of ‘n’?
2.	Find the sum of ‘n’ terms of the series
f = 0! + 1! + 2! + … +  n!  		(n >= 0)
3.	Find whether ‘n’ is the factorial number


## 4.1.5 MUTABILITY
1. What is the output?
```python
>>> a = 72
>>> mylist = [a]
>>> before = id(mylist)
>>> mylist[0] = 34
>>> after = id(mylist)
>>> before == after
```
2. What is the output?
``` python
>>> a = 72
>>> before = id(a)
>>> a = 34
>>> after = id(a)
>>> before == after
```
3. What is the output
```python
>>> a = 72
>>> mylist = [[a]*2]
>>> a = 34
>>> mylist += [[a]*3]
>>> before = id(mylist[1])
>>> mylist[1][2] = 45 
>>> after = id(mylist[1])
>>> before == after
```
## 4.1.6 ALIASING

1. What is the output?
```python
>>> a = [12,'python',True]
>>> b = a
>>> b[2] = False
>>> id(a) == id(b)
```
## 4.1.7 CLONING LISTS
1. Modify the program to get the desired output
```python
>>> old_stock = [['item1',23],['item2',34],['item3',45]]
>>> new_stock = old_stock.copy()
# Add 10 to each item
>>> for i in range(3):
        new_stock[i][1] += 10
# old_stock should not be changed
