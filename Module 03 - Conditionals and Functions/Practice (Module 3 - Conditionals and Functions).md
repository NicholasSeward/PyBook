# Practice Assignment: Module 3 - Conditionals and Functions

## Overview
Complete **3 problems total** - choose **1 from each section** below. Each section focuses on different aspects of conditionals and functions.

## Instructions
- Choose **1 problem from Section 1** (Conditionals)
- Choose **1 problem from Section 2** (Functions)  
- Choose **1 problem from Section 3** (Recursion)
- Use proper PEP 8 coding conventions
- Test your code with different inputs

## File Naming and Submission

### File Naming
Each problem should be a separate file:
- **Problem 1a:** `program1a.py` (Weather Classifier)
- **Problem 1b:** `program1b.py` (Grade Calculator)
- **Problem 2a:** `program2a.py` (Math Helper)
- **Problem 2b:** `program2b.py` (Text Processor)
- **Problem 3a:** `program3a.py` (Countdown Timer)
- **Problem 3b:** `program3b.py` (Number Sum)

### AI Disclaimer Requirement
**CRITICAL:** Each file must include an AI Disclaimer at the top. The autograder will look for this exact text and check the content after it.

**Examples of AI Disclaimers (choose the most appropriate or write your own):**

**No AI Use:**
```python
# AI Disclaimer: This code was written without the use of AI tools.
# Any assistance received was from course materials, textbooks, or instructor guidance only.
```

**Minimal AI Use (e.g., syntax help, debugging):**
```python
# AI Disclaimer: This code was written with minimal AI assistance.
# Used AI for: syntax checking and debugging only.
# Core logic and problem-solving approach are my own work.
```

**Moderate AI Use (e.g., code structure, algorithm suggestions):**
```python
# AI Disclaimer: This code was written with moderate AI assistance.
# Used AI for: code structure suggestions and algorithm guidance.
# I implemented the solutions and modified the AI suggestions to fit the requirements.
```

**Extensive AI Use (e.g., significant code generation):**
```python
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: code generation, debugging, and optimization.
# I reviewed, tested, and modified all AI-generated code to ensure it meets requirements.
```

**Unacceptable AI Use (e.g., "vibe coding" without learning):**
```python
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
4. Verify GitHub Actions shows green checkmark ✅
5. Submit your repository URL

**Example repository URL:** `https://github.com/Seward-Classes/practice-03-username`

---

## Section 1: Conditionals (Choose 1)

### Problem 1a: Weather Classifier

Create a program that classifies weather conditions based on temperature and precipitation.

**Requirements:**
- Ask the user for temperature (in Fahrenheit) and precipitation amount (in inches)
- Use chained conditionals (if/elif/else) to classify weather
- Display the weather classification and appropriate clothing suggestion
- Use logical operators (and, or) in your conditions

**Classification Rules:**
- Hot & Dry: temp > 80 and precipitation < 0.1
- Hot & Wet: temp > 80 and precipitation >= 0.1
- Mild & Dry: 50 <= temp <= 80 and precipitation < 0.1
- Mild & Wet: 50 <= temp <= 80 and precipitation >= 0.1
- Cold & Dry: temp < 50 and precipitation < 0.1
- Cold & Wet: temp < 50 and precipitation >= 0.1

**Sample Output:**
```
Enter temperature (F): 85
Enter precipitation (inches): 0.05
==========================================
WEATHER CLASSIFICATION
==========================================
Temperature: 85°F
Precipitation: 0.05 inches
Classification: Hot & Dry
Recommendation: Wear light clothing and sunscreen
==========================================
```

---

### Problem 1b: Grade Calculator

Create a program that calculates letter grades and provides feedback using conditionals.

**Requirements:**
- Ask the user for their numerical score (0-100)
- Use chained conditionals (if/elif/else) for grade calculation
- Display the grade and personalized feedback message
- Handle invalid input (scores outside 0-100 range)

