Practice of binding attributes and methods in a class. also giving this class multiple states(attributes) and hiding them ([[Abstraction]])

By Default all properties of class is Public, can be accessed with `.` operator
```run-python
class Home:
	def __init__(self):
		self.room=3
obj=Home()

#accessing self.room with "."
obj.room=10
print(obj.room)
```

We can also define Private attributes in python `__` prefix
Private class provide encapsulation. nothing outside class can access a private attribute

```run-python
class Home:
	def __init__(self):
		self.__room=3
		
	def remove(self):
		self.__room-=1
		
obj=Home()
print((obj.__room))
```
