# Scope (Local, Global)

## Overview
Scope is about where variables can be used in your code. Think of it as the "visibility" of a variable.

## Simple Example

```python
# This variable is "global" - can be used anywhere in this file
name = "Alice"

def say_hello():
    # This variable is "local" - only exists inside this function
    greeting = "Hello"
    print(f"{greeting}, {name}!")

say_hello()
print(name)      # This works - name is global
print(greeting)  # This will cause an error! greeting is local
```

## What Happens?

### Global Variables
- Variables defined **outside** functions
- Can be used **anywhere** in your code
- Live for the entire time your program runs

### Local Variables  
- Variables defined **inside** functions
- Only exist **while the function is running**
- Are destroyed when the function finishes

## Why Does This Matter?

### 1. Local Variables Keep Functions Independent
```python
def calculate_area():
    length = 10  # Local variable
    width = 5    # Local variable
    area = length * width
    return area

def calculate_perimeter():
    length = 20  # Different local variable
    width = 8    # Different local variable
    perimeter = 2 * (length + width)
    return perimeter

# These functions don't interfere with each other
print(calculate_area())      # Output: 50
print(calculate_perimeter()) # Output: 56
```

### 2. Global Variables Can Be Shared
```python
# Global variable - shared by all functions
total_score = 0

def add_points(points):
    global total_score  # Need this to change global variable
    total_score += points
    print(f"Added {points} points. Total: {total_score}")

def reset_score():
    global total_score
    total_score = 0
    print("Score reset to 0")

add_points(10)  # Output: Added 10 points. Total: 10
add_points(5)   # Output: Added 5 points. Total: 15
reset_score()    # Output: Score reset to 0
add_points(3)   # Output: Added 3 points. Total: 3
```

## Common Mistakes

### Mistake 1: Trying to Use Local Variables Outside Functions
```python
def create_name():
    first_name = "John"
    last_name = "Doe"
    full_name = first_name + " " + last_name
    return full_name

# This works
result = create_name()
print(result)

# This will cause an error!
print(first_name)  # first_name doesn't exist here
```

### Mistake 2: Forgetting `global` When Changing Global Variables
```python
counter = 0

def increment():
    counter += 1  # Error! Python thinks counter is local
    print(counter)

# Fix: Add global declaration
def increment():
    global counter
    counter += 1
    print(counter)
```

## Best Practices

### 1. Keep Functions Simple
```python
# Good - function gets all data it needs
def greet(name):
    print(f"Hello, {name}!")

# Less good - function relies on global variable
def greet():
    global user_name
    print(f"Hello, {user_name}!")
```

### 2. Use Global Variables Sparingly
```python
# Good - use for things that should be shared
PI = 3.14159
MAX_ATTEMPTS = 3

# Less good - too many globals
user_name = "Alice"
user_age = 25
user_email = "alice@email.com"
```

## Summary

**Simple rules to remember:**
1. Variables inside functions are **local** - only exist while the function runs
2. Variables outside functions are **global** - can be used anywhere
3. Use `global` keyword when you want to change a global variable inside a function
4. Keep functions independent by passing data as parameters instead of relying on globals

**Think of it this way:**
- **Local variables** are like temporary notes you write during a meeting
- **Global variables** are like information posted on the wall that everyone can see

Understanding scope helps you write better functions and avoid confusing bugs!
