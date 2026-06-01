# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `Subtraction(a, b)` method to return the difference of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `Subtraction`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
Add code here
class Addition:
    def add(self, a, b):
        return a + b


class Subtraction:
    def subtract(self, a, b):
        return a - b


class Division:
    def divide(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Error: Division by zero"


# Multiple Inheritance: Arithmetic inherits from all three
class Arithmetic(Addition, Subtraction, Division):
    def display(self, a, b):
        print("Addition:", self.add(a, b))
        print("Subtraction:", self.subtract(a, b))
        print("Division:", self.divide(a, b))


# Input from user
x = int(input("Enter first number: "))
y = int(input("Enter second number: "))

obj = Arithmetic()
obj.display(x, y)

## Output Example
Enter first number: 20
Enter second number: 5
Addition: 25
Subtraction: 15
Division: 4.0
##Result 
Hence the output is verified

