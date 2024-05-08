## lab04

### list
```python
"""
listX = [digit1, digit2, ..., digitn]
lenth = len(listX)

listX + listY = [digitx1, ..., digity1, ...]
listX * 2 = [digit1, ..., digit1, ...]

pairX = [[digit11, digit12], [digit21, digit22]]
pair[0] = [digit11, digit12]
pair[0][0] = digit11
"""
```
Like C++, the index begins at 0.  
```python
"""
>>> digits = [1]
>>> 1 in digits
>>> True
"""
```

### for statement
for <name> in <expression>: 
    <suite>

### range
range\[x, y\]: x, x + 1, x + 2, ..., y - 1
range\[x\]: 0, 1, ..., x - 1

### list comprehensions
[\<map exp> for <name> in <iter exp> if <filter exp>\]
or [\<map exp> for <name> in <iter exp>\]
(These are lists)
For instance,
```python
digits = [1, 2, 3, 4]
DoubleEvenDigits = [i * 2 for i in digits if i % 2 == 0]
DoubleEvenDigits = [4, 8]
```
