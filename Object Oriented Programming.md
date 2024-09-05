
Classes are special type of values 
Object is an instance of class
```run-python
class Wall:
    thickness=10
    def __init__(self):
        self.health = 5

    def take_damage(self, damage):
        self.health -= damage


soldier_one = Wall()
soldier_two = Wall()

soldier_one.take_damage(3)
soldier_two.take_damage(4)

print(f"Health of soldier one : {soldier_one.health}")
print(f"Health of soldier two : {soldier_two.health}")
```
here `Wall` is a class and `soldier_one` and `soldier_two` are both object of `Wall` class

### Methods
Ex. take_damage 
Similar to functions
usually don't return anything because they are used to mutate the object property
And when they do for output or input , they are called Getters and Setters
methods always take the first parameter as their own object(self)

### Constructor
A method named `__init__`
it doesn't take any input other than `self`
it is used to initialize `Instance Vriables`
here self.health is initialized

### Class vs Instance variable
Class variables are shared among all objects
Instance variable is only accessed by the given object
here `thickness` is `Class Variable`
and `self.health` is `Instance Variable`

## OOP Concepts

* [[Encapsulation]]
* [[Abstraction]]
* [[Inheritance]]
* [[Polymorphism]]
