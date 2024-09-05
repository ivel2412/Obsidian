`+` in python is used for summation and also for concatenation depending on the classes of operands
```run-python
print(3 + 4)
# prints "7"

print("Choco" + "late")
# prints "Chocolate"

```

## Use case ->
Built-in classes have support for operators like `add`, `sub`, `div`,...etc
we don't have this support of custom classes
```run-python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

p1 = Point(4, 5)
p2 = Point(2, 3)
p3 = p1 + p2
##unsupported operand type(s) for +: 'Point' and 'Point'
```

We can add this support by creating a  `__self__(self,other)` method

```run-python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, point):
        x = self.x + point.x
        y = self.y + point.y
        return Point(x, y)

p1 = Point(4, 5)
p2 = Point(2, 3)
p3 = p1 + p2

print(f"({p3.x},{p3.y})")
# p3 is (6, 8)
```

here is a list of similar methods

<table>
    <thead>
        <tr>
            <th>Operation</th>
            <th>Operator</th>
            <th>Method</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Addition</td>
            <td>+</td>
            <td>__add__</td>
        </tr>
        <tr>
            <td>Subtraction</td>
            <td>-</td>
            <td>__sub__</td>
        </tr>
        <tr>
            <td>Multiplication</td>
            <td>*</td>
            <td>__mul__</td>
        </tr>
        <tr>
            <td>Power</td>
            <td>**</td>
            <td>__pow__</td>
        </tr>
        <tr>
            <td>Division</td>
            <td>/</td>
            <td>__truediv__</td>
        </tr>
        <tr>
            <td>Floor Division</td>
            <td>//</td>
            <td>__floordiv__</td>
        </tr>
        <tr>
            <td>Remainder (modulo)</td>
            <td>%</td>
            <td>__mod__</td>
        </tr>
        <tr>
            <td>Bitwise Left Shift</td>
            <td>&lt;&lt;</td>
            <td>__lshift__</td>
        </tr>
        <tr>
            <td>Bitwise Right Shift</td>
            <td>&gt;&gt;</td>
            <td>__rshift__</td>
        </tr>
        <tr>
            <td>Bitwise AND</td>
            <td>&amp;</td>
            <td>__and__</td>
        </tr>
        <tr>
            <td>Bitwise OR</td>
            <td>|</td>
            <td>__or__</td>
        </tr>
        <tr>
            <td>Bitwise XOR</td>
            <td>^</td>
            <td>__xor__</td>
        </tr>
        <tr>
            <td>Bitwise NOT</td>
            <td>~</td>
            <td>__invert__</td>
        </tr>
    </tbody>
</table>
