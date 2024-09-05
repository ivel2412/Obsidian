Converting Single function with multiple arguments  into multiple function with single arguments

```python
box_volume(3, 4, 5)#normal function

box_volume(3)(4)(5)#curried function
```
Implementation
```run-python
def summ(a):
    def inner(b):
        return a + b
    return inner

out = summ(5)(6)
print(out)
```

- currying is often used to **change a function's signature** to make it conform to a specific shape.
better example
```python
final_volume = box_volume(3)(4)(5)
print(final_volume)
# 60

with_length_3 = box_volume(3)
with_len_3_width_4 = with_length_3(4)
final_volume = with_len_3_width_4(5)
print(final_volume)
# 60

```