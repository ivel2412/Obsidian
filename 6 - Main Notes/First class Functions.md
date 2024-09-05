Also Known as Higher order function

- in Python the function are values just like string or list
* these functions ca be assigned to a variable
* functions can be added to another function
* Anonymous Functions have no name in python they are known as

Where function are treated as a Values like a object or a variable

We are gonna use [[Python]] as an Example

**First-Class**
```run-python

# Assinging function as a variable

def add(a,b):
	return a+b
a=add
print(a(1,2))
```

**Higher-Order**
```run-python

# Passing a Function in another Function

def square(x):
	return x*x

def my_map(func,arg_list):
	result=[]
	for i in arg_list:
		result.append(func(i))
	return result

ls=[1,2,3,4,5]
output=my_map(square,ls)
print(output)
```


#### Examples
#####  **Map**

In Python, the built-in [map](https://docs.python.org/3/library/functions.html#map) function takes a function and an [[Iterable]](in this case a list) as inputs. It returns an iterator that applies the function to every item, yielding the results.

```run-python
# Map takes a list of inputs and passes it through the given function and outputs a Generator

def square(x):
	return x*x
	
ls = [1,2,3,4,5]
out = map(square,ls)
print(list(out))

```


#### **Filter**

The built-in [filter](https://docs.python.org/3/library/functions.html#filter) function takes a function and an iterable (in this case a list) and returns a _new_ iterable that only contains elements from the original iterable where the result of the function on that item returned `True`.

## Extra info
- [[Function Transformation]] is a type of Higher order function