```python
order = {
                'A': 1, '2': 2, '3': 3, '4': 4,
                '5': 5, '6': 6, '7': 7, '8': 8,
                '9': 9, '10': 10,
                'J': 11, 'Q': 12, 'K': 13
             }


def insertCard(deck, newCard):
    try:
        for card in deck:
            if order[card] > order[newCard]:                
                index = deck.index(card)
                deck.insert(index, newCard)
                break        
        return deck        
    except KeyError:
        print('Invalid card:', card)       
    
    
deck = ['2', '5', '8', '10', 'J', 'K']
insertCard(deck, '9')
print(deck)
```
