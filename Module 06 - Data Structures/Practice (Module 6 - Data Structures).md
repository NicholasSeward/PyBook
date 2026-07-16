# Practice Assignment: Module 6 - Data Structures

## Overview
Complete **3 problems total** - choose **1 from each section** below. Each section focuses on different aspects of data structures in Python.

## Instructions
- Choose **1 problem from Section 1** (Lists)
- Choose **1 problem from Section 2** (Dictionaries)  
- Choose **1 problem from Section 3** (Tuples)
- Use proper PEP 8 coding conventions
- Test your code with different inputs

## File Naming and Submission

### File Naming
Each problem should be a separate file:
- **Problem 1a:** `program1a.py` (Student Grade Manager)
- **Problem 1b:** `program1b.py` (Shopping List Manager)
- **Problem 2a:** `program2a.py` (Contact Book)
- **Problem 2b:** `program2b.py` (Word Frequency Counter)
- **Problem 3a:** `program3a.py` (Coordinate Calculator)
- **Problem 3b:** `program3b.py` (RGB Color Converter)

### AI Disclaimer Requirement
**CRITICAL:** Each file must include an AI Disclaimer at the top. The autograder will look for this exact text and check the content after it.

**Examples of AI Disclaimers (choose the most appropriate or write your own):**

**No AI Use:**
```
# AI Disclaimer: This code was written without the use of AI tools.
# Any assistance received was from course materials, textbooks, or instructor guidance only.
```

**Minimal AI Use (e.g., syntax help, debugging):**
```
# AI Disclaimer: This code was written with minimal AI assistance.
# Used AI for: syntax checking and debugging only.
# Core logic and problem-solving approach are my own work.
```

**Moderate AI Use (e.g., code structure, algorithm suggestions):**
```
# AI Disclaimer: This code was written with moderate AI assistance.
# Used AI for: code structure suggestions and algorithm guidance.
# I implemented the solutions and modified the AI suggestions to fit the requirements.
```

**Extensive AI Use (e.g., significant code generation):**
```
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: code generation, debugging, and optimization.
# I reviewed, tested, and modified all AI-generated code to ensure it meets requirements.
```

**Unacceptable AI Use (e.g., "vibe coding" without learning):**
```
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: complete code generation to pass autograder.
# I copied the code without understanding it, just to get a green checkmark.
# I didn't actually learn anything from this assignment.
```

**Your program code starts here...**

### Submission Process
1. Create your program files
2. Test your code thoroughly
3. Commit and push to GitHub
4. Submit your repository URL

**Example repository URL:** `https://github.com/Seward-Classes/practice-06-username`

---

## Section 1: Lists (Choose 1)

### Problem 1a: Student Grade Manager

Create a program that manages student grades using lists and list methods.

**Requirements:**
- Create a list to store student grades
- Allow the user to add grades to the list
- Use list methods: append(), insert(), remove(), pop()
- Calculate and display statistics (average, highest, lowest)
- Display the sorted list of grades
- Handle empty list cases

**Sample Output:**
```
==========================================
STUDENT GRADE MANAGER
==========================================
Enter grades (type 'done' to finish):
Enter grade: 85
Enter grade: 92
Enter grade: 78
Enter grade: 96
Enter grade: done

Grades entered: [85, 92, 78, 96]
Sorted grades: [78, 85, 92, 96]
Average: 87.75
Highest grade: 96
Lowest grade: 78
==========================================
```

---

### Problem 1b: Shopping List Manager

Create a program that manages a shopping list using lists and list operations.

**Requirements:**
- Create an empty shopping list
- Allow the user to add items to the list
- Allow the user to remove items from the list
- Display the current list
- Use list slicing to show first 3 items
- Use list methods: append(), remove(), index()
- Handle duplicate items and invalid operations

**Sample Output:**
```
==========================================
SHOPPING LIST MANAGER
==========================================
1. Add item
2. Remove item
3. View list
4. Exit
Enter choice: 1
Enter item to add: apples
Item added: apples

1. Add item
2. Remove item
3. View list
4. Exit
Enter choice: 1
Enter item to add: bread
Item added: bread

1. Add item
2. Remove item
3. View list
4. Exit
Enter choice: 3
Current shopping list: ['apples', 'bread']
First 3 items: ['apples', 'bread']
==========================================
```

