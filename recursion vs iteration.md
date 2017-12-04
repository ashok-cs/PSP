```python
from random import randint
def guess():
    myguess = int(input())
    if number > myguess:
        print('You guessed less')
    elif number < myguess:
        print('You guess high')
    else:
        print('Great! You guess right!')
        return True
    return False

    
attempt = 10
number = randint(1,100)
while attempt > 0:
    if guess():
        break
    attempt -= 1
print('Good try! Play again!')
```
