# Module 1 - Intro
## Programming I
### CPSI 17503
#### University of Arkansas at Little Rock

---

## Learning Objectives

- Understand what programming is and why we learn it
- Learn the difference between compiled and interpreted languages
- Write your first Python program (Hello World)
- Understand basic Python syntax and arithmetic operations
- Learn about IDEs and development tools
- Understand version control basics with Git and GitHub
- Learn about number systems (binary, decimal, hexadecimal)
- Understand formal vs natural languages
- Develop a debugging mindset

---

## Key Terms

- **Programming**: Giving instructions to a computer in a language it understands
- **Programming Language**: Formal language designed to express computations
- **Interpreter**: Program that reads and executes code line by line
- **Compiler**: Program that translates source code to machine code
- **IDE**: Integrated Development Environment
- **Version Control**: System for tracking changes in code
- **Repository**: Storage location for code and project files
- **Formal Language**: Precise language with exact rules
- **Natural Language**: Human languages that evolved naturally
- **Debugging**: Process of finding and fixing errors in code

---

## What is Programming?

Programming is giving instructions to a computer in a language it can understand.

**Think of it like:**
- Writing a recipe for a computer to follow
- Teaching someone who is very literal and precise
- Breaking down complex tasks into simple steps

**Why learn programming?**
- Solve problems systematically
- Automate repetitive tasks
- Create tools and applications
- Think logically and analytically
- Understand how technology works

---

## Programming as a Way of Thinking

Programming combines the best features of:

**Mathematics:**
- Use formal languages to express ideas
- Work with precise, unambiguous rules
- Solve problems step by step

**Engineering:**
- Design systems and components
- Evaluate trade-offs between solutions
- Build things that work reliably

**Science:**
- Observe system behavior
- Form hypotheses about problems
- Test predictions systematically

---

## Formal vs Natural Languages

**Natural Languages (English, Spanish, French):**
- Evolved naturally over time
- Full of ambiguity and context
- Use redundancy to avoid misunderstandings
- Rich in idioms and metaphors
- Flexible and forgiving

**Formal Languages (Programming, Math):**
- Designed by people for specific purposes
- Nearly or completely unambiguous
- Concise and precise
- Mean exactly what they say
- Every detail matters

---

## Why Formal Languages Matter

**In programming:**
- Every program has exactly one meaning
- Small errors can break everything
- Structure is more important than reading order
- Details like spelling and punctuation are critical

**Examples of formal language rules:**
- `print("Hello")` ≠ `Print("Hello")`
- `2 + 3 * 4` ≠ `(2 + 3) * 4`
- `"Hello"` ≠ `'Hello'` (but both work)

---

## Compiled vs Interpreted Languages

**Compiled (C, C++, Rust):**
- Code translated to machine language before running
- Faster execution, catches errors early
- Must recompile after changes

**Interpreted (Python, JavaScript):**
- Code read and executed line by line
- Slower but easier to test and modify
- Portable across different systems

---

## Why Python?

- **Beginner-friendly**: Clear, readable syntax
- **Interpreted**: No compilation step needed
- **Versatile**: Web, data science, AI, automation
- **Large community**: Lots of help and libraries available
- **Industry standard**: Used by Google, Netflix, NASA

---

## Your First Program: Hello World

```python
print("Hello, World!")
```

**What this does:**
- `print()` is a function that displays text
- `"Hello, World!"` is a string (text in quotes)
- This confirms your Python environment works

---

## Comments in Python

**Single-line comments:**
```python
# This is a comment
print("Hello")  # Comment on same line
```

**Multi-line comments:**
```python
"""
This is a multi-line comment
Useful for longer explanations
"""
```

**Good comments explain WHY, not WHAT**

---

## Basic Arithmetic

**Operators:**
- `+` Addition: `5 + 3 = 8`
- `-` Subtraction: `10 - 4 = 6`
- `*` Multiplication: `6 * 7 = 42`
- `/` Division: `15 / 3 = 5.0`
- `//` Integer division: `15 // 3 = 5`
- `**` Exponentiation: `2 ** 3 = 8`

---

## Numbers in Python

**Two main types:**
- **Integers** (`int`): Whole numbers like `5`, `-3`, `1000`
- **Floating-point** (`float`): Decimal numbers like `3.14`, `-2.5`

**Examples:**
```python
type(5)      # int
type(3.14)   # float
type(5.0)    # float
```

---

## Strings

