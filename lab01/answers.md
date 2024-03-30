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

```python
n = 3
while n >= 0:
    n -= 1
    print(n)

2
1
0
-1
```

```python
positive = 28
while positive:
    print("positive?")
    positive -= 3

Infinite Loop
```
```python
positive = -9
negative = -12
while negative:
    if positive:
        print(negative)
    positive += 3
    negative += 3

-12
-9
-6
```
### Q2
```python
>>> True and 13
13
>>> False or 0
0
>>> not 10
False
>>> not None
True
```

```python
>>> True and 1 / 0 and False
Error
>>> True or 1 / 0 or False
True
>>> True and 0
0
>>> False or 1
1
>>> 1 and 3 and 6 and 10 and 15
15
>>> -1 and 1 > 0
True
>>> 0 or False or 2 or 1 / 0
2
```

```python
>>> not 0
True
>>> (1 + 1) and 1
1
>>> 1/0 or True
Error
>>> (True or False) and False
False
```

### Q3
```python
```

### Q6
```python
```
