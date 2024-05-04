## lab02

### lambda expression
```python
square = lambda x: x * x
```
``lambda x: x * x`` is an expression. The first x is the argument, and ``x * x``evaluates to the return value.  

### currying
Currying is a technique that transforms multiple-argument functions into single-argument functions.  
For instance,  
```python
def f(x, y):
  return x + y
```
can be transformed into
```python
def f(x):
  return lambda argument y: x + y
```

### problems encountered in Q5
- Pay attention to the difference.
  ```python
  x = fun()
  x = fun
  ```
- When the default argument (or sth alike) need to be change, implement another function.
  ```python
  print(sofar)
    def up():
        return both_paths(sofar + "U")
    def down():
        return both_paths(sofar + "D")
    return up, down
  ```
  
