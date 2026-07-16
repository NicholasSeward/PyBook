# Hello World and Comments

## Hello World

The very first program most programmers write is "Hello, World!". Its purpose is simple: make sure your environment is working and show how to display output.

In Python, it looks like this:

```python
print("Hello, World!")
```

- `print()` is a built-in function that outputs text to the console.
- `"Hello, World!"` is a string of text.

When run, the program prints:
```
Hello, World!
```

This confirms that Python is installed, your IDE works, and you can run code successfully.

## Comments in Python

### Single-Line Comments
- Start with `#`.
- Everything after `#` on that line is ignored by Python.

**Example:**
```python
# This program prints a greeting
print("Hello, World!")  # Output: Hello, World!
```

### Multi-Line (or Block) Comments
Python doesn't have a true "block comment" symbol, but programmers often use triple quotes (`""" """` or `''' '''`) to create multi-line strings that aren't assigned to a variable.

**Example:**
```python
"""
Author: Bob Smith
Assignment: Hello World
Date: 1/1/2025
"""
print("Hello, World!")
```

## Why Use Comments?

- **Explain intent**: Describe why something is done, not just what is done.
- **Documentation**: Help others (and your future self) understand your code.
- **Disable code temporarily**: Comment out a line during debugging.

## When Not to Comment

Too many comments can clutter your code. In fact, comments can cause confusion if they're:

- **Obvious**: `x = x + 1  # adds 1 to x` ← unnecessary
- **Outdated**: If you change code but forget to update comments, they can mislead readers.
- **Repetitive**: Good code should mostly explain itself with clear variable names and structure.

## ✅ Rule of Thumb

- Use comments to explain **why**, not **what**.
- Let the code itself explain **what**.

## Key Takeaways

- Hello World is your first working Python program.
- Use `#` for single-line comments.
- Use `""" """` for multi-line explanations or documentation strings.
- Comment wisely: focus on intent, avoid clutter, and keep comments up to date.
