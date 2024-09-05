- When a function takes another function(s) as input.
- it is a higher order function([[First class Functions]])

```run-python
def multiply(x, y):
    return x * y

def add(x, y):
    return x + y

# self_math is a higher order function
# input: a function that takes two arguments and returns a value
# output: a new function that takes one argument and returns a value
def self_math(math_func):
    def inner_func(x):
        return math_func(x, x)
    return inner_func

square_func = self_math(multiply)
double_func = self_math(add)

print(square_func(5))
# prints 25

print(double_func(5))
# prints 10
```

its like decorating a function ( we will see [[Decorators]]) or encapsulating bunch of function within one function.

- 90% function transformation is used for closure function 
- ##### **[[Closure]]** Functions
- another type is [[Currying]] functions