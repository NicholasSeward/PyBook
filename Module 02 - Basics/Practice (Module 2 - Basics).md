# Practice Assignment: Module 2 - Basics

## Overview
Complete **3 out of 4** problems below. Each problem focuses on practical applications of Python basics including variables, types, arithmetic operations, type conversion, and f-string formatting.

## Instructions
- Choose any 3 problems to complete
- Use proper PEP 8 coding conventions
- Test your code with different inputs

## File Naming and Submission

### File Naming
Each problem should be a separate file:
- **Problem 1:** `program1.py` (Circle Calculator)
- **Problem 2:** `program2.py` (Temperature Converter)
- **Problem 3:** `program3.py` (Simple Calculator)
- **Problem 4:** `program4.py` (Shopping Cart)
- **Problem 5:** `program5.py` (String Analysis)

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
2. Test with autograde.py
3. Commit and push to GitHub
4. Verify GitHub Actions shows green checkmark
5. Submit your repository URL

**Example repository URL:** `https://github.com/Seward-Classes/practice-01-username`

---

## Problem 1: Circle Calculator

Create a program that calculates the area and circumference of a circle given its radius.

**Requirements:**
- Ask the user for the radius (as a float)
- Calculate area using: A = πr²
- Calculate circumference using: C = 2πr
- Display results formatted to 2 decimal places
- Use the math module for π

**Sample Output:**
```text
Enter the radius of the circle: 5.0
Area: 78.54 square units
Circumference: 31.42 units
```

---

## Problem 2: Temperature Converter

Create a program that converts Celsius to Fahrenheit and Kelvin.

**Requirements:**
- Ask the user for a temperature in Celsius
- Convert to Fahrenheit: F = (C × 9/5) + 32
- Convert to Kelvin: K = C + 273.15
- Display all three temperatures formatted to 1 decimal place

**Sample Output:**
```text
Enter temperature in Celsius: 25
25.0°C = 77.0°F = 298.2K
```

---

## Problem 3: Simple Calculator

Create a program that performs all four basic arithmetic operations.

**Requirements:**
- Ask the user for two numbers
- Perform all four operations: addition, subtraction, multiplication, division
- Display all results formatted to 2 decimal places

**Sample Output:**
```text
Enter first number: 10
Enter second number: 3
==========================================
CALCULATION RESULTS
==========================================
10.00 + 3.00 = 13.00
10.00 - 3.00 = 7.00
10.00 * 3.00 = 30.00
10.00 / 3.00 = 3.33
==========================================
```

---

## Problem 4: Shopping Cart

Create a program that calculates the total cost of items.

**Requirements:**
- Ask for item name, price, and quantity
- Calculate item total (price × quantity)
- Ask for tax rate as a percentage
- Calculate tax and final total
- Display formatted receipt

**Sample Output:**
```text
Enter item name: Apples
Enter price: 2.50
Enter quantity: 3
Enter tax rate (%): 8.5
==========================================
RECEIPT
==========================================
Apples: 3 x $2.50 = $7.50
Subtotal: $7.50
Tax (8.5%): $0.64
Total: $8.14
==========================================
```

---

## Problem 5: String Analysis Tool

Create a program that analyzes text input using the len() function.

**Requirements:**
- Ask the user to enter a sentence
- Calculate and display the number of characters using len()

**Sample Output:**
```text
Enter some text: Hello World!
==========================================
TEXT ANALYSIS REPORT
==========================================
Original text: Hello World!
Number of characters: 12
==========================================
```

---

## Submission Checklist

- [ ] Each completed problem has its own file (program1.py, program2.py, etc.)
- [ ] Each file follows the naming convention
- [ ] Each file passes the autograde.py test locally
- [ ] All files are committed and pushed to GitHub
- [ ] GitHub Actions tab shows green checkmark
- [ ] Repository URL is submitted on BlackBoard
---
