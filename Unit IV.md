# UNIT IV: COMPOUND DATA
## LISTS, TUPLES, DICTIONARIES

Lists, list operations, list slices, list methods, list loop, mutability, aliasing, cloning lists, list parameters; Tuples, tuple assignment, tuple as return value; Dictionaries: operations and methods; advanced list processing - list comprehension, Illustrative programs: selection sort, insertion sort, merge sort, quick sort.

### Objective:
To use Python data structures –- lists, tuples, dictionaries

### Outcome:
Represent compound data using Python  lists, tuples, dictionaries

# 4 COMPOUND DATA

Primitive data types are basic data types such as int, bool and float. Compound data is any data type which is constructed using primitive data types and other compound data types. Python offers different compound data types (sequences) such as lists, tuples and dictionaries.

# 4.1 LISTS

List is the collection (bag) of objects. We extensively use list to store and manipulate data in everyday computing.

### Examples
1.	List of web pages matching the keyword (google)
2.	List of friends (facebook)
3.	List of products prices (amazon)
4.	List of tasks to do
5.	List of grocery items to be purchased
6.	List of students enrolled in a class

The objects in the list can be of same type or of different types.

### Example

```python
>>>grocery = ['bread', 'butter', 'milk']
>>>absentees = [3, 14, 24, 35, 37, 41]
>>>movie_review = ['enthiran', {'5-rating':344, '4-rating': 28, '3-rating':0}]
>>>my_friends = ['akil', 'kapil', 'dhoni']
>>>my_favorite_menu = ['idli','dhosa','pongal']
```
Lists may be constructed in several ways:
- Using a pair of square brackets to denote the empty list: []
- Using square brackets, separating items with commas: [a], [a, b, c]
- Using a list comprehension: [x for x in iterable]
- Using the type constructor: list() or list(iterable)

## 4.1.1 LIST OPERATIONS
### repeat (*)
```python
>>> mylist = [1, True, 'python']
>>> mylist * 2
[1, True, 'python',1, True, 'python']
```

### concatenate (+)
```python
>>>part1 = ['python','is']
>>>part2 = ['all', 'purpose', 'language']
>>>part1 + part2
['python','is','all', 'purpose', 'language']
```
### empty list
```python
>>>a = []
>>>not a
True
```

### index
```python
>>>mylist = [12, 48, 12, 72, 34, 21]
>>>mylist[1]
48
>>>mylist[0]
12
```

Exercises:
1.	What is the output?
```python
>>> a = 10
>>> mylist = [a]*5
>>> mylist[3]
```
2.	What is the output?
```python
>>> mylist1 = ['In', 'python']
>>> mylist2 = ['explicit','is','better']
>>> mylist = mylist1 + mylist2
>>> mylist += ['than','implicit']
>>> mylist
```

```python
>>> mylist = [12, 48, 12, 72, 34, 21]
>>> mylist
[12, 48, 12, 72, 34, 21]
>>> mylist[2]
12
>>> mylist[-2]
34
>>> mylist[3]
72
```