**Grading Scale:**
- A: 90-100 ("Excellent work!")
- B: 80-89 ("Good job!")
- C: 70-79 ("Keep working hard!")
- D: 60-69 ("You can improve!")
- F: 0-59 ("Let's work together to improve!")
- Invalid: < 0 or > 100 ("Please enter a valid score between 0 and 100")

**Sample Output:**
```
Enter your score (0-100): 85
==========================================
GRADE REPORT
==========================================
Score: 85
Grade: B
Feedback: Good job!
==========================================
```

---

## Section 2: Functions (Choose 1)

### Problem 2a: Math Helper

Create a program with multiple functions to perform mathematical operations.

**Requirements:**
- Create a function `add_numbers(a, b)` that returns the sum
- Create a function `multiply_numbers(a, b)` that returns the product
- Create a function `is_even(number)` that returns True if even, False if odd
- Create a function `calculate_average(a, b, c)` that returns the average
- Ask the user for two numbers
- Call all functions and display results
- Use the modulus operator (%) in the is_even function

**Sample Output:**
```
Enter first number: 10
Enter second number: 7
==========================================
MATH HELPER RESULTS
==========================================
Numbers: 10 and 7
Sum: 17
Product: 70
Is 10 even? True
Is 7 even? False
Average of 10, 7, and 0: 5.67
==========================================
```

---

### Problem 2b: Text Processor

Create a program with functions to analyze and process text.

**Requirements:**
- Create a function `count_characters(text)` that returns the length
- Create a function `count_words(text)` that returns the word count (assume words are separated by spaces)
- Create a function `is_long_text(text)` that returns True if text has more than 20 characters
- Create a function `format_text(text)` that returns the text in all caps
- Ask the user to enter a sentence
- Call all functions and display results
- Use the len() function and string methods

**Sample Output:**
```
Enter a sentence: Hello world from Python
==========================================
TEXT PROCESSING RESULTS
==========================================
Original text: Hello world from Python
Character count: 23
Word count: 4
Is long text? True
Formatted text: HELLO WORLD FROM PYTHON
==========================================
```

---

## Section 3: Recursion (Choose 1)

### Problem 3a: Countdown Timer

Create a program with a recursive function that counts down from a given number.

**Requirements:**
- Create a recursive function `countdown(n)` that prints numbers from n down to 1
- Include a proper base case to stop the recursion
- Ask the user for a starting number
- Display the countdown sequence
- Keep it simple - just count down and print each number

**Sample Output:**
```
Enter starting number: 5
==========================================
COUNTDOWN TIMER
==========================================
Starting countdown from 5:
5
4
3
2
1
Blastoff!
==========================================
```

---

### Problem 3b: Number Sum

Create a program with a recursive function that calculates the sum of numbers from 1 to n.

**Requirements:**
- Create a recursive function `sum_to_n(n)` that returns the sum of all numbers from 1 to n
- Include a proper base case to stop the recursion
- Ask the user for a positive integer
- Display the sum calculation
- Keep it simple - just add numbers from 1 to n

**Sample Output:**
```
Enter a positive integer: 5
==========================================
NUMBER SUM CALCULATOR
==========================================
Calculating sum from 1 to 5:
Sum = 1 + 2 + 3 + 4 + 5 = 15
==========================================
```

---

## Submission Checklist

- [ ] Completed 1 problem from Section 1 (Conditionals)
- [ ] Completed 1 problem from Section 2 (Functions)
- [ ] Completed 1 problem from Section 3 (Recursion)
- [ ] Each file follows the naming convention
- [ ] Each file includes proper AI disclaimer
- [ ] Each file uses appropriate concepts for its section
- [ ] Each file passes the autograde.py test locally
- [ ] All files are committed and pushed to GitHub
- [ ] GitHub Actions tab shows green checkmark ✅
- [ ] Repository URL is submitted on BlackBoard
---
