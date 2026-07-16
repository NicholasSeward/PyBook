# Practice Assignment: Module 4 - Functions and Recursion

## Overview
Complete **3 problems total** - choose **1 from each section** below. Each section focuses on different aspects of functions and recursion.

## Instructions
- Choose **1 problem from Section 1** (Default Arguments)
- Choose **1 problem from Section 2** (Functions Calling Functions)  
- Choose **1 problem from Section 3** (Recursion)
- Use proper PEP 8 coding conventions
- Test your code with different inputs

## File Naming and Submission

### File Naming
Each problem should be a separate file:
- **Problem 1a:** `program1a.py` (User Profile Creator)
- **Problem 1b:** `program1b.py` (Shopping Cart Calculator)
- **Problem 2a:** `program2a.py` (Grade Analyzer)
- **Problem 2b:** `program2b.py` (Text Statistics)
- **Problem 3a:** `program3a.py` (Fibonacci Calculator)
- **Problem 3b:** `program3b.py` (Power Calculator)

### AI Disclaimer Requirement
**CRITICAL:** Each file must include an AI Disclaimer at the top. The autograder will look for this exact text and check the content after it.

**Examples of AI Disclaimers (choose the most appropriate or write your own):**

**No AI Use:**
```text
# AI Disclaimer: This code was written without the use of AI tools.
# Any assistance received was from course materials, textbooks, or instructor guidance only.
```

**Minimal AI Use (e.g., syntax help, debugging):**
```text
# AI Disclaimer: This code was written with minimal AI assistance.
# Used AI for: syntax checking and debugging only.
# Core logic and problem-solving approach are my own work.
```

**Moderate AI Use (e.g., code structure, algorithm suggestions):**
```text
# AI Disclaimer: This code was written with moderate AI assistance.
# Used AI for: code structure suggestions and algorithm guidance.
# I implemented the solutions and modified the AI suggestions to fit the requirements.
```

**Extensive AI Use (e.g., significant code generation):**
```text
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: code generation, debugging, and optimization.
# I reviewed, tested, and modified all AI-generated code to ensure it meets requirements.
```

**Unacceptable AI Use (e.g., "vibe coding" without learning):**
```text
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: complete code generation to pass autograder.
# I copied the code without understanding it, just to get a green checkmark.
# I didn't actually learn anything from this assignment.
```

**Your program code starts here...**

### Submission Process
1. Create your program files
2. Test your code with different inputs
3. Commit and push to GitHub
4. Submit your repository URL

**Example repository URL:** `https://github.com/Seward-Classes/practice-04-username`

---

## Section 1: Default Arguments (Choose 1)

### Problem 1a: Calculator with Default Arguments

Create a program that performs calculations with default arguments for optional parameters.

**Requirements:**
- Create a function `add_numbers(a, b, c=0)` with default argument for third number
- Create a function `multiply_numbers(a, b, c=1)` with default argument for third number
- Create a function `display_calculation(operation, a, b, c, result)` that shows the calculation
- Ask the user for two numbers
- Ask the user if they want to add a third number (optional)
- If they choose yes: ask for third number and use it in calculations
- If they choose no: use default values (0 for addition, 1 for multiplication)
- Display both addition and multiplication results

**Sample Output:**
```text
Enter first number: 5
Enter second number: 3
Add a third number? (y/n): y
Enter third number: 2
==========================================
CALCULATOR RESULTS
==========================================
Addition: 5 + 3 + 2 = 10
Multiplication: 5 * 3 * 2 = 30
==========================================
```

---

### Problem 1b: Rectangle/Square Area Calculator

Create a program that calculates area for rectangles and squares using default arguments.

**Requirements:**
- Create a function `rectangle_area(length, width=None)` with default argument for width
- If width is None: treat as a square (width = length)
- Ask the user for the length
- Ask the user if they want to enter a width (optional)
- If they choose yes: ask for width and calculate rectangle area
- If they choose no: use default (None) and calculate square area
- Display shape type and area

**Sample Output:**
```text
Enter length: 5
Enter width (or press Enter for square): 3
==========================================
SHAPE AREA CALCULATION
==========================================
Shape: Rectangle
Length: 5
Width: 3
Area: 15
==========================================
```

---

## Section 2: Functions Calling Functions (Choose 1)

### Problem 2a: Password Strength Checker

Create a program with two functions that work together to check password strength.

**Requirements:**
- Create a function `check_length(password)` that returns True if password is 8+ characters
- Create a function `has_uppercase(password)` that returns True if password contains uppercase letters
- Ask the user for a password
- Use both functions to determine if the password is strong
- Display password strength result

**Strength Rules:**
- Strong: 8+ characters AND has uppercase letters
- Weak: Less than 8 characters OR no uppercase letters

**Sample Output:**
```text
Enter a password: MySecret123
==========================================
PASSWORD STRENGTH CHECKER
==========================================
Password: MySecret123
Length OK: True
Has Uppercase: True
Password Strength: Strong
==========================================
```

---

### Problem 2b: Circle Calculator

Create a program with two functions where one function calls another to calculate circle properties.

**Requirements:**
- Create a function `calculate_area(radius)` that calculates circle area using π × radius²
- Create a function `calculate_circumference(radius)` that calculates circumference using 2 × π × radius
- Create a function `circle_info(radius)` that calls both functions and returns formatted information
- Ask the user for a radius
- Use the `circle_info` function to display area and circumference

**Formulas:**
- Area: π × radius² (use π = 3.14159)
- Circumference: 2 × π × radius

**Sample Output:**
```text
Enter radius: 5
==========================================
CIRCLE CALCULATOR
==========================================
Radius: 5
Area: 78.54
Circumference: 31.42
==========================================
```

---

## Section 3: Recursion (Choose 1)

### Problem 3a: Fibonacci Calculator

Create a program with a recursive function that calculates Fibonacci numbers.

**Requirements:**
- Create a recursive function `fibonacci(n)` that returns the nth Fibonacci number
- Include proper base cases (fibonacci(0) = 0, fibonacci(1) = 1)
- Ask the user for a positive integer
- Display the nth Fibonacci number
- Handle edge cases (n = 0, n = 1)

**Sample Output:**
```text
Enter a positive integer: 8
==========================================
FIBONACCI CALCULATOR
==========================================
The 8th Fibonacci number is: 13
==========================================
```

---

### Problem 3b: Power Calculator

Create a program with a recursive function that calculates powers.

**Requirements:**
- Create a recursive function `power(base, exponent)` that returns base^exponent
- Include proper base case (power(base, 0) = 1)
- Ask the user for base and exponent (both positive integers)
- Display the result
- Handle edge cases (exponent = 0, exponent = 1)

**Sample Output:**
```text
Enter base: 2
Enter exponent: 5
==========================================
POWER CALCULATOR
==========================================
2^5 = 32
==========================================
```

---

## Submission Checklist

- [ ] Completed 1 problem from Section 1 (Default Arguments)
- [ ] Completed 1 problem from Section 2 (Functions Calling Functions)
- [ ] Completed 1 problem from Section 3 (Recursion)
- [ ] Each file follows the naming convention
- [ ] Each file includes proper AI disclaimer
- [ ] Each file uses appropriate concepts for its section
- [ ] All files are committed and pushed to GitHub
- [ ] Repository URL is submitted on BlackBoard
---
