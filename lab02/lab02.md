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

### environment diagram practice need to complement

### environments for nested definitions
In python, the inner functions can access the value of non-local variables defined in the parent functions, but are not permitted to modify them.
(However, the keyword **nonlocal** enables us to specify a variable not to be local)  

```python
def cycle_first(n):
    def cycle_second(x):
        while n > 3: # n will be considered a local variable
            n -= 3
            x = f3(f2(f1(x)))
        return x
    return cycle_second
```
```python
def cycle_first(n):
    def cycle_second(x):
        times = n
        while times > 3:
            times -= 3
            x = f3(f2(f1(x)))
        return x
    return cycle_second
```
