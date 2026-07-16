# Tutorial: Conditionals and Functions

## Learning Objectives
- Understand function definitions, parameters, and return values
- Master conditional statements (if, elif, else)
- Learn about boolean expressions and logical operators
- Understand variable scope (local vs global)
- Work with truthy and falsy values
- Practice recursion and function composition
- Handle modulus operator and integer division

---

**Function definitions, parameters, and return values:**
```python
def greet(name):
    return f"Hello, {name}!"

message = greet("Alice")
print(message)  # Output: Hello, Alice!
```

**Question 1:** Multiple Choice: What prints if you did `message = greet`?
- A) `Hello, Alice!`
- B) `<function greet at 0x...>`
- C) `None`
- D) Error

**Question 2:** Multiple Choice: What prints if you did `message = greet()`?
- A) `Hello, Alice!`
- B) `<function greet at 0x...>`
- C) `None`
- D) Error

**Question 3:** Multiple Choice: What prints as is (with `message = greet("Alice")`)?
- A) `Hello, Alice!`
- B) `<function greet at 0x...>`
- C) `None`
- D) Error


**Conditional statements:**
```python
age = 18
if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teenager")
else:
    print("Child")
```

**Boolean expressions and logical operators:**
```python
x = 5
y = 10
print(x > 0 and y < 20)  # True
print(x == 5 or y == 5)  # True
print(not (x > 10))      # True
```

**Question 4:** Multiple Choice: Convert `not(x > 10)` to an equivalent inequality?
- A) `x <= 10`
- B) `x < 10`
- C) `x >= 10`
- D) `x > -10`

**Question 5:** Multiple Choice: Why can `=` not be used where the `==` are?
- A) `=` assigns values, `==` compares values
- B) `=` compares values, `==` assigns values
- C) They do the same thing
- D) `=` is faster than `==`

**Question 6:** True/False: There are values of x and y that will make `(x > 0 or y < 20)` false.

**Variable scope:**
```python
global_var = "I'm global"

def my_function():
    local_var = "I'm local"
    print(global_var)  # Can access global
    global_var="test"
    print(global_var) 

my_function()
# print(local_var)  # Error: local_var not accessible here
```

**Question 7:** Multiple Choice: What error do you get if you try to print `local_var` outside the function?
- A) `TypeError`
- B) `NameError`
- C) `ValueError`
- D) `SyntaxError`

**Question 8:** Multiple Choice: After calling the function, what is the value of `global_var`?
- A) `"I'm global"`
- B) `"test"`
- C) `None`
- D) Error

**Question 9:** Multiple Choice: If you add `global global_var` to the first line of the function, what is the value of `global_var` after calling the function?
- A) `"I'm global"`
- B) `"test"`
- C) `None`
- D) Error

**Truthy and falsy values:**
```python
values = [0, 1, "", "hello", [], [1, 2], None, True, False]
for val in values:
    if val:
        print(f"{val} is truthy")
    else:
        print(f"{val} is falsy")
```
**Question 10:** Multiple Choice: Which of the following are truthy values?
- A) `1`
- B) `"hello"`
- C) `[1, 2]`
- D) All of the above


**Modulus operator and integer division:**
```python
minutes = 125
hours = minutes // 60      # Integer division: 2
remaining = minutes % 60   # Modulus: 5
print(f"{minutes} minutes = {hours} hours and {remaining} minutes")
```

**Question 11:** What value of `minutes` will produce 5 hours and 22 minutes?

**Recursion:**
```python
def countdown(n):
    if n <= 0:
        print("Done!")
    else:
        print(n)
        countdown(n - 1)

countdown(3)  # Output: 3, 2, 1, Done!
```

**Question 12:** Multiple Choice: What happens if you replace `n <= 0` with `False`?
- A) The function works the same way
- B) The function prints "Done!" immediately
- C) The function causes infinite recursion
- D) The function prints nothing 
---

