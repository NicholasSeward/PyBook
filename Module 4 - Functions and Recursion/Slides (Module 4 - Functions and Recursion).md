# Module 4 - Functions and Recursion
## Programming I
### CPSI 17503
#### University of Arkansas at Little Rock

---

## Review from Previous Modules

**Function Basics**
- Functions are defined with `def` keyword
- Parameters receive arguments when called
- Functions can call other functions
- Variables inside functions are local

**Conditionals and Control Flow**
- `if`, `elif`, `else` statements control execution
- Boolean expressions use `and`, `or`, `not`
- Truthy/falsy values simplify conditionals

**Basic Recursion**
- Functions can call themselves
- Must have base case to stop recursion
- Stack diagrams show function call sequence

---

## Learning Objectives

By the end of this module, you will be able to:

1. **Design function interfaces** with clear parameters and return values
2. **Use return values** to pass data between functions
3. **Apply modular design principles** to break complex problems into smaller functions
4. **Write recursive functions** that return values and solve mathematical problems
5. **Use default arguments** to make functions more flexible
6. **Apply function annotations** to document parameter and return types
7. **Visualize call stacks** to understand program execution flow
8. **Implement incremental development** strategies for complex functions

---

## Key Terms

**Function Design:**
- Interface design, encapsulation, generalization
- Function signature, docstring, multiline string
- Precondition, postcondition, input validation

**Return Values:**
- Return value, return statement, pure function
- Dead code, incremental development, scaffolding

**Recursion:**
- Recursive function, base case, recursive case
- Turing complete, leap of faith

**Modular Design:**
- Modular design, decomposition, refactoring
- Call stack, stack frame, LIFO principle

---

## Content: Function Interfaces and Design

**Interface vs Implementation**
- **Interface**: How function is used (name, parameters, purpose)
- **Implementation**: How function accomplishes its task

**Example:**
```python
def circle(radius):
    """Draw a circle with given radius."""
    circumference = 2 * math.pi * radius
    n = 30
    length = circumference / n
    polygon(n, length)
```

**Interface Design Principles:**
- Clear, descriptive function names
- Logical parameter order
- Well-documented purpose
- Consistent with similar functions

---

## Content: Encapsulation and Generalization

**Encapsulation**
- Wrapping code in a function with a descriptive name
- Makes code reusable and easier to understand

**Example:**
```python
def square():
    for i in range(4):
        forward(50)
        left(90)

# Now we can call square() instead of repeating code
```

**Generalization**
- Adding parameters to make functions more flexible
- Replacing specific values with variables

**Example:**
```python
def square(length):  # Added length parameter
    for i in range(4):
        forward(length)  # Use parameter instead of hardcoded 50
        left(90)
```

---

## Content: Function Composition and Refactoring

**Functions Calling Functions**
```python
def polyline(n, length, angle):
    for i in range(n):
        forward(length)
        left(angle)

def polygon(n, length):
    angle = 360.0 / n
    polyline(n, length, angle)  # Uses polyline

def arc(radius, angle):
    arc_length = 2 * math.pi * radius * angle / 360
    n = 30
    length = arc_length / n
    step_angle = angle / n
    polyline(n, length, step_angle)  # Uses polyline
```

**Benefits:**
- Reuse existing code
- Break complex tasks into smaller parts
- Easier to test and debug

---

## Content: Return Values

**Functions with Return Values**
```python
def circle_area(radius):
    area = math.pi * radius**2
    return area  # Returns the calculated value

# Can assign return value to variable
result = circle_area(5)
print(result)  # 78.54...

# Can use in expressions
total_area = circle_area(3) + circle_area(4)
```

**Return Statement**
- `return` immediately ends function execution
- Returns value to caller
- Function without `return` returns `None`

---

## Content: Pure Functions

**Pure Functions**
- Functions that only return values
- No side effects (printing, drawing, etc.)
- Easier to test and reason about

**Example:**
```python
# Pure function - only returns value
def add(a, b):
    return a + b

# Not pure - has side effect (printing)
def add_and_print(a, b):
    result = a + b
    print(f"{a} + {b} = {result}")
    return result
```

**Benefits:**
- Predictable behavior
- Can be used in expressions
- Easier to test
- Can be composed together

---

## Content: Return Values and Conditionals

**Multiple Return Statements**
```python
def absolute_value(x):
    if x < 0:
        return -x    # Return negative of x
    else:
        return x     # Return x as-is
```

**Important Rules:**
- Every code path must reach a `return` statement
- Code after `return` is **dead code** (never executed)
- Function ends immediately when `return` is reached

**Common Mistake:**
```python
def absolute_value_wrong(x):
    if x < 0:
        return -x
    if x > 0:        # Missing else - what if x == 0?
        return x
    # Function ends without return if x == 0
```

---

## Content: Boolean Functions

**Functions Returning True/False**
```python
def is_divisible(x, y):
    if x % y == 0:
        return True
    else:
        return False

# More concise version
def is_divisible(x, y):
    return x % y == 0  # Returns boolean result directly
```

