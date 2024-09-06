In Python `*args` and `**kwargs` allow function to accept variable number of agruments

```python
def print_arguments(*args, **kwargs):
    print(f"Positional arguments: {args}")
    print(f"Keyword arguments: {kwargs}")

print_arguments("hello", "world", a=1, b=2)
# Positional arguments: ('hello', 'world')
# Keyword arguments: {'a': 1, 'b': 2}
```

`*args` -> n number of Positional Arguments
`**kwargs` -> n number of keyword arguments

### Positional arguments
```python
def sub(a, b):
    return a - b

# a=3, b=2
res = sub(3, 2)
# res = 1
```

### Keyword arguments

[Keyword arguments](https://docs.python.org/3/tutorial/controlflow.html#keyword-arguments) are passed in by name. _Order does not matter_. Like this:

```python
def sub(a, b):
    return a - b

res = sub(b=3, a=2)
# res = -1
res = sub(a=3, b=2)
# res = 1
```

#### A note on ordering
Any positional arguments _must come before_ keyword arguments. This will _not_ work:
```python
sub(b=3, 2)
#won't work
```
