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
