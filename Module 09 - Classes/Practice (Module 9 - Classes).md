# Practice Assignment: Module 9 - Classes

## Overview

This assignment provides an opportunity to apply the concepts covered in this module by writing Python programs using classes, objects, inheritance, and encapsulation.

You will complete:

- One problem from Section 1 – Basic Classes and Objects
- One problem from Section 2 – Inheritance and Encapsulation

---

## ▶️ Start Here

Before you begin, watch the walkthrough video below for guidance on how to approach this assignment.

*[Insert walkthrough video about completing programming assignments]*

---

## 🚀 GitHub Classroom

Open the GitHub Classroom assignment using the link below.

**GitHub Classroom Assignment**

[INSERT ASSIGNMENT LINK]

> WARNING: Submit the **repository** URL in the LMS (Blackboard), not a Codespaces / `github.dev` link (those are private to you).

---

## 📋 Assignment Requirements

Complete:

- One problem from Section 1 – Basic Classes and Objects
- One problem from Section 2 – Inheritance and Encapsulation
- Follow PEP 8 coding conventions
- Test your code with multiple inputs
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

---

## 📁 File Naming

Each problem should be saved as a separate Python file.

| Problem | File Name |
|---------|-----------|
| Rectangle Calculator | `program1a.py` |
| Shopping Cart | `program1b.py` |
| Employee Payroll System | `program2a.py` |
| University People System | `program2b.py` |

---

## 🤖 AI Usage Disclosure

**CRITICAL:** Each Python file must begin with an AI Disclaimer. The autograder will look for this exact text and check the content after it.

Choose the statement that best reflects how AI was (or was not) used while completing your assignment.

### Examples of AI Disclaimers (choose the most appropriate or write your own)

**No AI Use:**

```text
# AI Disclaimer: This code was written without the use of AI tools.
# Any assistance received was from course materials, textbooks, or instructor guidance only.
```

**Minimal AI Use (e.g., syntax help, debugging):**

```text
# AI Disclaimer: This code was written with minimal AI assistance.
# Used AI for: syntax checking and debugging only.
# Core logic and problem-solving approach are my own work.
```

**Moderate AI Use (e.g., code structure, algorithm suggestions):**

```text
# AI Disclaimer: This code was written with moderate AI assistance.
# Used AI for: code structure suggestions and algorithm guidance.
# I implemented the solutions and modified the AI suggestions to fit the requirements.
```

**Extensive AI Use (e.g., significant code generation):**

```text
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: code generation, debugging, and optimization.
# I reviewed, tested, and modified all AI-generated code to ensure it meets requirements.
```

**Unacceptable AI Use (e.g., "vibe coding" without learning):**

```text
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: complete code generation to pass autograder.
# I copied the code without understanding it, just to get a green checkmark.
# I didn't actually learn anything from this assignment.
```

Your program code starts here...

---

## 💻 Programming Problems

### Section 1 - Basic Classes and Objects (Choose One)

#### Problem 1a: Rectangle Calculator

Create a `Rectangle` class to calculate area and perimeter.

**Requirements:**

- Create a `Rectangle` class with `__init__` method taking width and height
- Add `area()` method that returns width * height
- Add `perimeter()` method that returns 2 * (width + height)
- Add `get_info()` method that returns a formatted string with dimensions
- Create at least 2 rectangle objects and display their info, area, and perimeter

**Sample Output:**

```text
Rectangle 1: 5 x 3
Area: 15
Perimeter: 16

Rectangle 2: 8 x 4
Area: 32
Perimeter: 24
```

**Starter shape (complete the class definition):**

```py
# Write your Rectangle class here
class Rectangle:
    # TODO: Implement the __init__ method
    # TODO: Implement the area method
    # TODO: Implement the perimeter method
    # TODO: Implement the get_info method
    pass

# Create rectangle objects
rect1 = Rectangle(5, 3)
rect2 = Rectangle(8, 4)

# Display information
print(f"Rectangle 1: {rect1.get_info()}")
print(f"Area: {rect1.area()}")
print(f"Perimeter: {rect1.perimeter()}")
print()
print(f"Rectangle 2: {rect2.get_info()}")
print(f"Area: {rect2.area()}")
print(f"Perimeter: {rect2.perimeter()}")
```

#### Problem 1b: Shopping Cart

Create a shopping cart program using classes.

**Requirements:**

- Create an `Item` class with `name` and `price` attributes
- Create a `ShoppingCart` class
  - Add a method to add items to the cart
  - Add a method to remove items by name
  - Add a method to display all items in the cart
  - Add a method to calculate and return the total price
