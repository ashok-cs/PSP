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
