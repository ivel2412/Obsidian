Closer is a type of higher order function that keeps the state of a function
similar to class and its object 

- **`a closure is just a function that **keeps track of some values** from the place where it was _defined_, no matter where it is executed later on.`**

```run-python
def concatter():
	doc = ""
	def doc_builder(word):
		# "nonlocal" tells Python to use the 'doc'
		# variable from the enclosing scope
		nonlocal doc
		doc += word + " "
		return doc
	return doc_builder

# save the returned 'doc_builder' function
# to the new function 'harry_potter_aggregator'
harry_potter_aggregator = concatter()
harry_potter_aggregator("Mr.")
harry_potter_aggregator("and")
harry_potter_aggregator("Mrs.")
harry_potter_aggregator("Dursley")
harry_potter_aggregator("of")
harry_potter_aggregator("number")
harry_potter_aggregator("four,")
harry_potter_aggregator("Privet")

print(harry_potter_aggregator("Drive"))
# Mr. and Mrs. Dursley of number four, Privet Drive
```

here `concatter` is a closer function that keeps `doc` variable in state for given instance `harry_potter_aggregator` 

#### **`nonlocal`** 
- `nonlocal` is python specific keyword that tells function to use higher scope than local
- in this case use `doc` from `concatter`
- use it only for immutable types because mutable types are accessed as reference [[Passed as Reference]]


better example 
```python
def css_styles(initial_styles):
    dic = initial_styles.copy()

    def add_style(selector, property, value):
        if selector in dic.keys():
            if property in dic[selector].keys():
                if dic[selector][property] is dict:
                    dic[selector][property].add(value)
                else:
                    dic[selector][property] = value
            else:
                dic[selector][property] = value
        else:
            dic[selector] = {property: value}
        return dic

    return add_style

```