**Using Boolean Functions**
```python
if is_divisible(6, 2):
    print('6 is divisible by 2')

# Don't need to compare with True
if is_divisible(6, 2) == True:  # Unnecessary comparison
    print('6 is divisible by 2')
```

---

## Content: Recursion with Return Values

**Factorial Function**
```python
def factorial(n):
    if n == 0:
        return 1                    # Base case
    else:
        recurse = factorial(n-1)    # Recursive call
        return n * recurse          # Return result
```

**How It Works:**
1. `factorial(3)` calls `factorial(2)`
2. `factorial(2)` calls `factorial(1)`
3. `factorial(1)` calls `factorial(0)`
4. `factorial(0)` returns `1`
5. Each function multiplies by its `n` and returns

**Result: 3 × 2 × 1 × 1 = 6**

---

## Content: Fibonacci Sequence

**Recursive Definition**
```python
def fibonacci(n):
    if n == 0:
        return 0                    # Base case 1
    elif n == 1:
        return 1                    # Base case 2
    else:
        return fibonacci(n-1) + fibonacci(n-2)  # Recursive case
```

**Mathematical Definition:**
- F(0) = 0
- F(1) = 1
- F(n) = F(n-1) + F(n-2)

**Example:**
- F(2) = F(1) + F(0) = 1 + 0 = 1
- F(3) = F(2) + F(1) = 1 + 1 = 2
- F(4) = F(3) + F(2) = 2 + 1 = 3

---

## Content: The Leap of Faith

**Understanding Recursion**
- Don't try to follow every recursive call
- Assume recursive calls work correctly
- Focus on the current function's logic

**Example with factorial:**
```python
def factorial(n):
    if n == 0:
        return 1
    else:
        # Assume factorial(n-1) returns correct value
        return n * factorial(n-1)
```

**Key Insight:**
- If you can compute factorial(n-1), you can compute factorial(n)
- Base case handles the stopping condition
- Recursive case builds on smaller solutions

---

## Content: Input Validation

**Checking Parameters**
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
```

**Benefits:**
- Prevents infinite recursion
- Provides clear error messages
- Makes functions more robust
- Documents function requirements

---

## Content: Incremental Development

**Step-by-Step Approach**
1. Start with working program (even if incomplete)
2. Make small changes
3. Test after every change
4. Add debugging output as needed

**Example: Distance Function**
```python
# Step 1: Always return 0
def distance(x1, y1, x2, y2):
    return 0.0

# Step 2: Calculate differences
def distance(x1, y1, x2, y2):
    dx = x2 - x1
    dy = y2 - y1
    print('dx is', dx)  # Debug output
    print('dy is', dy)
    return 0.0

# Step 3: Complete calculation
def distance(x1, y1, x2, y2):
    dx = x2 - x1
    dy = y2 - y1
    dsquared = dx**2 + dy**2
    result = math.sqrt(dsquared)
    return result
```

---

## Content: Modular Design Principles

**Breaking Problems Down**
```python
def analyze_grades(scores):
    """Main function that coordinates other functions."""
    average = calculate_average(scores)
    highest = find_highest(scores)
    lowest = find_lowest(scores)
    
    return {
        'average': average,
        'highest': highest,
        'lowest': lowest
    }

def calculate_average(scores):
    """Calculate average of scores."""
    if not scores:
        return 0
    return sum(scores) / len(scores)

def find_highest(scores):
    """Find highest score."""
    if not scores:
        return None
    return max(scores)
```

**Benefits:**
- Each function has single responsibility
- Easier to test individual functions
- Code can be reused in different contexts

---

## Content: Call Stack Visualization

**Understanding Function Calls**
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
```

**Call Stack (when function_c is running):**
```
┌─────────────────┐ ← TOP (currently running)
│ Function C      │
├─────────────────┤
│ Function B      │ (waiting for C to finish)
├─────────────────┤
│ Function A      │ (waiting for B to finish)
├─────────────────┤
│ Main Program    │ (waiting for A to finish)
└─────────────────┘ ← BOTTOM
```

---

## Content: Stack Diagrams for Recursion

**Recursive Function Stack**
```python
def factorial(n):
    if n == 0:
        return 1
    else:
        recurse = factorial(n-1)
        return n * recurse
```

**Stack for factorial(3):**
```
factorial: n=3, recurse=2, result=6
factorial: n=2, recurse=1, result=2
factorial: n=1, recurse=1, result=1
factorial: n=0, result=1  # Base case
```

**Key Points:**
- Each recursive call creates new frame
- Base case frame has no recursive calls
- Return values flow back up the stack

---

## Content: Default Arguments

**Making Parameters Optional**
```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

# Using default
print(greet("Alice"))           # Hello, Alice!

# Overriding default
print(greet("Bob", "Good morning"))  # Good morning, Bob!
```

**Rules:**
- Default arguments must come after required arguments
- Use `None` as default for mutable objects
- Choose sensible, descriptive defaults

