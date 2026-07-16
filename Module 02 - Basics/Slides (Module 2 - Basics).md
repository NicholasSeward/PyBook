# Module 2 - Basics
## Programming I
### CPSI 17503
#### University of Arkansas at Little Rock

---

## Review from Module 1

**What we learned:**
- Programming basics and Python fundamentals
- Writing simple programs with print statements
- Basic arithmetic operations and data types
- Using functions and expressions
- Debugging mindset and error types
- IDE setup and Git basics

**Key concepts:**
- Python is an interpreted language
- Every detail matters in formal languages
- Comments explain WHY, not WHAT
- Functions use parentheses: `print("Hello")`
- Types: `int`, `float`, `str`

---

## Learning Objectives

- Understand variables and assignment statements
- Learn about Python keywords and naming conventions
- Master the import statement and module usage
- Understand expressions vs statements
- Learn proper use of the print function
- Master function arguments and parameters
- Write effective comments
- Distinguish between different error types
- Apply PEP 8 coding conventions
- Understand type casting and conversion

---

## Key Terms

- **Variable**: A name that refers to a value
- **Assignment Statement**: Statement that assigns a value to a variable
- **State Diagram**: Visual representation of variables and their values
- **Keyword**: Special word used to specify program structure
- **Module**: File containing Python code and functions
- **Import Statement**: Statement that reads a module file
- **Expression**: Code that produces a value
- **Statement**: Code that performs an action
- **Argument**: Value provided to a function
- **Comment**: Text that explains code but has no effect

---

## Variables

**What is a variable?**
- A name that refers to a value
- Like a labeled box that stores data
- Can hold different types of data

**Creating variables:**
```python
n = 17                    # Integer
pi = 3.14159             # Float
message = "Hello World"   # String
```

**Assignment statement format:**
- Variable name on the left
- Equals sign (`=`) in the middle
- Value/expression on the right

---

## Variable Names

**Rules for variable names:**
- Can be as long as you want
- Can contain letters and numbers
- **Cannot start with a number**
- Can use underscores (`_`)
- Cannot use Python keywords

**Good examples:**
```python
user_name = "John"
age = 25
total_score = 100
```

**Bad examples:**
```python
2name = "John"      # Starts with number
user-name = "John"  # Contains hyphen
class = "CS101"     # Python keyword
```

---

## Python Keywords

**Keywords are reserved words that cannot be used as variable names:**

```python
False      await      else       import     pass
None       break      except     in         raise
True       class      finally    is         return
and        continue   for        lambda     try
as         def        from       nonlocal   while
assert     del        global     not        with
async      elif       if         or         yield
```

**Don't memorize this list!**
- Most IDEs highlight keywords in different colors
- You'll learn them as you program
- If you get a syntax error, check if you used a keyword

---

## State Diagrams

**Visual representation of variables:**
```
n → 17
pi → 3.14159
message → "Hello World"
```

**Why use state diagrams?**
- Shows the "state of mind" of your variables
- Helps visualize how data flows through your program
- Useful for debugging and understanding code
- Shows relationships between variables

**In Python:**
- Variables are stored in memory
- Each variable has a name and a value
- Values can change during program execution

---

## The Import Statement

**Why import?**
- Python comes with many built-in features
- But some features are in separate modules
- You must import modules to use them

**Basic import:**
```python
import math
```

**Using imported modules:**
```python
import math
print(math.pi)           # Access variables
result = math.sqrt(25)   # Use functions
```

**The dot operator (`.`):**
- Connects module name to variable/function name
- `math.pi` means "pi from the math module"

---

## Common Modules

**Math module:**
```python
import math
math.pi          # Mathematical constant π
math.sqrt(25)    # Square root
math.pow(2, 3)   # 2 to the power of 3
```

**Other useful modules:**
```python
import random    # Random number generation
import time      # Time-related functions
import os        # Operating system functions
```

**Built-in functions (no import needed):**
```python
print()          # Display output
len()            # Get length
int(), float(), str()  # Type conversion
```

---

## Expressions vs Statements

**Expressions:**
- Produce a value
- Can be evaluated
- Examples: `2 + 3`, `math.pi`, `len("Hello")`

**Statements:**
- Perform an action
- Have no value
- Examples: `x = 5`, `import math`, `print("Hello")`

**Key difference:**
```python
result = 2 + 3    # Expression 2+3 produces value 5
x = 5             # Statement assigns value (no value itself)
```

---

## The Print Function

**Basic usage:**
```python
print("Hello World")           # Single argument
print("Hello", "World")        # Multiple arguments
print("Value:", 42)            # Mixed types
```

**Print behavior:**
- Automatically adds spaces between arguments
- Moves to next line after printing
- Converts all arguments to strings

**Examples:**
```python
name = "Alice"
age = 25
print("Name:", name, "Age:", age)
# Output: Name: Alice Age: 25
```

---

## Function Arguments

