# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` , `Circle`,`Square`and `Triangle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `type_shape()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `type_shape()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `type_shape()` to compute the circle area.
  
5.**Create Subclass `Square`**:
   - Set default value for `side`.
   - Override `type_shape()` to compute the square area.

6.**Create Subclass `Triangle`**:
   - Set default value for `base` and `height`.
   - Override `type_shape()` to compute the triangle area.

7. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` , `Circle`,`Square` and `Triangle`.
   - Call their `type_shape()` methods.

---

## 💻 Program
```
from abc import ABC, abstractmethod

# Abstract base class
class type_shape(ABC):
    @abstractmethod
    def area(self):
        pass

# Rectangle subclass
class Rectangle(type_shape):
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

# Square subclass
class Square(type_shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side * self.side

# Circle subclass using π = 3.14
class Circle(type_shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return round(3.14 * self.radius ** 2, 2)  # Use 3.14 for π to match the expected output

# Triangle subclass
class Triangle(type_shape):
    def __init__(self, base, height):
        self.base = base
        self.height = height

    def area(self):
        return 0.5 * self.base * self.height

# Creating instances
rect = Rectangle(6, 4)
circle = Circle(7)
square = Square(4)
triangle = Triangle(4, 5)

# Output results
print("Area of a rectangle:", rect.area())
print("Area of a circle:", circle.area())
print("Area of a square:", square.area())
print("Area of a triangle:", triangle.area())
```
## Output
![image](https://github.com/user-attachments/assets/9660a622-477a-49a5-9772-a55d6fee4fd4)

## Result
Thus the program of abstract class has been executed successfully.


# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
```
class Rectangle:
    def __init__(self):
        self._length=5
        self._breath=3
    def values(self):
        print(self._length)
        print(self._breath)
        
rect=Rectangle()
rect.values()
```
## Output

![image](https://github.com/user-attachments/assets/514cef94-2836-4b3e-a1c3-3854f08f4cd4)

## Result
Thus the program to implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth` has been executed successfully.


# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```
class Fish:
    def fish(self):
        print("fish")

class Shark:
    def shark(self):
        print("shark")


obj_goldfish=Fish()
obj_hammerhead=Shark()
obj_goldfish.fish()
obj_hammerhead.shark()
```

## OUTPUT
![image](https://github.com/user-attachments/assets/6a9ce93f-4b41-4f53-b320-9224bc66c860)

## RESULT
Thus the program  that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method ha been executed successfully.


# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
```
class Marks(object):
    def __init__(self, x):
        self.x = x
    def __lt__(self, other):
        return self.x> other

obj1 = Marks(20)
obj2 = Marks(10)

print(obj1 < obj2)
```

## Output
![image](https://github.com/user-attachments/assets/a4dd56a3-fc32-4f1b-8704-c0f8f8aa9872)

## Result
Thus the program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class has been executed successfully.


# # 🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.
   - 
---

## 💻 Program
```
class Beans(): 
     def type(self): 
       print("Vegetable") 
     def color(self):
       print("Green") 
class Mango(): 
     def type(self): 
       print("Fruit") 
     def color(self): 
       print("Yellow")      

obj_beans = Beans() 
obj_mango = Mango() 
for i in (obj_beans,obj_mango):
    i.type()
    i.color()
```
## Output
![image](https://github.com/user-attachments/assets/33aefb21-3e9b-4394-bfaa-2a3df815e49a)

## Result
Thus the python program to Polymorphism with Classes has been executed successfully.
