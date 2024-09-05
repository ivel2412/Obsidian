- Functions that have side effects
- that read or right file (I/O or Std.in Std.out)
- doesn't return something as output
- Ex. `print()` a impure function

```run-python
#Impure Function
def read_file(path):
	file= open(path,"w").read()

```