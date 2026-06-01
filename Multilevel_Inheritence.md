# Multilevel Inheritance Example in Python

This Python project demonstrates the concept of **Multilevel Inheritance** to collect and display the **name**, **age**, and **location** of a person.

## 🎯 Aim

To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.

## 🧠 Algorithm

1. **Parent Class**  
   - `__init__(name)` initializes the `name` attribute.  
   - `getName()` returns the `name`.

2. **Child Class (inherits Parent)**  
   - `__init__(name, age)` initializes `name` using `super()` and adds `age`.  
   - `getAge()` returns the `age`.

3. **Grandchild Class (inherits Child)**  
   - `__init__(name, age, location)` initializes `name` and `age` using `super()` and adds `location`.  
   - `getLocation()` returns the `location`.

4. **Input & Output**  
   - Take user input for name, age, and location.  
   - Create an instance of `Grandchild`.  
   - Print all details using class methods.

## Program
Add code here
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def display(self):
        print("Name:", self.name)
        print("Age:", self.age)


# Child class inheriting from Person
class Details(Person):
    def __init__(self, name, age, location):
        super().__init__(name, age)
        self.location = location

    def display(self):
        super().display()
        print("Location:", self.location)


# Grandchild class inheriting from Details
class Show(Details):
    def __init__(self, name, age, location):
        super().__init__(name, age, location)

    def display(self):
        print("\n--- Person Details ---")
        super().display()


# Input from user
name = input("Enter name: ")
age = int(input("Enter age: "))
location = input("Enter location: ")

# Create object of Show class
person = Show(name, age, location)

# Display details
person.display()


## Sample Output
Enter name: Aishwarya
Enter age: 19
Enter location: Chennai

--- Person Details ---
Name: Aishwarya
Age: 19
Location: Chennai
##Result
Hence the output is verified

