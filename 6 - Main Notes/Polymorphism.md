Poly -> many
Morph -> forms

ex. -> 
```python
class Human:
    def hit_by_fire(self):
        self.health -= 5
        return self.health

class Archer:
    def hit_by_fire(self):
        self.health -= 10
        return self.health
```
here Human and Archer have `hit_by_fire` method that has different purpose depending on the class

### **Concepts of Polymorphism**
[[Operator Overloading]]