---

## Section 2: Dictionaries (Choose 1)

### Problem 2a: Contact Book

Create a program that manages contacts using dictionaries.

**Requirements:**
- Create a dictionary to store contacts (name: phone_number)
- Allow the user to add new contacts
- Allow the user to look up contacts by name
- Allow the user to update existing contacts
- Display all contacts
- Use dictionary methods: get(), keys(), values(), items()
- Handle contact not found cases

**Sample Output:**
```
==========================================
CONTACT BOOK
==========================================
1. Add contact
2. Look up contact
3. Update contact
4. View all contacts
5. Exit
Enter choice: 1
Enter name: John Smith
Enter phone number: 555-1234
Contact added: John Smith - 555-1234

1. Add contact
2. Look up contact
3. Update contact
4. View all contacts
5. Exit
Enter choice: 2
Enter name to look up: John Smith
Contact found: John Smith - 555-1234

1. Add contact
2. Look up contact
3. Update contact
4. View all contacts
5. Exit
Enter choice: 4
All contacts:
John Smith: 555-1234
==========================================
```

---

### Problem 2b: Word Frequency Counter

Create a program that counts word frequencies in text using dictionaries.

**Requirements:**
- Ask the user to enter a sentence
- Split the sentence into words
- Use a dictionary to count word frequencies
- Display the word frequency results
- Use dictionary methods: get(), setdefault(), items()
- Handle case sensitivity (convert to lowercase)
- Sort results by frequency

**Sample Output:**
```
Enter a sentence: The quick brown fox jumps over the lazy dog
==========================================
WORD FREQUENCY COUNTER
==========================================
Sentence: The quick brown fox jumps over the lazy dog
Word frequencies:
the: 2
quick: 1
brown: 1
fox: 1
jumps: 1
over: 1
lazy: 1
dog: 1
Total unique words: 8
==========================================
```

---

## Section 3: Tuples (Choose 1)

### Problem 3a: Coordinate Calculator

Create a program that works with coordinate points using tuples.

**Requirements:**
- Create tuples to represent 2D coordinates (x, y)
- Allow the user to enter coordinates for two points
- Calculate the distance between the two points
- Calculate the midpoint between the two points
- Display coordinate information
- Use tuple unpacking to access x and y values
- Use tuple methods: count(), index()

**Sample Output:**
```
==========================================
COORDINATE CALCULATOR
==========================================
Enter coordinates for point 1:
X coordinate: 3
Y coordinate: 4
Point 1: (3, 4)

Enter coordinates for point 2:
X coordinate: 7
Y coordinate: 1
Point 2: (7, 1)

Distance between points: 5.0
Midpoint: (5.0, 2.5)
==========================================
```

---

### Problem 3b: RGB Color Converter

Create a program that works with RGB color values using tuples.

**Requirements:**
- Create tuples to represent RGB color values (red, green, blue)
- Allow the user to enter RGB values (0-255)
- Convert RGB to grayscale using the formula: (R + G + B) / 3
- Display the original RGB and grayscale values
- Use tuple unpacking to access color components
- Validate that RGB values are within 0-255 range
- Use tuple methods: count(), index()

**Sample Output:**
```
==========================================
RGB COLOR CONVERTER
==========================================
Enter RGB values (0-255):
Red: 255
Green: 128
Blue: 64
==========================================
Original RGB: (255, 128, 64)
Grayscale value: 149
Converted RGB: (149, 149, 149)
==========================================
```

---

## Submission Checklist

- [ ] Completed 1 problem from Section 1 (Lists)
- [ ] Completed 1 problem from Section 2 (Dictionaries)
- [ ] Completed 1 problem from Section 3 (Tuples)
- [ ] Each file follows the naming convention
- [ ] Each file includes proper AI disclaimer
- [ ] Each file uses appropriate concepts for its section
- [ ] Code is tested and working properly
- [ ] All files are committed and pushed to GitHub
- [ ] Repository URL is submitted on BlackBoard
---
