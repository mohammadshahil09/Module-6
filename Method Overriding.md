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

## OUTPUT
<img width="521" height="332" alt="504009421-99d946dd-648d-4cd6-b03a-63f37474bbb6" src="https://github.com/user-attachments/assets/6aef45b8-a137-4cdd-84dd-fad3b3dfc0c0" />

## RESULT
The given program is successfully executed
