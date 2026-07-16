# Module 9 - Classes
## Programming I
### CPSI 17503
#### University of Arkansas at Little Rock

---

## Review from Previous Modules

### Functions and Scope
- Functions organize code and data
- Local vs global variable scope
- Function parameters and return values

### Data Structures
- Lists, dictionaries, and tuples
- Mutable vs immutable objects
- File I/O for data persistence

---

## Learning Objectives

1. **Define classes** to create programmer-defined types
2. **Create objects** and work with attributes and methods
3. **Implement methods** within classes for object behavior
4. **Apply encapsulation** to protect data and control access
5. **Design clean interfaces** for user-friendly classes
6. **Recognize inheritance** and polymorphism concepts

---

## Key Terms

**Class** - A template or blueprint for creating objects

**Object** - An instance of a class with its own data and behavior

**Attribute** - A variable that belongs to an object (data)

**Method** - A function that belongs to a class (behavior)

**Self** - A reference to the current object instance in methods

**Encapsulation** - Bundling data and methods together, hiding implementation details

**Inheritance** - Creating new classes based on existing ones

---

## What are Classes?

### Programmer-Defined Types
- **Built-in types** like `int`, `str`, `list` are predefined
- **Classes** let you create your own types
- **Objects** are instances of these types
- **Attributes** store data for each object
- **Methods** define behavior for objects

### Why Use Classes?
- **Organize related data** and functions together
- **Model real-world objects** and concepts
- **Create reusable code** templates
- **Build complex systems** from simple components

---

## Basic Class Definition

```python
class Time:
    """Represents a time of day."""
    pass

# Create an instance
lunch = Time()
lunch.hour = 11
lunch.minute = 59
```

### Class Anatomy
- **`class` keyword** - defines a new class
- **Class name** - PascalCase (e.g., `Time`)
- **Docstring** - explains what the class represents
- **Instantiation** - calling the class like a function

---

## Attributes and Objects

```python
class Student:
    """Represents a student."""
    pass

alice = Student()
alice.name = "Alice"
alice.gpa = 3.8

print(f"{alice.name}: {alice.gpa}")
```

### Key Concepts
- **Each object** has its own copy of attributes
- **Objects are independent** - changing one doesn't affect others
- **Attributes can be added** dynamically after object creation

---

## Methods and Behavior

```python
class Time:
    """Represents a time of day."""
    
    def print_time(self):
        """Print time in HH:MM:SS format."""
        s = f'{self.hour:02d}:{self.minute:02d}'
        print(s)
    
    def add_minutes(self, minutes):
        """Add minutes to the current time."""
        self.minute += minutes
        if self.minute >= 60:
            self.minute -= 60
            self.hour += 1
```

### Method Characteristics
- **`self` parameter** - refers to the current object instance
- **Access attributes** using `self.attribute_name`
- **Call methods** on objects using dot notation

---

## Constructor Method

```python
class Time:
    """Represents a time of day."""
    
    def __init__(self, hour=0, minute=0):
        """Initialize a Time object."""
        self.hour = hour
        self.minute = minute

# Create objects
lunch = Time(11, 59)
midnight = Time()  # Uses default values
```

### Constructor Benefits
- **Automatic initialization** when creating objects
- **Default values** for optional parameters
- **Consistent object state** from the start

---

## Object Interaction

```python
class Point:
    """Represents a point in 2D space."""
    
    def __init__(self, x=0, y=0):
        self.x = x
        self.y = y
    
    def distance_to(self, other):
        """Calculate distance to another point."""
        dx = self.x - other.x
        dy = self.y - other.y
        return (dx**2 + dy**2)**0.5

# Use the class
p1 = Point(3, 4)
p2 = Point(6, 8)
print(p1.distance_to(p2))
```

---

## Encapsulation

```python
class BankAccount:
    """A simple bank account with balance protection."""
    
    def __init__(self, initial_balance=0):
        self.__balance = initial_balance  # Private
    
    def get_balance(self):
        return self.__balance
    
    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
```

### Access Control
- **Public attributes** - accessible from anywhere
- **Protected** - single underscore `_` (convention)
- **Private** - double underscore `__` (name mangling)

---

## Interface Design

```python
class Book:
    """A book that can be borrowed and returned."""
    
    def __init__(self, title, author):
        self._title = title
        self._author = author
        self._is_borrowed = False
    
    def borrow(self):
        if not self._is_borrowed:
            self._is_borrowed = True
            return True
        return False
    
    def is_available(self):
        return not self._is_borrowed
```

### Interface Principles
- **Simple methods** - easy to understand and use
- **Clear names** - obvious what each method does
- **Safe operations** - prevent users from making mistakes

---

## Inheritance Basics

```python
class Animal:
    """Base class for animals."""
    
    def __init__(self, name):
        self.name = name
    
    def speak(self):
        pass

class Dog(Animal):
    """Dog class inherits from Animal."""
    
    def speak(self):
        return "Woof!"

dog = Dog("Buddy")
print(dog.speak())  # Woof!
```

### Inheritance Benefits
- **Code reuse** - inherit methods from parent
- **Specialization** - override methods for specific behavior
- **Polymorphism** - different objects respond to same calls

---

## Dos and Don'ts

### ✅ DO:
- **Use descriptive class names** in PascalCase
- **Include docstrings** explaining what your class represents
- **Use `__init__`** for object initialization
- **Use private attributes** (`__`) to protect data
- **Make methods simple** and focused on single tasks

### ❌ DON'T:
- **Create classes for everything** - sometimes functions are better
- **Access private attributes** from outside the class
- **Make methods too complex** - break into smaller ones
- **Ignore encapsulation** - expose all attributes publicly

---

## Key Takeaways

### Object-Oriented Programming
- **Classes are templates** for creating objects with data and behavior
- **Objects have state** (attributes) and behavior (methods)
- **Encapsulation protects** data and provides controlled access
- **Inheritance enables** code reuse and specialization

### Best Practices
- **Use meaningful names** for classes, methods, and attributes
- **Document your classes** with clear docstrings
- **Keep classes focused** on single responsibilities
- **Design clean interfaces** that are easy to use

---

## Further Explorations

### Advanced Class Features
- **Class methods** and **static methods** for utility functions
- **Property decorators** for computed attributes
- **Multiple inheritance** and mixins

### Design Patterns
- **Singleton pattern** for unique instances
- **Factory pattern** for object creation
- **Observer pattern** for event handling

### Advanced Python Features
- **Abstract base classes** for defining interfaces
- **Descriptors** for attribute access control
- **Decorators** for method enhancement
