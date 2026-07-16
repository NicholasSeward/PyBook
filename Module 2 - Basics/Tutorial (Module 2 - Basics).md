# Tutorial: Python Basics - Variables, Types, and Operations

## Learning Objectives
- Understand Python coding conventions (PEP 8)
- Learn basic program structure and flow
- Work with variables and different data types
- Master arithmetic and logical operations
- Handle input/output operations
- Format strings using f-strings
- Convert between data types safely
- Read and understand error messages

---

## Coding Conventions (PEP 8)

**Try this code and identify the convention violations:**

```python
# Bad code - multiple violations
x=5
y=10
if x<y:
    print("x is less than y")
else:
    print("x is greater than or equal to y")
```

**Question 1:** Multiple Choice: What should the first line of the if statement look like with proper PEP 8 formatting?
- A) `if x<y:`
- B) `if x < y:`
- C) `if x  <  y:`
- D) `if  x < y:`

**Question 2:** True/False: Does the code run any different if you add spaces correctly like `x = 5`?

**Question 3:** Multiple Choice: Should you use spaces or tabs when indenting Python code?
- A) Spaces only
- B) Tabs only  
- C) Either spaces or tabs, it doesn't matter
- D) A mix of both

*Reference: [PEP 8 Style Guide](https://peps.python.org/pep-0008/)*

---

## Basic Program Structure

**Try this simple program:**

```python
# Start with a variable
count = 5
# Modify it
count = count + 3
# Print it
print(count)
```

**Question 4:** What is the output of this program?

**Question 5:** What do you get if you print `count` before modifying it?

**Question 6:** Multiple Choice: What error do you get if you try to modify `count` before declaring it?
- A) NameError
- B) TypeError
- C) SyntaxError
- D) ValueError

---

## Variables & Types

**Try these expressions and identify the types:**

```python
# Test these expressions
a = 42
b = "hello"
c = 3.14
d = True
e = [1, 2, 3]
f = {"name": "Alice"}

print(type(a))
print(type(b))
print(type(c))
print(type(d))
print(type(e))
print(type(f))
```

**Question 7:** Match each value with its type:
- `42`
- `3.14`
- `True`
- `{"name": "Alice"}`
- `[1, 2, 3]`
- `"hello"`

**Types:**
- `str`
- `list`
- `int`
- `dict`
- `float`
- `bool`

**Question 8:** Multiple Choice: What is the result of `a + b`?
- A) `TypeError`
- B) `42hello`
- C) `45`

**Question 9:** Multiple Choice: What is the result of `a * 2`?
- A) `84`
- B) `42`
- C) `TypeError`

---

## Arithmetic & Logical Operations

**Try these operations:**

```python
# Arithmetic operations
x = 10
y = 3

print(f"x = {x}, y = {y}")
print(f"Addition: {x + y}")
print(f"Subtraction: {x - y}")
print(f"Multiplication: {x * y}")
print(f"Division: {x / y}")
print(f"Floor division: {x // y}")
print(f"Remainder: {x % y}")
print(f"Power: {x ** y}")

# String operations
text = "Python"
print(f"Text: {text}")
print(f"Text * 3: {text * 3}")
print(f"Text + ' is fun': {text + ' is fun'}")

# Logical operations
p = True
q = False
print(f"p = {p}, q = {q}")
print(f"p and q: {p and q}")
print(f"p or q: {p or q}")
print(f"not p: {not p}")
```

**Question 10:** Multiple Choice: Which operator is closer to what you expect a calculator to do?
- A) `/`
- B) `//`

**Question 11:** Multiple Choice: Which operator is used for exponentiation?
- A) `**`
- B) `^`

**Question 12:** Pick all that apply: Which of the following gives you a True?
- A) `True and False`
- B) `False or True`
- C) `not False`
- D) `False and False`
- E) `not 123`

**Question 13:** What is the result of `True and False`?
- A) `True`
- B) `False`
- C) `Error`
- D) `None`

---

## Input/Output with `input()` and `print()`

**Try this input/output program:**

```python
# Get user input
user_input = input("Enter a number: ")
print(f"You entered: {user_input}")

# Multiply by 3
result = user_input * 3
print(result)
```

**Question 14:** If you enter "5", what is the output of `user_input * 3`?

**Question 15:** Change `user_input = input("Enter a number: ")` to `user_input = int(input("Enter a number: "))`, what is the output if you enter "5"?

**Question 16:** What is the output or error if you enter "hello" instead of a number?

---

## Formatting Strings (f-strings)

**Try this f-string formatting:**

```python
# Basic f-string
name = "Alice"
age = 25
height = 5.5

message = f"Hello, {name}! You are {age} years old and {height} feet tall."
print(message)

# Number formatting
pi = 3.14159
price = 19.99
count = 7

formatted_pi = f"Pi: {pi:.2f}"
formatted_price = f"Price: ${price:.2f}"
formatted_count = f"Count: {count:05d}"

print(formatted_pi)
print(formatted_price)
print(formatted_count)
```

**Question 17:** What do you get for pi if you change `.2f` to the `.3f` format specifier?

**Question 18:** What should `f"Count: {count:05d}"` be changed to to get `007`?

**Question 19:** Does `f"Count: {count:05d}"` work if you change it to `f"Count: {count}"`?

---

## Casting between Types

**Try these type conversions:**

```python
# Working conversions
string_num = "42"
string_float = "3.14"
string_bool = "True"
empty_string = ""

print("=== Working Conversions ===")
print(f"int('42'): {int(string_num)}")
print(f"float('3.14'): {float(string_float)}")
print(f"bool('True'): {bool(string_bool)}")
print(f"str(42): {str(42)}")
print(f"bool('hello'): {bool('hello')}")
print(f"bool(''): {bool(empty_string)}")
```

**Question 20:** Which of the following gives `True` when evaluated?
- A) `bool('')`
- B) `bool('hello')`
- C) `bool(0)`
- D) `bool(1)`
- E) `bool([])`
- F) `bool([1, 2, 3])`

---

## Errors and Tracebacks

**Try this code with an error:**

```python
# Code with an error
x = 10
y = "hello"
result = x + y
print(result)
```

**Question 21:** What line has the error?

**Question 22:** What type of error is this?

**Question 23:** How would you fix this error?
- A) Convert `y` to an integer using `int(y)`
- B) Convert `x` to a string using `str(x)`
- C) Use a different variable name for `result`
- D) Remove the `print(result)` line