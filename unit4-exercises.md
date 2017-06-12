# 4.1 LIST
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
```
## 4.1.8 LIST PARAMETERS
1. Write a function `cat_num` which takes a list, say, ```[1,2,3,4,5]``` and modifies to  ```[11,22,33,44,55]``` and returns None.

# 4.2 TUPLES

## 4.2.1 TUPLE ASSIGNMENT
1. What is the output
```python
>>> a,b,c = 10, 00, 000
>>> (a, b, c)*2
>>> a,b,c
```

## 4.2.2 TUPLE AS RETURN VALUE
1. Write the function `quotient_reminder` to return quotient and reminder of ```a/b```
Answer:
``` python
>>>def quotient_reminder(a,b):
        return a // b, a % b
>>>quotient_reminder(13,2)
```

# 4.3 DICTIONARIES
## 4.3.1 OPERATIONS AND METHODS
1. Write the function letters_freq to find the frequency of letters in a string. Return the result as the dictionary.
2. Find the capital for the given country from  the imported dictionary capital
```python
from country import capital
def find_capital(country):
        # your code

```
3. Find the country for the given capital.
```python
from country import capital
def find_country(capital):
        # your code
```
4. Find the countries for the given capitals.
```python
from country import capital
def find_countries(capitals):
        # your code
Example: input = [‘New Delhi’,’Washington DC’]  output = [‘India’,’US’]
```

# 4.4 ADVANCED LIST PROCESSING
## 4.4.1 LIST COMPREHENSION
1. What is the output?
```python
>>> num = [ d**3 for d in range(1,10)]
>>> num
```

2. What is the output?
```python
>>> cols = [1,2]
>>> row = [12, 'medium', 23.25, True]
>>> [ row[col] for col in cols]
```

3. Split the time “7:20 am” and store it in hour and min as integers.(in 24 hour format). Then find the time elapsed and return the value.
Example: 
```start: “7:20 am”, end: “12.30 pm” 	output: 5 hr 10 min```
```python
def elapsed(start,end):
        #your code here
```

# 4.5 ILLUSTRATIVE PROGRAMS
## 4.5.1 SELECTION SORT

1. Assume that `first` number in the list is minimum. Exchange, if first> second
```
Example
input = [12,3,15,7,23]	output = [3,12,15,7,23]
```
2. Assume that `first` element in the list is minimum. Compare it with every other element. Exchange if it is greater.
```
Example:
[12,23,15,7,3]   As 12<23, don’t exchange.
[12,23,15,7,3] As 12<15, don’t exchange.
[12,23,15,7,3] As 12>7, exchange
[7,23,15,12,3] As 7>3, exchange
[3,23,15,12,7] Stop. 
```
3. Now, the first element is the minimum. Now, bring the next minimum value in the list as the second element.
```
Example:
[3,23,15,12,7] As 23>15, exchange
[3,15,23,12,7] As 15>12, exchange
[3,12,23,15,7] As 12>7, exchange
[3,7,23,15,12] stop
```

## 4.5.2 INSERTION SORT
1. Consider the second `element` in the list `num`. Insert  at index 0, if element < first.
hint: use `insert()`
2. Remove `element` if it is inserted.
hint: use `pop()` or `remove`
3. Now `num[0:1]` is in sorted order. Now, consider the third `element` in the list (`num[2]`).
Compare with first two elements. 
Insert at 0, if `element` is less than first.
Insert at 1, if `element` is less than second.
Remove num[2], if it is inserted.


## Implementation
```python
def insertion_sort(num):    
    for i in range(1,len(num)):
        element = num[i]
        inserted = False
        for j in range(i):
            if element < num[j]:
                print(num,"insert",element," at ",j)
                num.insert(j,element)
                inserted = True
                break
        if inserted:            
            num.pop(i+1)                   


#Test
mylist = [12,3,45,72,15]
insertion_sort(mylist)
print(mylist)
```

## 4.5.3 MERGE SORT
1. Consider `left` and `right` lists of size 1. Merge them in a sorted order.
```
Example:
left = [12]  right = [3]
merged = [3,12]
```
2. Now consider the two sorted lists of unspecified size. Merge them in a sorted order.
```
Example:
left = [12,45]  right = [3,17]
merged = [3,12,17,45]
```

3. Divide the list `num` into `left` and `right` halves.
4. Recursively divide, till the partition size is 1
```
Example:
num = [12,3,45,17,15]
left = [12,3]
        left = [12]
        right = [3]
right = [17, 15]
        left = [17]
        right = [15]
```
