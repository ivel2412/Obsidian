Decorators are syntactic sugar for for higher order functions
denoted by `@`
```run-python
def vowel_counter(func_to_decorate):
    vowel_count = 0
    def wrapper(doc):
        nonlocal vowel_count
        vowels = "aeiou"
        for char in doc:
            if char in vowels:
                vowel_count += 1
        print(f"Vowel count: {vowel_count}")
        return func_to_decorate(doc)
    return wrapper

@vowel_counter
def process_doc(doc):
    print(f"Document: {doc}")

process_doc("What")
# Vowel count: 1
# Document: What

process_doc("a wonderful")
# Vowel count: 5
# Document: a wonderful

process_doc("world")
# Vowel count: 6
# Document: world
```

its just decoration

### With Decorators
```python

@vowel_counter
def process_doc(doc):
    print(f"Document: {doc}")

process_doc("Something wicked this way comes")
```

### Without Decorators
```python
def process(doc):
    print(f"Document: {doc}")

process_doc = vowel_counter(process)
process_doc("Something wicked this way comes")
```


### [[Cache-Decorator]]

