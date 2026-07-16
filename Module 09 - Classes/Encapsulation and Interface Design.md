# Encapsulation and Interface Design

## What is Encapsulation?

Encapsulation is like putting your data in a box with controlled access. Think of it like a vending machine:
- You can't reach inside to grab items directly
- You use buttons and slots to interact with it
- The machine controls how you access its contents
- The internal workings are hidden from you

## The Theory

### Why Encapsulate?
- **Data Protection** - prevent accidental changes to important data
- **Control Access** - decide how and when data can be modified
- **Hide Complexity** - users don't need to know how things work inside
- **Maintain Code** - easier to change internal logic without breaking external code

### Access Levels
- **Public** - anyone can access (normal attributes and methods)
- **Protected** - internal use, but accessible if needed (single underscore `_`)
- **Private** - only the class itself can access (double underscore `__`)

## Basic Examples

### Private Attributes
```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private - can't access from outside
    
    def get_balance(self):
        return self.__balance     # Public method to access private data
    
    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

# Use the class
account = BankAccount(1000)
print(account.get_balance())  # Works
# print(account.__balance)    # Error! Can't access private attribute
```

### Protected Attributes
```python
class Student:
    def __init__(self, name, gpa):
        self._name = name      # Protected - internal use
        self.__gpa = gpa       # Private - very hidden
    
    def get_gpa(self):
        return self.__gpa      # Public method to access private data
```

## Interface Design

### What is a Good Interface?
- **Simple** - easy to understand and use
- **Clear** - obvious what each method does
- **Consistent** - similar operations work the same way
- **Safe** - prevents users from making mistakes

### Example: Simple Interface
```python
class Book:
    def __init__(self, title, author):
        self._title = title
        self._author = author
        self._is_borrowed = False
    
    # Simple, clear methods
    def borrow(self):
        if not self._is_borrowed:
            self._is_borrowed = True
            return True
        return False
    
    def return_book(self):
        self._is_borrowed = False
    
    def is_available(self):
        return not self._is_borrowed
```

## Key Concepts

### 1. Hide Implementation Details
Users don't need to know:
- How data is stored internally
- What calculations happen behind the scenes
- What helper methods exist

### 2. Provide Clear Methods
Instead of letting users access data directly:
- Give them methods with clear names
- Control what they can do
- Prevent invalid operations

### 3. Use Naming Conventions
- **No underscore** - public (anyone can use)
- **Single underscore** - protected (internal use)
- **Double underscore** - private (very hidden)

## Real-World Analogy

Think of a car:
- **Public interface**: steering wheel, gas pedal, brake pedal
- **Protected parts**: engine compartment (mechanic can access)
- **Private parts**: internal engine workings (only the car itself controls)

You drive the car using the public interface. You don't need to know how the engine works inside.

## Summary

✅ **Encapsulation** - hide data and provide controlled access  
✅ **Private attributes** - use `__` to hide data completely  
✅ **Protected attributes** - use `_` for internal use  
✅ **Public methods** - provide clean interface for users  
✅ **Hide complexity** - users see simple, clear methods  
✅ **Good design** - classes that are easy to use correctly  

Good encapsulation makes your classes more reliable and easier to use!