**Strings** are sequences of characters (text):
```python
"Hello, World!"
'Python Programming'
"123"  # This is text, not a number!
```

**String operations:**
- `+` concatenates (joins) strings
- `*` repeats strings
- `len()` gives string length

---

## Functions

**Functions** are reusable blocks of code:
```python
print("Hello")           # Built-in function
len("Python")           # Returns 6
round(3.7)              # Returns 4
abs(-5)                 # Returns 5
```

**Calling functions:** Always use parentheses `()`

---

## Expressions

**Expressions** combine values and operators:
```python
2 + 3 * 4        # Order of operations: 14
(2 + 3) * 4      # Parentheses first: 20
"Hello" + " " + "World"  # String concatenation
```

**Every expression has a value and a type**

---

## Types and Type Conversion

**Converting between types:**
```python
int("123")       # String to integer: 123
float(42)        # Integer to float: 42.0
str(99)          # Number to string: "99"
```

**Type checking:**
```python
type(42)         # <class 'int'>
type("42")       # <class 'str'>
```

---

## Number Systems

**Decimal (Base 10):** What we use every day
- Digits: 0-9
- Example: 374 = (3×10²) + (7×10¹) + (4×10⁰)

**Binary (Base 2):** How computers store data
- Digits: 0, 1
- Example: 1011₂ = 8 + 0 + 2 + 1 = 11

**Hexadecimal (Base 16):** Shorthand for binary
- Digits: 0-9, A-F
- Example: 2F₁₆ = 47

---

## Debugging Mindset

**What is debugging?**
- Finding and fixing errors in your code
- A normal part of programming
- How you learn and improve

**Common emotions during debugging:**
- Frustration, anger, embarrassment
- These are normal and expected
- Use them to stay engaged with the problem

---

## Think Like a Manager

**Treat the computer like an employee:**
- **Strengths**: Speed, precision, never forgets
- **Weaknesses**: No empathy, can't see the big picture
- **Your job**: Leverage strengths, work around weaknesses

**Good debugging strategies:**
- Take breaks when frustrated
- Work on smaller pieces
- Ask for help when stuck
- Learn from every error

---

## Common Error Types

**Syntax Errors:**
- Code structure is wrong
- Python can't understand what you wrote
- Usually caught before running

**Runtime Errors:**
- Code runs but fails during execution
- Often related to data or logic problems
- Examples: division by zero, wrong data types

**Logical Errors:**
- Code runs without errors
- But doesn't do what you intended
- Hardest to find and fix

---

## Integrated Development Environments (IDEs)

**What is an IDE?**
- Text editor + debugging tools + project management
- Makes programming easier and faster

**Popular IDEs:**
- **VS Code**: Free, powerful, many extensions
- **PyCharm**: Python-specific, full-featured
- **IDLE**: Simple, comes with Python
- **Jupyter Notebooks**: Great for learning and data science

---

## Git and GitHub Basics

**Version Control:**
- Track changes in your code
- Collaborate with others
- Backup your work
- Roll back to previous versions

**GitHub:**
- Host your code online
- Share projects with the world
- Contribute to open source
- Build a portfolio

---

## Basic Git Commands

```bash
git init          # Start a new repository
git add .         # Stage all changes
git commit -m "message"  # Save changes
git push          # Upload to GitHub
git pull          # Download from GitHub
```

---

## Programming Dos and Don'ts

**DO:**
- Start simple and build up
- Test your code frequently
- Use clear variable names
- Comment your code
- Save your work often
- Take breaks when debugging

**DON'T:**
- Try to write everything at once
- Ignore error messages
- Use unclear names like `x` or `temp`
- Forget to backup your work
- Give up when things don't work
- Let frustration stop you from learning

---

## Key Takeaways

1. **Programming is problem-solving** - break big problems into small steps
2. **Python is beginner-friendly** - interpreted, readable, versatile
3. **Start with basics** - variables, types, functions, expressions
4. **Use the right tools** - IDEs make programming easier
5. **Version control matters** - Git helps you track changes and collaborate
6. **Practice makes perfect** - write code every day
7. **Don't fear errors** - they're how you learn
8. **Comments help others** - explain why, not what
9. **Formal languages are precise** - every detail matters
10. **Debugging is normal** - use errors as learning opportunities

---

## Next Steps

- Practice writing simple programs
- Experiment with different data types
- Learn about variables and input/output
- Explore your IDE's features
- Set up a GitHub account
- Join the programming community
- Practice debugging with simple exercises
