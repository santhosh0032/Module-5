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
```
class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def getName(self):
        return self.name

    def getAge(self):
        return self.age

class Employee(Details):
    def __init__(self, name, age, employee_id, department):
        super().__init__(name, age)
        self.employee_id = employee_id
        self.department = department

    def getEmployeeDetails(self):
        print(f"Employee ID: {self.employee_id}, Department: {self.department}")

class Patient(Details):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)
        self.patient_id = patient_id
        self.disease = disease

    def getPatientDetails(self):
        print(f"Patient ID: {self.patient_id}, Disease: {self.disease}")

e_name = input()
e_age = int(input())
e_id = input()
e_dept = input()

p_name = input()
p_age = int(input())
p_id = input()
p_disease = input()

emp = Employee(e_name, e_age, e_id, e_dept)
pat = Patient(p_name, p_age, p_id, p_disease)

print(f"Name: {emp.getName()}, Age: {emp.getAge()}")
emp.getEmployeeDetails()

print(f"Name: {pat.getName()}, Age: {pat.getAge()}")
pat.getPatientDetails()
```
## Sample Output
<img width="841" height="702" alt="image" src="https://github.com/user-attachments/assets/4790d53a-7f19-454b-a839-e8c6dd8138e8" />

## Result
Thus, The Python program that uses Hierarchical Inheritance to input and display Employee and Patient details was executed successfully.

