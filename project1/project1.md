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

### local variable \[var\] reference before assignment
The following program will cause such error. 
```python
def announce(score0, score1, last_score = 0, running_high = 0):
    if score0 - last_score > running_high:
        running_high = score0 - last_score
        print(running_high, "point(s)! That's the biggest gain yet for Player 0")
    last_score = score0
    annonuce = announce(score0, score1, last_score = score0,  running_high = running_high)
    return announce
return announce
```
As the hint says, "**This happens because in Python, you aren't normally allowed to modify variables defined in parent frames. Instead of reassigning \[var\], the interpreter thinks you're trying to define a new variable within the current frame.** "  
The following program can fix the problem.  
```python
def announce(score0, score1, last_score = 0, running_high = 0):
    if score0 - last_score > running_high:
        running_high = score0 - last_score
        print(running_high, "point(s)! That's the biggest gain yet for Player 0")
    last_score = score0
    def new_announce(score0, score1):
        return announce(score0, score1, last_score = score0, running_high = running_high)
    return new_announce
return announce
```
Beside, passing new values as arguments can also fix the problem.
