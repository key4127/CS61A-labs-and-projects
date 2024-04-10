## project1: the game of hog

### assert
```python
assert expression, 'error message'
```
If the expression is true, the program will continue to execute normally, or the program will throw an **AssertionError** exception and output the error message. 

### randint
```python
from random import randint
randint (x, y)
```
The function randint can produce a random integer between x and y.

### nonlocal
```python
index = len(outcomes) - 1
def dice():
  nonlocal index
  index = (index + 1) % len(outcomes)
  return outcomes[index]
```
The keywords nonlocal is used in a nested function to declare that a variable is not local or global, but is in the outer non-global scope. This means that even if the variable is modified within the inner function, the change will also affect the variable with the same name in the outer scope.
