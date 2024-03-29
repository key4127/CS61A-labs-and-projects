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
- The global frame alone, or  
- A local frame, followed by the global frame.  
