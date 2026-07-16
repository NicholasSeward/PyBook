# Practice Assignment: Module 9 - Classes

## Overview
Complete **2 problems total** - choose **1 from each section** below. Each section focuses on different aspects of object-oriented programming with classes.

## Instructions
- Choose **1 problem from Section 1** (Basic Classes and Objects)
- Choose **1 problem from Section 2** (Inheritance and Encapsulation)  
- Use proper PEP 8 coding conventions
- Test your code with different inputs

## File Naming and Submission

### File Naming
Each problem should be a separate file:
- **Problem 1a:** `program1a.py` (Rectangle Calculator)
- **Problem 1b:** `program1b.py` (Shopping Cart)
- **Problem 2a:** `program2a.py` (Employee Payroll System)
- **Problem 2b:** `program2b.py` (University People System)

### AI Disclaimer
Each file must include an AI Disclaimer at the top.

### Submission Process
1. Create your program files
2. Test your code thoroughly
3. Commit and push to GitHub
4. Submit your repository URL

**Example repository URL:** `https://github.com/Seward-Classes/practice-09-username`

---

## Section 1: Basic Classes and Objects (Choose 1)

### 1a: Rectangle Calculator

**File:** `program1a.py`

Create a Rectangle class to calculate area and perimeter.

**Requirements:**
- Create a `Rectangle` class with `__init__` method taking width and height
- Add `area()` method that returns width * height
- Add `perimeter()` method that returns 2 * (width + height)
- Add `get_info()` method that returns a formatted string with dimensions
- Create at least 2 rectangle objects and display their info, area, and perimeter

**Your code should produce this output:**
```
Rectangle 1: 5 x 3
Area: 15
Perimeter: 16

Rectangle 2: 8 x 4
Area: 32
Perimeter: 24
```

**Here's how your main code should look (complete the class definition):**

```python
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

---

### 1b: Shopping Cart

**File:** `program1b.py`

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

**Your code should produce this output:**
```
Items in cart:
- Apple: $0.99
- Bread: $2.50

Total: $3.49

Removing Apple from cart...

Items in cart:
- Bread: $2.50

Total: $2.50
```

**Here's how your main code should look (complete the class definitions):**

```python
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

## Section 2: Inheritance and Encapsulation (Choose 1)

### 2a: Employee Payroll System

**File:** `program2a.py`

Design a payroll system using inheritance.

**Requirements:**
- Create an `Employee` base class with attributes for name
- Create a `SalariedEmployee` subclass that stores a salary and its `get_pay()` returns that salary
- Create a `HourlyEmployee` subclass that stores hours worked and hourly rate; `get_pay()` returns hours * rate
- Create objects for both types and print their names and pay

**Your code should produce this output:**
```
Alice (Hourly): $600.00
Bob (Salaried): $1200.00
```

**Here's how your main code should look (complete the class definitions):**

```python
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

---

### 2b: University People System

**File:** `program2b.py`

Create a hierarchy representing people at a university using inheritance and method overriding.

**Requirements:**
- Create a `Person` base class with `name` attribute
- Add a `get_role()` method that returns "Person"
- Add a `do_your_thing()` method to the base class that returns "`[name] is doing their thing`"
- Create a `Student` subclass that overrides `get_role()` to return "Student", and overrides `do_your_thing()` to return "`[name] is studying`"
- Create a `Professor` subclass that overrides `get_role()` to return "Professor", and overrides `do_your_thing()` to return "`[name] is teaching`"
- Create objects and demonstrate polymorphism and specific behaviors

**Your code should produce this output:**
```
Student: Student
Professor: Professor
Person: Person
Alice is studying
Dr. Smith is teaching
Sam is doing their thing
```

**Here's how your main code should look (complete the class definitions):**

```python
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

## Submission Checklist

- [ ] Completed 1 problem from Section 1 (Basic Classes and Objects)
- [ ] Completed 1 problem from Section 2 (Inheritance and Encapsulation)
- [ ] Each file follows the naming convention (program1a.py, program1b.py, etc.)
- [ ] Each file includes an AI Disclaimer at the top
- [ ] Each file uses appropriate class concepts
- [ ] Code is tested and working properly
- [ ] All files are committed and pushed to GitHub
- [ ] Repository URL is submitted on BlackBoard

