# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
~~~
# Step 1: Import ABC module
from abc import ABC, abstractmethod
import math

# Step 2: Create Abstract Class Shape
class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass

# Step 3: Create Subclass Rectangle
class Rectangle(Shape):
    def __init__(self, length=5, breadth=3):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        area = self.length * self.breadth
        print(f"Rectangle area: {area}")

# Step 4: Create Subclass Circle
class Circle(Shape):
    def __init__(self, radius=4):
        self.radius = radius

    def calculate_area(self):
        area = math.pi * self.radius ** 2
        print(f"Circle area: {area:.2f}")

# Step 5: Create Objects & Call Methods
rect = Rectangle()
rect.calculate_area()

circ = Circle()
circ.calculate_area()

~~~

## Output:


<img width="726" height="227" alt="image" src="https://github.com/user-attachments/assets/d4a50117-be88-4793-a720-22485c447485" />

## Result
The given program is successfully executed




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
~~~
# Step 1 & 2: Define the Class with private attributes and initialize them
class Rectangle:
    def __init__(self, length=5, breadth=3):
        self.__length = length      # Private attribute
        self.__breadth = breadth    # Private attribute
        # Step 3: Print values from within the class
        print(f"Rectangle created with length = {self.__length} and breadth = {self.__breadth}")

# Step 4: Instantiate the object
rect = Rectangle()

~~~

## Output
<img width="348" height="242" alt="image" src="https://github.com/user-attachments/assets/7e805a50-0c8e-4df5-be1d-e46f36078dea" />

## Result
The given program is successfully executed



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
~~~
# Step 1: Define the Fish class
class Fish:
    def type(self):
        print("fish")

# Step 2: Define the Shark class as a subclass of Fish
class Shark(Fish):
    def type(self):
        print("shark")

# Step 3 & 4: Create instances
obj_goldfish = Fish()
obj_hammerhead = Shark()

# Step 5 & 6: Iterate over both objects and call type()
for obj in (obj_goldfish, obj_hammerhead):
    obj.type()

~~~

## OUTPUT
<img width="521" height="332" alt="image" src="https://github.com/user-attachments/assets/99d946dd-648d-4cd6-b03a-63f37474bbb6" />

## RESULT
The given program is successfully executed




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
~~~
# Step 1: Create Class A
class A:
    def __init__(self, a):
        self.a = a

    # Step 2: Overload the '<' operator
    def __lt__(self, o):
        if self.a < o.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"

# Step 3: Create objects
ob1 = A(10)
ob2 = A(20)

# Step 4: Use '<' operator
print(ob1 < ob2)

~~~

## Output
<img width="907" height="286" alt="image" src="https://github.com/user-attachments/assets/9641fee1-c76f-4e20-97b0-812ec1d67d2a" />

## Result
The given program is successfully executed

## 🐍 Python OOP: Polymorphism with Classes

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

---

## 💻 Program
```python
class Beans:

def type(self):

print("Vegetable")

def color(self):

print("Green") class Mango:

def type(self):

print("Fruit")

def color(self):

print("Yellow")
obj_beans = Beans()

obj_mango = Mango()

obj_beans.type()

obj_beans.color()

obj_mango.type()

obj_mango.color()
```

## Output
![488720303-25d5a198-6e75-4eb0-9825-7c651cd47d90](https://github.com/user-attachments/assets/e7662c67-7fb1-4f8a-bbb4-19d9ddd8fe17)


## Result
Thus, the program To create two specific classes — Beans and Mango. Then, create a generic function that can accept any object and determine its type (Fruit or Vegetable) and color, using polymorphism is excuted and verified.





