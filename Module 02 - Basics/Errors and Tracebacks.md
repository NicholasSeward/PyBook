# Errors and Tracebacks

## Overview
When your Python program has a problem, it stops and shows you an error message. Understanding these error messages helps you fix your code quickly.

## Three Types of Errors

### 1. Syntax Errors
These happen when Python can't understand your code structure.

```python
# Missing colon
if x > 5
    print("x is big")

# SyntaxError: invalid syntax
```

**Common causes:**
- Missing colons (`:`)
- Unmatched parentheses or quotes
- Wrong indentation

### 2. Runtime Errors
These happen while your program is running.

```python
# Division by zero
result = 10 / 0
# ZeroDivisionError: division by zero

# List index too big
numbers = [1, 2, 3]
print(numbers[5])
# IndexError: list index out of range
```

### 3. Logical Errors
Your program runs but gives wrong answers.

```python
# Meant to find average, but divided by wrong number
numbers = [1, 2, 3, 4, 5]
total = sum(numbers)
count = len(numbers)
average = total / (count - 1)  # Should be just 'count'
print(average)  # Wrong answer!
```

## Reading Error Messages

### Simple Error
```
Traceback (most recent call last):
  File "example.py", line 5, in <module>
    result = 10 / 0
ZeroDivisionError: division by zero
```

**What this tells you:**
- **File**: Which file had the error
- **Line**: Which line number had the error  
- **Error type**: What kind of error occurred
- **Error message**: What went wrong

### Error in a Function
```python
def divide(a, b):
    return a / b

def calculate_average(numbers):
    total = sum(numbers)
    count = len(numbers)
    return divide(total, count)

# Call with empty list
numbers = []
result = calculate_average(numbers)
```

**Error message:**
```
Traceback (most recent call last):
  File "example.py", line 12, in <module>
    result = calculate_average(numbers)
  File "example.py", line 7, in calculate_average
    return divide(total, count)
  File "example.py", line 2, in divide
    return a / b
ZeroDivisionError: division by zero
```

**How to read it:**
1. **Line 12**: Error happened when calling `calculate_average`
2. **Line 7**: Inside `calculate_average`, when calling `divide`
3. **Line 2**: Inside `divide`, when trying to divide
4. **Root cause**: Division by zero because `count` is 0

## Common Error Types

### ValueError
Wrong value for the right type.

```python
# Can't convert "abc" to a number
age = int("abc")
# ValueError: invalid literal for int() with base 10: 'abc'
```

### TypeError
Wrong type for the operation.

```python
# Can't add string and number
result = "Hello" + 5
# TypeError: can only concatenate str (not "int") to str
```

### IndexError
Trying to access a list position that doesn't exist.

```python
fruits = ["apple", "banana"]
print(fruits[2])  # Only has positions 0 and 1
# IndexError: list index out of range
```

## Simple Debugging Steps

### 1. Read the Error Message
- Look at the line number
- Read the error type and message
- Follow the traceback to find the root cause

### 2. Add Print Statements
```python
def calculate_area(length, width):
    print(f"Debug: length = {length}, width = {width}")
    
    area = length * width
    print(f"Debug: calculated area = {area}")
    return area

result = calculate_area(5, 3)
print(f"Final result: {result}")
```

### 3. Handle Errors Gracefully
```python
def safe_divide(a, b):
    try:
        result = a / b
        return result
    except ZeroDivisionError:
        print("Error: Cannot divide by zero")
        return None

# Test the function
print(safe_divide(10, 2))    # Works fine
print(safe_divide(10, 0))    # Handles error gracefully
```

## Quick Tips

1. **Start from the bottom** of the error message - it shows the actual problem
2. **Check the line number** - that's where the error occurred
3. **Look at the error type** - tells you what kind of problem it is
4. **Add print statements** to see what your variables contain
5. **Use try-except** to handle expected errors gracefully

## Summary

Errors are normal when programming! They help you find and fix problems. Remember:
- Read error messages carefully
- Look at the line numbers
- Add print statements to debug
- Use try-except for error handling

The more you practice debugging, the faster you'll become at fixing problems in your code.
