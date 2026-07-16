# Tutorial: Introduction to Programming and Python

## Learning Objectives
- Understand what programming is and how to think like a computer scientist
- Learn basic Python syntax and arithmetic operations
- Practice using the print function and creating strings
- Understand different number systems (decimal, binary, hexadecimal)
- Learn about IDEs and development environments
- Practice debugging and error handling

---

## Experiment 1: Your First Python Program

**Try this code:**
```python
print("Hello, World!")
```

**Now try this:**
```python
print("Hello, World! Welcome to Python!")
```

**Question:** How many lines of output does this code produce?

**Experiment:** Put a '\n' between the two sentences. How many lines of output does this produce? 

---

## Experiment 2: Basic Arithmetic Operations

**Try these arithmetic operations:**
```python
print(5 + 3)
print(10 - 4)
print(6 * 7)
print(21 / 4)
```

**Question:** What is the output of `6 * 7`? (Answer with a number)

**Question:** What is the output of `21 / 4`? (Answer with a number)

**Question:** Try `21 // 4`. What is the output of `21 // 4`? (Answer with a number)

---

## Experiment 3: Working with Functions

**Try these function calls:**
```python
print(abs(-15))
print(round(3.7))
print(len("Python"))
```

**Question:** What is the output of `abs(-15)`? (Answer with a number)

**Question:** What is the output of `round(3.5)`? (Answer with a number)

**Question:** What is the output of `round(4.5)`? (Answer with a number)

Python's `round()` function rounds a number to the nearest integer. If the number is exactly halfway between two integers (like 3.5 or 4.5), Python uses a rule called "round to even" (also known as "bankers' rounding"). This means it will round to the nearest even number.

**Question:** What is the output of `len("asdf")`? (Answer with a number)

**Question:** What is the output of `len("asdf"*10)`? (Answer with a number)

In Python, the `*` operator can be used with strings and integers to repeat the string multiple times.

---

## Experiment 4: String Operations

**Try these string operations:**
```python
print("Hello" + " " + "World")
print("Python " * 3)
print(len("Computer Science"))
```

**Question:** What is the output of `print("Python " * 3)`? (Answer with a number)

---

## Experiment 5: Understanding Types

**Try this code to see different data types:**
```python
print(type(42))
print(type(3.14))
print(type("Hello"))
```

**Question:** What is the output of `type(42)`? (Answer with the exact text shown)

**Now try this:**
```python
print(type(100))
print(type(2.5))
print(type("Python"))
```

**Question:** What is the output of `type(2.5)`? (Answer with the exact text shown)

**Experiment:** Change `type(100)` to `type("100")`. What is the new output?

---

## Experiment 6: Number Systems

**Try converting between number systems:**
```python
# Decimal to binary
print(bin(10))
print(bin(15))

# Decimal to hexadecimal
print(hex(16))
print(hex(255))
```

**Question:** What is the output of `bin(10)`? (Answer with the exact text shown)

**Now try this:**
```python
print(bin(8))
print(hex(10))
print(bin(20))
```

**Question:** What is the output of `hex(10)`? (Answer with the exact text shown)

---

## Experiment 7: Error Handling and Debugging

**Try this code that will cause an error:**
```python
print(5 + "3")
```

**Question:** What type of error message do you see? (Answer with the exact error type shown)

**Now try this:**
```python
print(10 / 0)
```

**Question:** What type of error message do you see? (Answer with the exact error type shown)

---

## Experiment 8: Comments and Documentation

**Try this code with comments:**
```python
# This is a single-line comment
print("Hello")  # This comment is on the same line

"""
This is a multi-line comment
It can span multiple lines
"""
print("World")
```

**Now try this:**
```python
# Program: Calculator
# Author: Student
print(5 + 3)  # Addition
print(10 - 2)  # Subtraction
```

**Question:** Does this print anything?

---
