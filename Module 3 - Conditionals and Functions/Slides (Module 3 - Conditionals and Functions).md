# Module 3 - Conditionals and Functions
## Programming I
### CPSI 17503
#### University of Arkansas at Little Rock

---

## Review from Previous Modules

**Variables and Data Types**
- Remember that variables store different types of data
- `=` assigns values, `==` compares values
- Strings, integers, and floats behave differently

**Basic Operations**
- Mathematical operators: `+`, `-`, `*`, `/`, `//`, `%`
- String concatenation with `+`
- Type conversion with `int()`, `float()`, `str()`

**Print Statements**
- `print()` function displays output
- Can print multiple items separated by commas
- Remember proper syntax and parentheses

---

## Learning Objectives

By the end of this module, you will be able to:

1. **Define and call functions** with parameters and return values
2. **Use conditional statements** (`if`, `elif`, `else`) to control program flow
3. **Apply boolean logic** with relational and logical operators
4. **Understand variable scope** and distinguish between local and global variables
5. **Write recursive functions** that call themselves
6. **Use truthy and falsy values** to write cleaner conditional code
7. **Debug functions** using stack diagrams and tracebacks

---

## Key Terms

**Functions:**
- Function definition, header, body, parameter, argument
- Function object, local variable, return value

**Conditionals:**
- Boolean expression, relational operator, logical operator
- Conditional statement, condition, block, branch
- Chained conditional, nested conditional

**Recursion:**
- Recursive function, base case, infinite recursion
- Stack diagram, frame, traceback

**Scope:**
- Local scope, global scope, global keyword

**Truthy/Falsy:**
- Truthy values, falsy values, boolean context

---

## Content: Functions Fundamentals

**Function Definition Structure**
```python
def function_name(parameters):
    # Function body (indented)
    statements
    return value  # optional
```

**Key Components:**
- `def` keyword starts the definition
- Function name follows naming conventions
- Parameters in parentheses (can be empty)
- Body indented with 4 spaces
- Optional return statement

---

## Content: Function Examples

**Simple Function**
```python
def greet():
    print("Hello, World!")
```

**Function with Parameters**
```python
def greet(name):
    print(f"Hello, {name}!")
```

**Function with Return Value**
```python
def add(a, b):
    return a + b
```

**Calling Functions**
```python
greet()           # No arguments
greet("Alice")    # One argument
result = add(5, 3)  # Store return value
```

---

## Content: Parameters and Arguments

**Parameters vs Arguments**
- **Parameter**: Variable in function definition
- **Argument**: Value passed when calling function

**Example:**
```python
def print_twice(string):  # 'string' is parameter
    print(string)
    print(string)

print_twice("Hello")      # "Hello" is argument
```

**Multiple Parameters:**
```python
def repeat(word, n):
    print(word * n)

repeat("Spam ", 4)
```

---

## Content: Function Composition

**Functions Calling Functions**
```python
def repeat(word, n):
    print(word * n)

def first_two_lines():
    repeat("Spam ", 4)
    repeat("Spam ", 4)

def print_verse():
    first_two_lines()
    print("(Lovely Spam!)")
```

**Benefits:**
- Break complex tasks into smaller parts
- Reuse code
- Make programs easier to read and debug

---

## Content: Local Variables and Scope

**Local Variables**
- Variables created inside functions are **local**
- Only exist while function is running
- Are destroyed when function ends

**Example:**
```python
def cat_twice(part1, part2):
    cat = part1 + part2    # Local variable
    print_twice(cat)

# cat variable doesn't exist outside function
```

**Parameters are also local** to their function

---

## Content: Stack Diagrams

**Visualizing Function Calls**
- Each function call creates a **frame**
- Frames show parameters and local variables
- Stack shows calling order

**Example Stack:**
```
__main__: line1, line2
cat_twice: part1, part2, cat
print_twice: string
print: ?
```

**Reading Stack:**
- Bottom frame is currently running
- Each frame above called the one below it

---

## Content: Boolean Expressions

**Boolean Values**
- `True` and `False` are boolean literals
- Type is `bool`
- Used in conditional statements

**Relational Operators:**
```python
x == y    # Equal to
x != y    # Not equal to
x > y     # Greater than
x < y     # Less than
x >= y    # Greater than or equal
x <= y    # Less than or equal
```

---

## Content: Logical Operators

**Combining Boolean Values**
```python
# AND - both must be True
x > 0 and x < 10

# OR - at least one must be True
x % 2 == 0 or x % 3 == 0

# NOT - negates the value
not x > y
```

**Short-circuit Evaluation:**
- `and` stops at first `False`
- `or` stops at first `True`

---

## Content: if Statements

**Basic if Statement**
```python
if condition:
    # Code block runs if condition is True
    statements
```

**Example:**
```python
x = 5
if x > 0:
    print('x is positive')
```

**Structure:**
- `if` keyword
- Boolean expression (condition)
- Colon `:` at end of header
- Indented block of statements

---

## Content: else and elif Clauses

**if-else Statement**
```python
if x % 2 == 0:
    print('x is even')
else:
    print('x is odd')
```

