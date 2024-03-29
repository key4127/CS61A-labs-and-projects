## homework1: variables, functions and control

### assignment statements
1.  Evaluate all expressions to the right of = from left to right.
2.  Bind all names to the left of = to those resulting values in the current frame.

### defining functions
Assignment is a simple means of abstraction: binds names to values.  
Function definition is a more powerful means of abstraction: binds names to expressions.  
The bind can be assigned to new variables.  
```python
def origin_function():
    print("Hello")
new_function = origin_function
new_function()
# the new function can be used in the same way as the origin function
```

### environments
Every expression is evaluated in the context of an environment.  
So far, the current environment is either:  
- The global frame alone.  
- A local frame, followed by the global frame.

**An environment is a sequence of frames.  
A name evaluates to the value bound to that name in the earliest frame of the current environment in which that name is found.**

### none
The special value **None** represents nothing in Python. a function that does not explicitly return a value will return **None**.    
```python
def return_nothing(x):
    x += 1
```
```python
>>> x = 5
>>> y = return_nothing(x)
>>> y + 1
TypeError: unsupported operand type(s) for +: 'NoneType' and 'int'
```
As the name y has been bound to the value **None**, it produces an error.  

### pure funcions and non-pure functions
Pure functions only return values. To be excatly, pure functions always give the same output for the same input, and do not have any side effect. They do not modify the state of the external environment.  
```python
def pow(x, y)
    return x ** y
# this is a pure function
```
Non-pure functions may change the state of the program or have other side effects. For example, the function may alter **global variables**, modify **input parameters**, perform **I/O operations**, etc.  
```python
def print_hello():
    print("hello")
# python will display the output "hello". this is a non-pure function.
```
```python
count = 0
def increment()
    global count  # global is used to reference variables defined in the global frame.
    count += 1
# the function changes the global variable count. this is also a non_pure function.
```

### conditional statements
```python
def absolute_value(x):
    if x < 0:
        return -x
    elif x == 0:
        return 0
    else:
        return x
```
Unlike C++, the scope of a variable is not limited to the block of code where it's defined. If a variable was defined inside a loop or a conditional statement, the variable will still exist even after the completion of the loop or the conditional statement.  

### while statements
```python
i, total = 0, 0
while i < 3:
    i = i + 1
    total = total + i
```

### designing functions
- Give each function exactly one job, but make it apply to many related situations.
- Implement a process just once, but execute it many times.

### logical operators
|C++|&&|\|\||!|
|:-:|:-:|:-:|:-:|
|python|and|or|not|

To evaluate the expression related to **and**:  
- Evaluate the subexpression <left>.
- If the result is a false value v, then the expression evaluates to v.
- Otherwise, the expression evaluates to the value of the subexpression <right>.

To evaluate the expression related to **or**:  
-  Evaluate the subexpression <left>.
-  If the result is a true value v, then the expression evaluates to v.
-  Otherwise, the expression evaluates to the value of the subexpression <right>.

### conditional expressions
```python
consequent if predicate else alternative
```
Similar to the ternary operator in C++. The difference is that it is the second statement that is the conditional statement, not the first.  

The evaluation rule is:  
- Evaluate the <predicate> expression.  
- If it's a true value, the value of the whole expression is the value of the <consequent>.
- Otherwise, the value of the whole expression is the value of the <alternative>.  
  
