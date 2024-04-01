## homework02: higher-order functions （高阶函数）

Higher-order functions in python are functions which use functions as its parameters or return value.

### functions as parameters
```python
def higher-order-fun(n, term):
    return term(term(n))
# this is a higher-order function, in which a function is used as a parameter.
```

### functions as return values
Functions defined within other function bodies are bound to names in a local frame.
```python
def make_adder(n):
    def adder(k):
        return k + n
    return adder
# this is a higher-order function, in which a function is used as a return value.
# adder can not be assess directly outside of make_adder.
```

### choosing names
Suitable names matter a lot for composition.  Names should convey the meaning or purpose of the values to which they are bound.  
The type of value bound to the name is best documented in a function's docstring.  

Reasons to add a new name:  
- repeated compound expressions
- meaningful parts of complex expressions

Choosing name length:  
- Names can be long if they help document your code.
- Names can be short if they represent generic quantities: counts, arbitrary functions, arguments to mathematical operations, etc.
