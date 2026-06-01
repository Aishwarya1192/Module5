# Destructor in Python

This project demonstrates how to implement a **destructor** in Python using a simple class.

## 🚀 Overview

The program defines a class `Demo` with:

- A **constructor** `__init__` that initializes an instance variable and prints a message.
- A **destructor** `__del__` that prints a message when the object is destroyed.

## 🧠 Algorithm

1. Define a class named `Demo`.
2. Inside the class, define the `__init__` method:
   - Initialize an instance variable `status` with the value `"Alive"`.
   - Print the value of `status`.
3. Define the `__del__` method:
   - Print a message indicating the object is being destroyed.
4. Outside the class:
   - Create an instance of the `Demo` class.
   - Delete the object using the `del` keyword.
## Program
Add code Here
class Demo:
    def __init__(self, value):
        self.value = value
        print(f"Constructor called: Object created with value = {self.value}")

    def __del__(self):
        print(f"Destructor called: Object with value = {self.value} is being destroyed")

# Create an object
d1 = Demo(100)

# Explicitly delete the object
del d1

print("End of program")


## 🧪 Output
Constructor called: Object created with value = 100
Destructor called: Object with value = 100 is being destroyed
End of program

## Result
Hence the output is verified
