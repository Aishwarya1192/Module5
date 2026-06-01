# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
Add code here
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def display(self):
        print("Name:", self.name)
        print("Age:", self.age)


# Employee inherits from Person
class Employee(Person):
    def __init__(self, name, age, emp_id, department):
        super().__init__(name, age)
        self.emp_id = emp_id
        self.department = department

    def display(self):
        super().display()
        print("Employee ID:", self.emp_id)
        print("Department:", self.department)


# Patient inherits from Person
class Patient(Person):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)
        self.patient_id = patient_id
        self.disease = disease

    def display(self):
        super().display()
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)


# Input Employee details
print("Enter Employee details:")
emp_name = input("Name: ")
emp_age = int(input("Age: "))
emp_id = input("Employee ID: ")
emp_dept = input("Department: ")

employee = Employee(emp_name, emp_age, emp_id, emp_dept)

print("\nEnter Patient details:")
pat_name = input("Name: ")
pat_age = int(input("Age: "))
pat_id = input("Patient ID: ")
pat_disease = input("Disease: ")

patient = Patient(pat_name, pat_age, pat_id, pat_disease)

print("\n--- Employee Details ---")
employee.display()

print("\n--- Patient Details ---")
patient.display()

## Sample Output
Enter Employee details:
Name: John
Age: 30
Employee ID: E101
Department: HR

Enter Patient details:
Name: Alice
Age: 25
Patient ID: P202
Disease: Flu

--- Employee Details ---
Name: John
Age: 30
Employee ID: E101
Department: HR

--- Patient Details ---
Name: Alice
Age: 25
Patient ID: P202
Disease: Flu
##Result
Hence the output is verified

