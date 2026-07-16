# Modular Design and Decomposition

## Overview
Modular design means breaking big problems into smaller pieces. Each piece does one job.

## Why Use Modular Design?

Think of it like building with LEGO blocks:
- Each block has one purpose
- You can test each block separately
- You can reuse blocks in different projects

## Simple Example: Student Grades

Instead of one big function, we break it into smaller functions:

```python
def calculate_average(scores):
    """Calculate the average of scores."""
    if not scores:
        return 0
    return sum(scores) / len(scores)

def find_highest(scores):
    """Find the highest score."""
    if not scores:
        return None
    return max(scores)

def analyze_grades(scores):
    """Analyze grades using smaller functions."""
    average = calculate_average(scores)
    highest = find_highest(scores)
    
    return {
        'average': average,
        'highest': highest
    }

# Test the modular approach
student_scores = [85, 92, 78, 96, 88]
result = analyze_grades(student_scores)
print(f"Grades: {student_scores}")
print(f"Result: {result}")
```

**Output:**
```
Grades: [85, 92, 78, 96, 88]
Result: {'average': 87.8, 'highest': 96}
```

## Benefits

### 1. Easier to Test
```python
# Test individual functions
print(f"Average: {calculate_average(student_scores)}")
print(f"Highest: {find_highest(student_scores)}")
```

### 2. Easier to Reuse
```python
# Use the same functions for different data
class_scores = [90, 85, 95, 88, 92]
class_result = analyze_grades(class_scores)
print(f"Class result: {class_result}")
```

## Simple Calculator Example

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        return "Error: Cannot divide by zero"
    return a / b

def calculator(operation, a, b):
    if operation == "add":
        return add(a, b)
    elif operation == "subtract":
        return subtract(a, b)
    elif operation == "multiply":
        return multiply(a, b)
    elif operation == "divide":
        return divide(a, b)
    else:
        return "Error: Unknown operation"

# Test the calculator
print(f"5 + 3 = {calculator('add', 5, 3)}")
print(f"10 - 4 = {calculator('subtract', 10, 4)}")
print(f"6 * 7 = {calculator('multiply', 6, 7)}")
print(f"15 / 3 = {calculator('divide', 15, 3)}")
```

**Output:**
```
5 + 3 = 8
10 - 4 = 6
6 * 7 = 42
15 / 3 = 5.0
```

## How to Break Down Problems

### Step 1: Find the main operations
- What does your program need to do?
- Break it into smaller tasks

### Step 2: Make each function do one thing
- `calculate_average()` - just calculates average
- `find_highest()` - just finds highest number
- `analyze_grades()` - uses other functions

## Best Practices

### 1. One Function = One Job
```python
# Good - each function does one thing
def clean_text(text):
    return text.strip().lower()

def count_words(text):
    return len(text.split())

def analyze_text(text):
    cleaned = clean_text(text)
    word_count = count_words(cleaned)
    return f"Words: {word_count}"
```

### 2. Use Clear Names
```python
def f(x, y):  # Bad - what does this do?
    return x + y

def add_numbers(a, b):  # Good - clear what it does
    return a + b
```

## Summary

Modular design helps you:

✅ **Break big problems into small pieces**  
✅ **Test each piece separately**  
✅ **Reuse code in different places**  
✅ **Work with others on different parts**  

**Key rule:** Each function should do ONE thing well.

**Think of it this way:**
- 🧩 **Puzzle pieces** - each piece has one job
- 🏗️ **Building blocks** - stack them together
- 🔧 **Toolbox** - each tool does one job

Start small and build up!