**if-elif-else Statement**
```python
if x < y:
    print('x is less than y')
elif x > y:
    print('x is greater than y')
else:
    print('x and y are equal')
```

**Key Points:**
- `elif` means "else if"
- Only one branch executes
- `else` is optional but must be last

---

## Content: Nested Conditionals

**Conditionals Inside Conditionals**
```python
if x == y:
    print('x and y are equal')
else:
    if x < y:
        print('x is less than y')
    else:
        print('x is greater than y')
```

**Better Alternative:**
```python
if x == y:
    print('x and y are equal')
elif x < y:
    print('x is less than y')
else:
    print('x is greater than y')
```

**Avoid nested conditionals when possible**

---

## Content: Recursion Basics

**Recursive Functions**
- Functions that call themselves
- Powerful problem-solving technique
- Must have a **base case** to stop

**Example: Countdown**
```python
def countdown(n):
    if n <= 0:           # Base case
        print('Blastoff!')
    else:
        print(n)
        countdown(n-1)    # Recursive call
```

---

## Content: Recursion Examples

**Print String n Times**
```python
def print_n_times(string, n):
    if n > 0:                    # Base case
        print(string)
        print_n_times(string, n-1)  # Recursive call
```

**Key Requirements:**
1. **Base case** - condition that stops recursion
2. **Recursive case** - calls function with smaller problem
3. **Progress** - must move toward base case

---

## Content: Stack Diagrams for Recursion

**Recursive Function Stack**
- Each recursive call creates new frame
- Base case frame has no recursive calls
- Stack grows until base case is reached

**Example: countdown(3)**
```
countdown: n=3
countdown: n=2
countdown: n=1
countdown: n=0  # Base case
```

**Infinite Recursion:**
- Missing base case
- Never reaches stopping condition
- Causes runtime error

---

## Content: Truthy and Falsy Values

**Falsy Values (6 total):**
```python
False
None
0
0.0
""      # Empty string
[]      # Empty list
()      # Empty tuple
{}      # Empty dictionary
set()   # Empty set
```

**Everything else is Truthy**

---

## Content: Using Truthy/Falsy Values

**In Conditional Statements**
```python
name = "Alice"
if name:  # Same as: if name != ""
    print(f"Hello, {name}")

# Check if list is empty
if not my_list:
    print("List is empty")
```

**Default Values**
```python
def greet(name=None):
    if not name:  # If name is None or empty
        name = "Guest"
    print(f"Hello, {name}!")
```

---

## Content: Variable Scope

**Global vs Local Variables**
```python
# Global variable
total = 0

def add_to_total(n):
    global total      # Declare global
    total += n        # Modify global variable
    local_var = n     # Local variable
    return total

# local_var doesn't exist here
```

**Best Practices:**
- Pass data as parameters instead of using globals
- Use globals sparingly (constants, shared state)
- Keep functions independent

---

## Content: Common Scope Mistakes

**Mistake 1: Using Local Variables Outside Function**
```python
def create_name():
    first = "John"
    last = "Doe"
    return first + " " + last

result = create_name()
# print(first)  # Error! first is local
```

**Mistake 2: Forgetting global Declaration**
```python
counter = 0
def increment():
    # counter += 1  # Error! Python thinks counter is local
    global counter  # Fix: declare global
    counter += 1
```

---

## Content: Debugging Functions

**Tracebacks**
- Show function call stack when errors occur
- Bottom of traceback shows current function
- Each line shows calling function

**Stack Diagrams**
- Visual representation of function calls
- Show variables and their values
- Help understand program state

**Debugging Tips:**
- Start with working code
- Make small changes
- Test after each change
- Use print statements to see values

---

## Dos and Don'ts

**DO:**
- ✅ Use descriptive function names
- ✅ Include docstrings for complex functions
- ✅ Keep functions focused on single task
- ✅ Use parameters instead of global variables
- ✅ Always have a base case in recursive functions
- ✅ Use `elif` instead of nested `if` statements
- ✅ Check for truthy/falsy values in conditionals

**DON'T:**
- ❌ Forget the colon `:` after `if`, `elif`, `else`
- ❌ Mix tabs and spaces for indentation
- ❌ Create infinite recursion without base case
- ❌ Use `=` instead of `==` in comparisons
- ❌ Rely heavily on global variables
- ❌ Nest conditionals deeply
- ❌ Forget to handle edge cases

---

## Key Takeaways

**Functions are the foundation of programming:**
- Break complex problems into manageable pieces
- Make code reusable and maintainable
- Improve readability and debugging

**Conditionals control program flow:**
- `if` statements make decisions
- Boolean logic combines conditions
- Truthy/falsy values simplify conditionals

**Recursion solves problems elegantly:**
- Functions calling themselves
- Must have base case to stop
- Alternative to loops for some problems

**Scope matters:**
- Local variables keep functions independent
- Global variables should be used sparingly
- Understanding scope prevents bugs

---

## Further Explorations

- Explore advanced function concepts like decorators and lambda functions
- Study more complex conditional logic, such as switch-case statements in other languages
- Investigate different recursion techniques and their applications
- Learn about functional programming paradigms and how they differ from procedural programming
- Delve into error handling and exceptions in Python
- Experiment with creating and using modules and packages in Python
