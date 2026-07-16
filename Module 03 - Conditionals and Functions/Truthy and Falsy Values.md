# Truthy and Falsy Values

## Overview
In Python, every value can be treated as either "truthy" or "falsy" in boolean contexts. Understanding this concept helps you write cleaner, more Pythonic code.

## What are Truthy and Falsy Values?

- **Truthy values**: Values that Python considers `True` in boolean contexts
- **Falsy values**: Values that Python considers `False` in boolean contexts

## Falsy Values in Python

Python has exactly **6 falsy values**:

```python
# All of these are considered False
False
None
0
0.0
""  # Empty string
[]   # Empty list
()   # Empty tuple
{}   # Empty dictionary
set() # Empty set
```

## Truthy Values

Everything else is considered truthy:

```python
# All of these are considered True
True
42          # Non-zero numbers
-5          # Negative numbers
3.14        # Non-zero floats
"hello"     # Non-empty strings
[1, 2, 3]   # Non-empty lists
(1, 2)      # Non-empty tuples
{"a": 1}    # Non-empty dictionaries
{1, 2}      # Non-empty sets
```

## How Python Uses Truthy/Falsy Values

### In if Statements
```python
name = "Alice"
if name:  # Same as: if name != ""
    print("Hello, " + name)

# This is equivalent to:
if name != "":
    print("Hello, " + name)
```

### In while Loops
```python
numbers = [1, 2, 3, 4, 5]
while numbers:  # Same as: while len(numbers) > 0
    print(numbers.pop())

# This is equivalent to:
while len(numbers) > 0:
    print(numbers.pop())
```

### In and/or Operations
```python
# and returns the first falsy value, or the last truthy value
result = "hello" and "world"  # Returns "world"
result = "" and "world"       # Returns ""
result = 0 and "world"        # Returns 0

# or returns the first truthy value, or the last falsy value
result = "hello" or "world"   # Returns "hello"
result = "" or "world"        # Returns "world"
result = 0 or "world"         # Returns "world"
```

## Common Use Cases

### Checking if a List is Empty
```python
# Good - Pythonic way
if not my_list:
    print("List is empty")

# Less Pythonic
if len(my_list) == 0:
    print("List is empty")
```

### Default Values
```python
def greet(name=None):
    if not name:  # If name is None or empty string
        name = "Guest"
    print(f"Hello, {name}!")

greet()        # Output: Hello, Guest!
greet("")     # Output: Hello, Guest!
greet("Alice") # Output: Hello, Alice!
```

### Checking User Input
```python
user_input = input("Enter your name: ")
if user_input:  # If user entered something
    print(f"Hello, {user_input}!")
else:
    print("You didn't enter a name.")
```

## The `bool()` Function

You can explicitly convert any value to a boolean:

```python
print(bool(0))        # False
print(bool(1))        # True
print(bool(""))       # False
print(bool("hello"))  # True
print(bool([]))       # False
print(bool([1, 2]))   # True
print(bool(None))     # False
```

## Common Pitfalls

### String "0" vs Integer 0
```python
# These are different!
print(bool(0))      # False
print(bool("0"))    # True (non-empty string)

# In comparisons
if 0:          # False
    print("This won't print")

if "0":       # True
    print("This will print")
```

### Empty vs None
```python
# These are different falsy values
empty_list = []
none_value = None

print(empty_list == None)  # False
print(empty_list is None)  # False

# Check for None specifically
if value is None:
    print("Value is None")

# Check for empty
if not value:
    print("Value is falsy (None, empty, 0, etc.)")
```

## Best Practices

### 1. Use Truthy/Falsy for Simple Checks
```python
# Good
if user_name:
    print(f"Hello, {user_name}")

# Good
if not numbers:
    print("No numbers to process")
```

### 2. Be Explicit for Complex Logic
```python
# Good - explicit comparison
if age >= 18:
    print("Adult")

# Good - explicit check
if len(items) > 0:
    print("Has items")
```

### 3. Use `is` for None Checks
```python
# Good
if value is None:
    print("Value is None")

# Avoid
if value == None:
    print("Value is None")
```

## Examples in Practice

### Function with Default Parameters
```python
def create_user(name, age=None, email=None):
    user = {"name": name}
    
    if age:  # Only add if age is provided and not 0
        user["age"] = age
    
    if email:  # Only add if email is provided and not empty
        user["email"] = email
    
    return user

# Test the function
user1 = create_user("Alice", 25, "alice@email.com")
user2 = create_user("Bob")  # age and email will be None
user3 = create_user("Charlie", 0, "")  # 0 and "" are falsy

print(user1)  # {'name': 'Alice', 'age': 25, 'email': 'alice@email.com'}
print(user2)  # {'name': 'Bob'}
print(user3)  # {'name': 'Charlie'}
```

### List Processing
```python
def process_items(items):
    if not items:  # Check if list is empty
        print("No items to process")
        return
    
    print(f"Processing {len(items)} items...")
    for item in items:
        if item:  # Check if item is truthy
            print(f"Processing: {item}")
        else:
            print("Skipping falsy item")

# Test with different inputs
process_items([1, 2, 3])      # Processes all items
process_items([1, 0, 3, ""])  # Skips 0 and empty string
process_items([])              # No items to process
```

## Summary

Understanding truthy and falsy values makes your Python code:
- **More readable**: `if name:` is clearer than `if name != ""`
- **More Pythonic**: Follows Python's philosophy of explicit over implicit
- **More efficient**: Avoids unnecessary comparisons
- **More maintainable**: Less code to write and debug

Remember: Python has exactly 6 falsy values, and everything else is truthy. Use this knowledge to write cleaner, more expressive code!
