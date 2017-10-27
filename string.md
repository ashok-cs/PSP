# String

```python
>>> a = 'hello'
```

## Immutable
```python
>>> a[2] = 'x'
Traceback (most recent call last):
  File "<pyshell#15>", line 1, in <module>
    a[2] = 'x'
TypeError: 'str' object does not support item assignment
```

## Re-assign
```
>>> a = a + ' world'
```

### Paragraph
```
>>> pangrams = '''
The quick brown fox jumps over the lazy dog.
Pack my box with five dozen liquor jugs.
Amazingly few discotheques provide jukeboxes.
Sphinx of black quartz, judge my vow.
The quick onyx goblin jumps over the lazy dwarf
'''
```

# String methods
### count()
```
>>> pangrams.count('jumps')
2
```
### split()
```python
>>> words = pangrams.split()
['The', 'quick', 'brown', 'fox', 'jumps', 'over', 'the', 'lazy', 'dog.', 'Pack', 'my', 'box', 'with', 'five', 'dozen', 'liquor', 'jugs.', 'Amazingly', 'few', 'discotheques', 'provide', 'jukeboxes.', 'Sphinx', 'of', 'black', 'quartz,', 'judge', 'my', 'vow.', 'The', 'quick', 'onyx', 'goblin', 'jumps', 'over', 'the', 'lazy', 'dwarf']
>>> pangrams.split('\n')
['', 'The quick brown fox jumps over the lazy dog.', 'Pack my box with five dozen liquor jugs.', 'Amazingly few discotheques provide jukeboxes.', 'Sphinx of black quartz, judge my vow.', 'The quick onyx goblin jumps over the lazy dwarf', '']
>>> pangrams.split('jumps')
>>> pangrams.split('jumps')
['\nThe quick brown fox ', ' over the lazy dog.\nPack my box with five dozen liquor jugs.\nAmazingly few discotheques provide jukeboxes.\nSphinx of black quartz, judge my vow.\nThe quick onyx goblin ', ' over the lazy dwarf\n']
```
# Problem 1

Write a python program that accepts the string and calculate the number of digits and letters

Given string:  "python 3.2"

Expected output:

- Number of letters: 6
- Number of digits: 2

```python
text = "Python 3.2"
letters = 0
digits = 0
for c in text:
    if c.isnumeric():
        digits += 1
    if c.isalpha():
        letters += 1
print("Number of letters:", letters)
print("Number of digits:", digits)
```
