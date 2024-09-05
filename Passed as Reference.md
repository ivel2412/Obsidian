The function has access to the original value of the variable and can change it
it is Mutable and the function is can be called a [[Impure functions]]

```run-python
# here inp is a refernece to ls

ls=[1,2,3,4,5]
def pop_last(inp):
	inp.pop(-1)
	return inp
	
pop_last(ls)
print(ls)
```
`list.sort()` method is an example of this
we can make [[Pure functions]] for reference with `.copy()` method

```run-python
ls=[1,2,3,4,5] 
def pop_last(inp):
	inp.pop(-1)
	return inp
# .copy method creates a copy of a reference
out=pop_last(ls.copy())
print(ls)
print(out)
```
