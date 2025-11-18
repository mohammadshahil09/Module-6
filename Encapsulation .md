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
# Step 1 & 2: Define the Class with private attributes and initialize them
class Rectangle:
    def __init__(self, length=5, breadth=3):
        self.__length = length      # Private attribute
        self.__breadth = breadth    # Private attribute
        # Step 3: Print values from within the class
        print(f"Rectangle created with length = {self.__length} and breadth = {self.__breadth}")

# Step 4: Instantiate the object
rect = Rectangle()

## Output
<img width="348" height="242" alt="504009334-7e805a50-0c8e-4df5-be1d-e46f36078dea" src="https://github.com/user-attachments/assets/878cb5f5-fbc5-4682-95d6-1182024be07b" />

## Result
The given program is successfully executed