- Create at least 2 items and add them to the cart
- Demonstrate adding, removing, displaying items, and printing the total

**Sample Output:**

```text
Items in cart:
- Apple: $0.99
- Bread: $2.50

Total: $3.49

Removing Apple from cart...

Items in cart:
- Bread: $2.50

Total: $2.50
```

**Starter shape (complete the class definitions):**

```py
# Write your classes here
class Item:
    # TODO: Implement the __init__ method
    pass

class ShoppingCart:
    # TODO: Implement the __init__ method
    # TODO: Implement add_item method
    # TODO: Implement remove_item method
    # TODO: Implement display_cart method
    # TODO: Implement get_total method
    pass

# Create items and cart
cart = ShoppingCart()
item1 = Item("Apple", 0.99)
item2 = Item("Bread", 2.50)

cart.add_item(item1)
cart.add_item(item2)
cart.display_cart()
print(f"Total: ${cart.get_total():.2f}")
print()
print("Removing Apple from cart...")
print()
cart.remove_item("Apple")
cart.display_cart()
print(f"Total: ${cart.get_total():.2f}")
```

---

### Section 2 - Inheritance and Encapsulation (Choose One)

#### Problem 2a: Employee Payroll System

Design a payroll system using inheritance.

**Requirements:**

- Create an `Employee` base class with attributes for name
- Create a `SalariedEmployee` subclass that stores a salary and its `get_pay()` returns that salary
- Create a `HourlyEmployee` subclass that stores hours worked and hourly rate; `get_pay()` returns hours * rate
- Create objects for both types and print their names and pay

**Sample Output:**

```text
Alice (Hourly): $600.00
Bob (Salaried): $1200.00
```

**Starter shape (complete the class definitions):**

```py
# Write your classes here
class Employee:
    # TODO: Implement the __init__ method
    # TODO: Implement the get_pay method
    pass

class HourlyEmployee(Employee):
    # TODO: Implement the __init__ method to call super().__init__()
    # TODO: Override the get_pay method
    pass

class SalariedEmployee(Employee):
    # TODO: Implement the __init__ method to call super().__init__()
    pass

# Create employee objects
emp1 = HourlyEmployee("Alice", 40, 15)  # hours, rate
emp2 = SalariedEmployee("Bob", 1200)  # salary

print(f"{emp1.name} (Hourly): ${emp1.get_pay():.2f}")
print(f"{emp2.name} (Salaried): ${emp2.get_pay():.2f}")
```

#### Problem 2b: University People System

Create a hierarchy representing people at a university using inheritance and method overriding.

**Requirements:**

- Create a `Person` base class with `name` attribute
- Add a `get_role()` method that returns `"Person"`
- Add a `do_your_thing()` method to the base class that returns `"[name] is doing their thing"`
- Create a `Student` subclass that overrides `get_role()` to return `"Student"`, and overrides `do_your_thing()` to return `"[name] is studying"`
- Create a `Professor` subclass that overrides `get_role()` to return `"Professor"`, and overrides `do_your_thing()` to return `"[name] is teaching"`
- Create objects and demonstrate polymorphism and specific behaviors

**Sample Output:**

```text
Student: Student
Professor: Professor
Person: Person
Alice is studying
Dr. Smith is teaching
Sam is doing their thing
```

**Starter shape (complete the class definitions):**

```py
# Write your classes here
class Person:
    # TODO: Implement the __init__ method (store name)
    # TODO: Implement get_role method (return "Person")
    # TODO: Implement do_your_thing method (return "[name] is doing their thing")
    pass

class Student(Person):
    # TODO: Implement __init__ to call super().__init__()
    # TODO: Override get_role method (return "Student")
    # TODO: Override do_your_thing method (return "[name] is studying")
    pass

class Professor(Person):
    # TODO: Implement __init__ to call super().__init__()
    # TODO: Override get_role method (return "Professor")
    # TODO: Override do_your_thing method (return "[name] is teaching")
    pass

# Create university people objects
student = Student("Alice")
professor = Professor("Dr. Smith")
person = Person("Sam")

print(f"Student: {student.get_role()}")
print(f"Professor: {professor.get_role()}")
print(f"Person: {person.get_role()}")
print(student.do_your_thing())
print(professor.do_your_thing())
print(person.do_your_thing())
```

---

## 📤 Submission Instructions

1. Complete the required programming problems.
2. Commit and push your files to GitHub.
3. Copy your GitHub repository URL.
4. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Completed one Basic Classes and Objects problem
- ☐ Completed one Inheritance and Encapsulation problem
- ☐ Correct file names
- ☐ AI Disclaimer included
- ☐ Code follows PEP 8 conventions
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