**Arguments are values passed to functions:**
```python
print("Hello")           # 1 argument
math.pow(2, 3)          # 2 arguments
round(3.14159, 2)       # 2 arguments (value, decimal places)
```

**Argument types:**
- **Required**: Must be provided
- **Optional**: Have default values
- **Variable**: Can take any number

**Common errors:**
```python
math.sqrt()              # TypeError: missing argument
math.sqrt("25")          # TypeError: wrong type
math.sqrt(25, 5)        # TypeError: too many arguments
```

---

## Comments

**Why comment?**
- Code gets complex quickly
- Comments explain what and why
- Help others (and future you) understand code

**Single-line comments:**
```python
# Calculate area of circle
radius = 5
area = math.pi * radius ** 2  # Area = πr²
```

**Multi-line comments:**
```python
"""
This program calculates the volume of a sphere
using the formula V = (4/3)πr³
"""
```

**Good vs Bad comments:**
```python
x = 5     # x equals 5          # BAD: Obvious
x = 5     # Initial position     # GOOD: Explains purpose
```

---

## Error Types

**Three main categories:**

**1. Syntax Errors:**
- Code structure is wrong
- Python can't understand what you wrote
- Program won't run at all
```python
x = 5    # Correct
x = 5    # SyntaxError: invalid syntax
```

**2. Runtime Errors:**
- Code runs but fails during execution
- Also called exceptions
```python
print(10 / 0)  # ZeroDivisionError
```

**3. Semantic Errors:**
- Code runs without errors
- But doesn't do what you intended
- Hardest to find and fix

---

## Debugging Strategies

**When you encounter errors:**

**1. Read the error message carefully:**
- Look at the line number
- Understand what Python is telling you
- Don't panic - errors are learning opportunities

**2. Check common issues:**
- Variable names spelled correctly?
- Proper syntax (parentheses, quotes)?
- Right number of arguments?

**3. Use print statements:**
```python
x = 5
print("x =", x)  # See what x actually contains
```

---

## Coding Conventions (PEP 8)

**PEP 8 is Python's style guide:**

**Variable naming:**
```python
user_name = "John"      # Use underscores for multi-word names
age = 25                # Lowercase letters
MAX_SCORE = 100         # Uppercase for constants
```

**Spacing:**
```python
x = 5 + 3              # Spaces around operators
def calculate_area():   # Two blank lines before function
    radius = 5         # 4 spaces for indentation
    return math.pi * radius ** 2
```

**Why follow conventions?**
- Makes code readable
- Helps others understand your code
- Professional standard

---

## Type Casting

**Converting between data types:**

**String to Number:**
```python
age = "25"
age_num = int(age)      # String "25" → integer 25
height = "5.8"
height_num = float(height)  # String "5.8" → float 5.8
```

**Number to String:**
```python
score = 95
score_str = str(score)  # Integer 95 → string "95"
```

**When casting fails:**
```python
int("abc")              # ValueError: invalid literal
float("12.34.56")       # ValueError: invalid literal
```

---

## Basic Program Structure

**Typical Python program layout:**
```python
# 1. Import statements
import math
import random

# 2. Constants (if any)
PI = math.pi
MAX_ATTEMPTS = 3

# 3. Variable definitions
radius = 5
name = "Student"

# 4. Functions (if any)
def calculate_perimeter(r):
    return 2 * PI * r

# 5. Main program logic
area = PI * radius ** 2
print(f"Area of circle: {area}")
perimeter = calculate_perimeter(radius)
print(f"Perimeter: {perimeter}")
```

**Important Note:** Functions must be defined before they are used because Python is an interpreted language. The interpreter reads and executes code line by line, so it needs to know about a function before it can call it.

---

## Common Pitfalls

**Things to avoid:**

**1. Forgetting to import:**
```python
print(math.pi)  # NameError: name 'math' is not defined
# Should be: import math first
```

**2. Wrong variable names:**
```python
Name = "John"   # Capital N - not conventional
name = "John"   # Better
```

**3. Missing parentheses:**
```python
print "Hello"   # SyntaxError
print("Hello")  # Correct
```

**4. Ignoring error messages:**
- Always read error messages
- They tell you exactly what's wrong

---

## Key Takeaways

1. **Variables store data** - use descriptive names
2. **Import what you need** - modules provide extra functionality
3. **Expressions produce values** - statements perform actions
4. **Print displays output** - essential for seeing results
5. **Comments explain why** - not what the code does
6. **Follow PEP 8** - makes code professional and readable
7. **Handle errors gracefully** - they're learning opportunities
8. **Type casting converts** - between strings, integers, floats
9. **Structure matters** - organize your code logically
10. **Practice debugging** - it's a crucial programming skill

---

## Next Steps

- Practice creating variables with different data types
- Experiment with the math module and other imports
- Write programs that use print statements effectively
- Practice commenting your code
- Follow PEP 8 conventions in all your code
- Debug simple programs to understand error messages
- Work on the Chapter 2 exercises
- Build small programs combining multiple concepts
