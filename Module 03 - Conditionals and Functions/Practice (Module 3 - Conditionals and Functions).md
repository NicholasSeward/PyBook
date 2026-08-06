# Practice Assignment: Module 3 - Conditionals and Functions

## Overview

This assignment provides an opportunity to apply the concepts covered in this module by writing Python programs using conditionals and functions.

You will complete:

- One problem from Section 1 – Conditionals
- One problem from Section 2 – Functions

---

## ▶️ Start Here

If this is your first GitHub Classroom assignment or you need a refresher, begin by watching the assignment walkthrough below.

The video demonstrates how to:

- Access the GitHub Classroom assignment
- Navigate the repository
- Complete and submit your work
- Troubleshoot common issues

*[Insert assignment walkthrough video]*

---

## 🚀 GitHub Classroom

After watching the walkthrough, open the GitHub Classroom assignment using the link below.

**GitHub Classroom Assignment**

[INSERT ASSIGNMENT LINK]

Starter template (Codespaces / Python): `programming-1`

> WARNING: Submit the **repository** URL in the LMS (Blackboard), not a Codespaces / `github.dev` link (those are private to you).

---

## 📋 Assignment Requirements

Complete:

- One problem from Section 1 – Conditionals
- One problem from Section 2 – Functions
- Follow PEP 8 coding conventions
- Test your code with multiple inputs
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

---

## 📁 File Naming

Each problem should be saved as a separate Python file.

| Problem | File Name |
|---------|-----------|
| Weather Classifier | `program1a.py` |
| Grade Calculator | `program1b.py` |
| Math Helper | `program2a.py` |
| Text Processor | `program2b.py` |

---

## 🤖 AI Usage Disclosure

**CRITICAL:** Each Python file must begin with an AI Disclaimer. The autograder will look for this exact text and check the content after it.

Choose the statement that best reflects how AI was (or was not) used while completing your assignment.

### Examples of AI Disclaimers (choose the most appropriate or write your own)

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

Your program code starts here...

---

## 💻 Programming Problems

### Section 1 - Conditionals (Choose One)

#### Problem 1a: Weather Classifier

Create a program that classifies weather conditions based on temperature and precipitation.

**Requirements:**

- Ask the user for temperature (in Fahrenheit) and precipitation amount (in inches)
- Use chained conditionals (`if`/`elif`/`else`) to classify weather
- Display the weather classification and appropriate clothing suggestion
- Use logical operators (`and`, `or`) in your conditions

**Classification Rules:**

- Hot & Dry: temp > 80 and precipitation < 0.1
- Hot & Wet: temp > 80 and precipitation >= 0.1
- Mild & Dry: 50 <= temp <= 80 and precipitation < 0.1
- Mild & Wet: 50 <= temp <= 80 and precipitation >= 0.1
- Cold & Dry: temp < 50 and precipitation < 0.1
- Cold & Wet: temp < 50 and precipitation >= 0.1

**Sample Output:**

```text
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

#### Problem 1b: Grade Calculator

Create a program that calculates letter grades and provides feedback using conditionals.

**Requirements:**

- Ask the user for their numerical score (0-100)
- Use chained conditionals (`if`/`elif`/`else`) for grade calculation
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

```text
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

### Section 2 - Functions (Choose One)

#### Problem 2a: Math Helper

Create a program with multiple functions to perform mathematical operations.

**Requirements:**

- Create a function `add_numbers(a, b)` that returns the sum
- Create a function `multiply_numbers(a, b)` that returns the product
- Create a function `is_even(number)` that returns `True` if even, `False` if odd
- Create a function `calculate_average(a, b)` that returns the average
- Ask the user for two numbers
- Call all functions and display results
- Use the modulus operator (`%`) in the `is_even` function

**Sample Output:**

```text
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
Average of 10 and 7: 8.5
==========================================
```

#### Problem 2b: Text Processor

Create a program with functions to analyze and process text.

**Requirements:**

- Create a function `count_characters(text)` that returns the length
- Create a function `count_words(text)` that returns the word count (assume words are separated by spaces)
- Create a function `is_long_text(text)` that returns `True` if text has more than 20 characters
- Create a function `format_text(text)` that returns the text in all caps
- Ask the user to enter a sentence
- Call all functions and display results
- Use the `len()` function and string methods

**Sample Output:**

```text
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

## 📤 Submission Instructions

1. Complete both programming problems.
2. Commit and push your files to GitHub.
3. Copy your GitHub repository URL.
4. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Completed one Conditionals problem
- ☐ Completed one Functions problem
- ☐ Correct file names
- ☐ AI Disclaimer included
- ☐ Code follows PEP 8 conventions
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
