## answers to lab01

### Q1
```python
def xk(c, d):
    if c == 4:
        return 6
    elif d >= 4:
        return 6 + 7 + c
    else:
        return 25

>>> xk(10, 10)
23
>>> xk(10, 6)
23
>>> xk(4, 6)
6
>>> xk(0, 0)
25
```

### Q2
```python
def how_big(x):
    if x > 10:
        print('huge')
    elif x > 5:
        return 'big'
    elif x > 0:
        print('small')
    else:
        print("nothin'")

>>> how_big(7)
'big'
>>> how_big(12)
huge
>>> how_big(1)
small
>>> how_big(-1)
nothin'
```

### Q3
```python
```

### Q6
```python
```
