# Tutorial: Functions and Recursion

## Learning Objectives
- Design function interfaces with clear parameters and return values
- Use return values to pass data between functions
- Apply modular design principles to break complex problems into smaller functions
- Write recursive functions that return values and solve mathematical problems
- Use default arguments to make functions more flexible
- Apply function annotations to document parameter and return types
- Visualize call stacks to understand program execution flow
- Implement incremental development strategies for complex functions

---

## Experiment: Function Return Values

**Try this code:**
```python
def circle_area(radius):
    area = 3.14159 * radius**2
    return area

result = circle_area(5)
print(result)
```

**Question 1:** Write down the output.

**Now try this:**
```python
def circle_area(radius):
    area = 3.14159 * radius**2
    # Missing return statement

result = circle_area(5)
print(result)
```

**Question 2:** What does the second code print?
- A) `78.54`
- B) `None`
- C) `Error`
- D) `0`

---

## Experiment: Multiple Return Statements

**Type this:**
```python
def absolute_value(x):
    if x < 0:
        return -x
    else:
        return x

print(absolute_value(-5))
print(absolute_value(3))
print(absolute_value(0))
```

**Question 3:** What is the output of `absolute_value(-5)`?
- A) `-5`
- B) `5`
- C) `None`
- D) `Error`

**Try this broken version:**
```python
def absolute_value_wrong(x):
    if x < 0:
        return -x
    if x > 0:  # Missing else
        return x
    # No return for x == 0

print(absolute_value_wrong(0))
```

**Question 4:** What happens when you run the broken version?
- A) Prints `0`
- B) Prints `None`
- C) Prints `Error`
- D) Nothing happens

---

## Experiment: Boolean Functions

**Run this code:**
```python
def is_divisible(x, y):
    return x % y == 0

print(is_divisible(6, 2))
print(is_divisible(7, 2))
print(is_divisible(10, 3))
```

**Question 5:** How many `True` values are printed?
- A) `0`
- B) `1`
- C) `2`
- D) `3`

**Try this variation:**
```python
def is_even(n):
    return n % 2 == 0

if is_even(8):
    print("Even number")
else:
    print("Odd number")
```

**Question 6:** What does this code print?
- A) `Even number`
- B) `Odd number`
- C) `True`
- D) `8`

**Question 7:** Replace `8` with `8.01`. What does this print?
- A) `Even number`
- B) `Odd number`
- C) `True`
- D) `8.01`

---

## Experiment: Recursive Factorial

**Type this:**
```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(3))
```

**Question 8:** What is the output?
- A) `3`
- B) `6`
- C) `9`
- D) `Error`

**Question 9:** Change `factorial(3)` to `factorial(4)`. What is the new output?
- A) `12`
- B) `24`
- C) `36`
- D) `48`

**Question 10:** Change to `factorial(-1)`. What happens?
- A) Returns `-1`
- B) Returns `None`
- C) Causes infinite recursion
- D) Returns `0`

---

## Experiment: Default Arguments

**Type this:**
```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

print(greet("Alice"))
print(greet("Bob", "Good morning"))
```

**Question 11:** How many lines of output does this produce?
- A) `1`
- B) `2`
- C) `3`
- D) `4`

**Question 12:** Change a greet call to have no arguments. What happens?
- A) Prints `Hello, !`
- B) Prints `None`
- C) Causes a TypeError
- D) Prints `Hello, None!`

---

## Experiment: Function Annotations

**Run this code:**
```python
def calculate_area(length: float, width: float) -> float:
    return length * width

def process_user(name: str, age: int) -> str:
    return f"Hello {name}, you are {age} years old"

result1 = calculate_area(5.0, 3.0)
result2 = process_user("Alice", 25)
print(result1)
print(result2)
```

**Question 13:** What is the output of `result1`?
- A) `8.0`
- B) `15.0`
- C) `53.0`
- D) `Error`

**Question 14:** Change `calculate_area(5.0, 3.0)` to `calculate_area(4, 6)`. What is the output now?
- A) `10.0`
- B) `24.0`
- C) `46.0`
- D) `Error`

**Question 15:** Are type annotations used at runtime?
- A) Yes, they enforce types
- B) No, they are only hints
- C) Yes, but only for validation
- D) No, they cause errors

---

## Experiment: Call Stack Visualization

**Run this code:**
```python
def function_a():
    print("Function A starts")
    function_b()
    print("Function A ends")

def function_b():
    print("Function B starts")
    function_c()
    print("Function B ends")

def function_c():
    print("Function C starts")
    print("Function C ends")

function_a()
```

**Question 16:** How many lines of output does this produce?
- A) `4`
- B) `5`
- C) `6`
- D) `7`

**Question 17:** What is the second line of output?
- A) `Function A starts`
- B) `Function B starts`
- C) `Function C starts`
- D) `Function C ends`

---

## Experiment: Input Validation

**Type this:**
```python
def factorial(n):
    if not isinstance(n, int):
        print('factorial is only defined for integers.')
        return None
    elif n < 0:
        print('factorial is not defined for negative numbers.')
        return None
    elif n == 0:
        return 1
    else:
        return n * factorial(n-1)

print(factorial(3))
print(factorial(-2))
print(factorial("hello"))
```

**Question 18:** How many lines of output does this produce?
- A) `3`
- B) `4`
- C) `5`
- D) `6`

**Question 19:** What is the output of `factorial(-2)`?
- A) `2`
- B) `None`
- C) `Error`
- D) `-2`