---

## Content: Default Arguments Examples

**Multiple Default Arguments**
```python
def create_user(username, is_active=True, role="user"):
    user = {"username": username}
    
    if is_active:
        user["status"] = "active"
    else:
        user["status"] = "inactive"
    
    user["role"] = role
    return user

# Test different combinations
print(create_user("alice123"))                    # Uses all defaults
print(create_user("bob456", False))               # Override is_active
print(create_user("charlie789", True, "admin"))   # Override both
```

**Common Pattern:**
```python
def process_data(data, filter_func=None, sort_key=None, limit=None):
    # Use None to indicate "no operation"
    if filter_func:
        data = [item for item in data if filter_func(item)]
    # ... rest of function
```

---

## Content: Function Annotations

**Type Hints and Documentation**
```python
def calculate_area(length: float, width: float) -> float:
    """Calculate the area of a rectangle."""
    return length * width

# length: float means parameter should be float
# -> float means function returns float
```

**Different Annotation Types**
```python
def process_user(name: str, age: int) -> str:
    return f"Hello {name}, you are {age} years old"

def get_even_numbers(numbers: list) -> list:
    return [num for num in numbers if num % 2 == 0]

def create_profile(name: str, age: int) -> dict:
    return {"name": name, "age": age, "status": "active"}
```

---

## Content: Docstrings and Documentation

**Function Documentation**
```python
def polyline(n, length, angle):
    """Draws line segments with the given length and angle between them.
    
    n: integer number of line segments
    length: length of the line segments
    angle: angle between segments (in degrees)
    """    
    for i in range(n):
        forward(length)
        left(angle)
```

**Docstring Guidelines:**
- Explain what function does (not how)
- Describe each parameter's purpose and type
- Use triple quotes for multiline strings
- Keep descriptions concise and clear

---

## Content: Development Plan

**Encapsulation and Generalization Process**
1. Start with small working program (no functions)
2. Identify coherent pieces and encapsulate in functions
3. Generalize functions by adding parameters
4. Repeat until you have working function set
5. Look for refactoring opportunities

**Example Progression:**
```python
# Step 1: Working program
make_turtle()
for i in range(4):
    forward(50)
    left(90)

# Step 2: Encapsulate
def square():
    for i in range(4):
        forward(50)
        left(90)

# Step 3: Generalize
def square(length):
    for i in range(4):
        forward(length)
        left(90)
```

---

## Content: Preconditions and Postconditions

**Function Contracts**
```python
def polyline(n, length, angle):
    """Draws line segments with given length and angle.
    
    Preconditions:
    - n must be positive integer
    - length must be positive number
    - angle must be number (in degrees)
    
    Postconditions:
    - Turtle draws n line segments
    - Turtle ends at starting position
    - Turtle faces original direction
    """
    for i in range(n):
        forward(length)
        left(angle)
```

**Benefits:**
- Clear expectations for function users
- Help with debugging
- Document function behavior
- Establish responsibility boundaries

---

## Dos and Don'ts

**DO:**
- ✅ Use descriptive function names that explain purpose
- ✅ Write docstrings for all functions
- ✅ Start with simple working code and build up
- ✅ Use incremental development for complex functions
- ✅ Validate input parameters when appropriate
- ✅ Use default arguments for optional parameters
- ✅ Break complex problems into smaller functions
- ✅ Test functions after each small change

**DON'T:**
- ❌ Write functions that do multiple unrelated tasks
- ❌ Skip input validation for critical functions
- ❌ Use mutable objects as default arguments
- ❌ Write recursive functions without base cases
- ❌ Forget to handle edge cases
- ❌ Write functions that are too long or complex
- ❌ Ignore return values from function calls
- ❌ Create functions with too many parameters

---

## Key Takeaways

**Function Design is Fundamental:**
- Good interfaces make functions easy to use
- Encapsulation and generalization improve code quality
- Modular design breaks complex problems into manageable pieces

**Return Values Enable Composition:**
- Functions can pass data between each other
- Pure functions are easier to test and reason about
- Return values make functions more flexible

**Recursion Solves Problems Elegantly:**
- Recursive functions can solve complex problems simply
- Base cases are essential for stopping recursion
- The "leap of faith" helps understand recursive logic

**Development Process Matters:**
- Incremental development reduces debugging time
- Small changes are easier to test and debug
- Refactoring improves code without changing behavior

---

## Further Explorations

- Investigate advanced recursion techniques, such as tail recursion and memoization, to optimize recursive solutions.
- Explore the use of higher-order functions and how they can be used to create more abstract and reusable code.
- Study the concept of closures and how they can be used to maintain state in a functional programming context.
- Delve into the use of decorators in Python to modify or enhance the behavior of functions.
- Learn about functional programming paradigms and how they differ from procedural and object-oriented programming.
- Experiment with creating and using Python modules and packages to organize and reuse code effectively.
- Explore the use of type hints and static type checking to improve code reliability and maintainability.




