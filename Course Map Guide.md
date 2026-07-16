# Course Map Guide: Aligning Your Online Course

To complete your course map, start by clearly defining the course objectives, outlining what students should achieve by the end. Next, break down the content into modules or units, and list the learning activities and assessments for each section.

Include all necessary resources and create a schedule that sequences the modules, activities, and assessments throughout the course. This structure will guide both instructors and students, ensuring a clear and organized course.

> NOTE: Adapted from *The Online Course Map Guide* (2019). The Online Course Mapping Guide Course Map Template is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

---

## Course Map

| Field | Value |
|-------|-------|
| Course ID | CPSI 17503 |
| Course Name | Programming I |
| Instructor Name | |
| Designer Name | |

### Program Outcomes Addressed (optional)

- Apply fundamental programming concepts to solve computational problems
- Use version control and professional development workflows
- Communicate program behavior through clear code and documentation

### Course Learning Outcomes (CLOs)

1. Write, run, and debug Python programs that use variables, expressions, and standard input/output. (CLO1)
2. Implement control flow with conditionals, loops, and functions, including basic recursion. (CLO2)
3. Select and use core data structures (strings, lists, dictionaries, tuples) appropriately. (CLO3)
4. Persist and process data with files, and organize programs with classes where appropriate. (CLO4)
5. Analyze simple algorithms for correctness and basic time/space tradeoffs. (CLO5)
6. Submit work through GitHub using course naming, formatting, and verification practices. (CLO6)

### Course Materials

| Type | Details |
|------|---------|
| Primary digital text | Course TxtBook modules (each module links to related *Think Python*, 3rd edition content) |
| Textbook | Downey, A. B. *Think Python*, 3rd edition |
| LMS / course shell | Module videos and any participation activities hosted in the course shell |
| Development tools | Python 3, IDE or editor, Git, GitHub |

### Assessment Types (all modules)

| Assessment | Delivery | Grading |
|------------|----------|---------|
| Quiz | LMS / TxtBook quiz | Autograded |
| Tutorial | LMS / TxtBook tutorial | Autograded |
| Practice | GitHub repository submission | Instructor graded with [Practice Rubric](#practice-rubric) |

---

## How to Use This Map

For each module below:

- **MLOs** are measurable outcomes. CLO numbers in parentheses show course alignment.
- **Assessments** are Quiz, Tutorial, and Practice unless noted.
- **Instructional materials** center on the TxtBook module (with Think Python links). Videos live in the course shell.
- **Student steps** follow the same workflow every module.

### Default student steps (every module)

1. Complete the in-class interactive activity (or activities) scheduled for the module. Student handouts live in each module folder as `Activity N - ....md`.
2. Complete the LMS participation activity if one is present.
3. Read and watch the module materials (TxtBook sections, Think Python links, and course-shell videos).
4. Complete the **Quiz** (autograded).
5. Complete the **Tutorial** (autograded), when offered.
6. Complete the **Practice** assignment and submit through **GitHub**, when offered.

---

## Modules

### Module 01: Intro

**Overview:** Students meet Python as a way of thinking about problems. They write a first program, use comments, explore number systems and how languages run (compiled vs interpreted), set up an IDE, and begin using Git and GitHub for coursework.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Write and run a simple Python program that prints output. | CLO1 |
| 2 | Distinguish compiled and interpreted execution at a high level. | CLO1 |
| 3 | Convert between common number-system representations used in computing. | CLO1 |
| 4 | Use comments to document intent in source files. | CLO1, CLO6 |
| 5 | Perform basic Git operations (clone, add, commit, push) for a course repo. | CLO6 |
| 6 | Navigate an IDE or editor well enough to create, save, and run a `.py` file. | CLO1, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 1 - Intro) | Autograded | 1, 2, 3, 4 |
| Tutorial (Module 1 - Intro) | Autograded | 1, 4, 6 |
| Practice (Module 1 - Intro) | [Practice Rubric](#practice-rubric) | 1, 4, 5, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Number Systems Relay](Module 01 - Intro/Activity 1 - Number Systems Relay.md) (20-25 min, teams) | 1, 3 |
| In-class: [Activity 2 - Hello Git Pair Lab](Module 01 - Intro/Activity 2 - Hello Git Pair Lab.md) (25-30 min, pairs) | 1, 5, 6 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 01 - Intro (includes Think Python Chapter 1 links) | 1-6 |
| Course-shell videos for Module 01 | 1, 5, 6 |
| Sections: Hello World and Comments; Compiled vs Interpreted; Number Systems; IDEs; Git GitHub Basics | 1-6 |
| Slides (Module 1 - Intro) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 02: Basics

**Overview:** Students build fluency with variables, types, operators, casting, f-strings, PEP 8 style, and reading error messages so they can write small interactive programs confidently.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Declare variables and evaluate arithmetic and comparison expressions. | CLO1 |
| 2 | Convert values between types using casting, and predict common conversion results. | CLO1 |
| 3 | Format output with f-strings. | CLO1 |
| 4 | Apply PEP 8 naming and spacing conventions in short programs. | CLO6 |
| 5 | Interpret basic traceback messages to locate syntax and runtime errors. | CLO1 |
| 6 | Write a short program that uses input, calculation, and formatted output. | CLO1, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 2 - Basics) | Autograded | 1-5 |
| Tutorial (Module 2 - Basics) | Autograded | 1-4, 6 |
| Practice (Module 2 - Basics) | [Practice Rubric](#practice-rubric) | 1-4, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Error Autopsy](Module 02 - Basics/Activity 1 - Error Autopsy.md) (25 min, teams) | 5 |
| In-class: [Activity 2 - F-String Gallery Walk](Module 02 - Basics/Activity 2 - F-String Gallery Walk.md) (20-25 min, pairs) | 3, 4, 6 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 02 - Basics (includes Think Python Chapter 2 links) | 1-6 |
| Course-shell videos for Module 02 | 1, 5, 6 |
| Sections: Casting; Formatting Strings; Coding Conventions (PEP 8); Errors and Tracebacks | 2-5 |
| Slides (Module 2 - Basics) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 03: Conditionals and Functions

**Overview:** Students branch with `if`/`elif`/`else`, reason about truthy and falsy values, and write functions with parameters and scope so programs can make decisions and reuse logic.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Write chained conditionals that select among multiple cases. | CLO2 |
| 2 | Predict results of boolean expressions, including truthy and falsy values. | CLO2 |
| 3 | Define and call functions with parameters. | CLO2 |
| 4 | Distinguish local and global scope in short examples. | CLO2 |
| 5 | Trace simple recursive or nested function calls at a conceptual level. | CLO2 |
| 6 | Combine conditionals and functions in a small complete program. | CLO2, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 3 - Conditionals and Functions) | Autograded | 1-5 |
| Tutorial (Module 3 - Conditionals and Functions) | Autograded | 1-4, 6 |
| Practice (Module 3 - Conditionals and Functions) | [Practice Rubric](#practice-rubric) | 1, 3, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Truthy / Falsy Card Sort](Module 03 - Conditionals and Functions/Activity 1 - Truthy Falsy Card Sort.md) (20-25 min, teams) | 2 |
| In-class: [Activity 2 - Function Signature Trade](Module 03 - Conditionals and Functions/Activity 2 - Function Signature Trade.md) (25-30 min, pairs) | 3, 4, 6 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 03 - Conditionals and Functions (Think Python Chapters 3 and 5 links) | 1-6 |
| Course-shell videos for Module 03 | 1, 3, 5 |
| Sections: Scope; Truthy and Falsy Values | 2, 4 |
| Slides (Module 3 - Conditionals and Functions) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 04: Functions and Recursion

**Overview:** Students deepen function design: return values, default arguments, decomposition, call-stack mental models, and turtle-based interface examples that show how functions work together.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Write functions that return values and use those returns in expressions. | CLO2 |
| 2 | Use default arguments appropriately in function signatures. | CLO2 |
| 3 | Decompose a problem into cooperating functions with clear responsibilities. | CLO2 |
| 4 | Explain stack frames for a short call chain (including simple recursion). | CLO2 |
| 5 | Read function annotations or signatures as documentation of intent. | CLO2 |
| 6 | Implement a multi-function solution that meets a stated interface. | CLO2, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 4 - Functions and Recursion) | Autograded | 1-5 |
| Tutorial (Module 4 - Functions and Recursion) | Autograded | 1-3, 6 |
| Practice (Module 4 - Functions and Recursion) | [Practice Rubric](#practice-rubric) | 1, 3, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Human Call Stack](Module 04 - Functions and Recursion/Activity 1 - Human Call Stack.md) (20-25 min, whole class) | 4 |
| In-class: [Activity 2 - Decompose the Spec](Module 04 - Functions and Recursion/Activity 2 - Decompose the Spec.md) (25-30 min, teams) | 3, 6 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 04 - Functions and Recursion (Think Python Chapters 4 and 6 links) | 1-6 |
| Course-shell videos for Module 04 | 3, 4, 6 |
| Sections: Default Arguments; Function Signatures; Modular Design; Call Stack Visualization | 2-5 |
| Slides (Module 4 - Functions and Recursion) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 05: Iteration

**Overview:** Students master `while` and `for` loops, accumulators, loop control (`break`/`continue`), and index-based vs direct iteration to process sequences systematically.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Write `while` loops with clear termination conditions. | CLO2 |
| 2 | Write `for` loops over ranges and sequences. | CLO2, CLO3 |
| 3 | Use accumulators and counters to compute running results. | CLO2 |
| 4 | Apply `break` and `continue` intentionally (and avoid misuse). | CLO2 |
| 5 | Choose between index-based and direct iteration for a task. | CLO2, CLO3 |
| 6 | Solve a multi-step problem that requires nested or sequential loops. | CLO2, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 5 - Iteration) | Autograded | 1-5 |
| Tutorial (Module 5 - Iteration) | Autograded | 1-4, 6 |
| Practice (Module 5 - Iteration) | [Practice Rubric](#practice-rubric) | 1-3, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Loop Translation Race](Module 05 - Iteration/Activity 1 - Loop Translation Race.md) (20-25 min, pairs) | 1, 2 |
| In-class: [Activity 2 - Accumulator Clinic](Module 05 - Iteration/Activity 2 - Accumulator Clinic.md) (25 min, teams) | 3, 6 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 05 - Iteration (Think Python Chapter 7 links) | 1-6 |
| Course-shell videos for Module 05 | 1-4 |
| Sections: While Loops; Accumulators and Counters; Loop Control; Index-based vs Direct Iteration | 1-5 |
| Slides (Module 5 - Iteration) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 06: Data Structures

**Overview:** Students use lists, dictionaries, and tuples; compare mutable vs immutable behavior; and pick structures that fit the data and operations they need.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Create, index, slice, and update lists using common list methods. | CLO3 |
| 2 | Store and retrieve values with dictionaries; iterate keys, values, and items. | CLO3 |
| 3 | Use tuples for immutable sequences and multiple return values. | CLO3 |
| 4 | Explain how mutability affects aliasing and unexpected shared updates. | CLO3, CLO5 |
| 5 | Choose among list, dict, and tuple for a stated problem. | CLO3 |
| 6 | Implement a small program that combines at least two structure types. | CLO3, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 6 - Data Structures) | Autograded | 1-5 |
| Tutorial (Module 6 - Data Structures) | Autograded | 1-3, 6 |
| Practice (Module 6 - Data Structures) | [Practice Rubric](#practice-rubric) | 1, 2, 5, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Structure Speed Dating](Module 06 - Data Structures/Activity 1 - Structure Speed Dating.md) (25-30 min, trios) | 5 |
| In-class: [Activity 2 - Mutation Mystery](Module 06 - Data Structures/Activity 2 - Mutation Mystery.md) (20-25 min, pairs) | 4 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 06 - Data Structures (Think Python Chapters 9-11 links) | 1-6 |
| Course-shell videos for Module 06 | 1-4 |
| Sections: List Methods; Immutable vs Mutable | 1, 4 |
| Slides (Module 6 - Data Structures) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 07: String Manipulation

**Overview:** Students treat strings as sequences, use indexing and methods, understand escape characters and character encodings, and apply basic pattern tools where introduced.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Index, slice, and traverse strings correctly (including zero-based indexing). | CLO3 |
| 2 | Use common string methods (`upper`, `strip`, `split`, `join`, `replace`, and similar). | CLO3 |
| 3 | Explain and use common escape sequences in string literals. | CLO1, CLO3 |
| 4 | Convert between characters and codes with `ord`/`chr` at an introductory level. | CLO3 |
| 5 | Apply a simple regular-expression or pattern task when presented in the module. | CLO3 |
| 6 | Build a short program that cleans or analyzes text input. | CLO3, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 7 - String Manipulation) | Autograded | 1-5 |
| Tutorial (Module 7 - String Manipulation) | Autograded | 1-3, 6 |
| Practice (Module 7 - String Manipulation) | [Practice Rubric](#practice-rubric) | 1, 2, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Escape Hatch Decode](Module 07 - String Manipulation/Activity 1 - Escape Hatch Decode.md) (20 min, teams) | 3 |
| In-class: [Activity 2 - Text Surgery Relay](Module 07 - String Manipulation/Activity 2 - Text Surgery Relay.md) (25-30 min, relay teams) | 2, 6 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 07 - String Manipulation (Think Python Chapter 8 links) | 1-6 |
| Course-shell videos for Module 07 | 1-4 |
| Sections: Escape Characters; ASCII and Unicode | 3, 4 |
| Slides (Module 7 - String Manipulation) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 08: File IO

**Overview:** Students read and write files safely, choose open modes, handle path and I/O errors, and explore simple persistence ideas (including pickle and basic DB concepts).

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Open, read, and write text files using appropriate modes. | CLO4 |
| 2 | Process files line by line and as a whole, choosing an approach that fits memory and task. | CLO4 |
| 3 | Use `pathlib` or equivalent path handling for portable file locations. | CLO4 |
| 4 | Catch and respond to common I/O errors with `try`/`except`. | CLO4 |
| 5 | Explain when serialization (for example pickle) or a simple DB approach is useful. | CLO4 |
| 6 | Deliver a GitHub practice that reads and/or writes files correctly. | CLO4, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 8 - File IO) | Autograded | 1-5 |
| Tutorial (Module 8 - File IO) | Autograded | 1-4, 6 |
| Practice (Module 8 - File IO) | [Practice Rubric](#practice-rubric) | 1, 2, 4, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Path Scavenger Hunt](Module 08 - File IO/Activity 1 - Path Scavenger Hunt.md) (25 min, pairs) | 3 |
| In-class: [Activity 2 - Broken File Clinic](Module 08 - File IO/Activity 2 - Broken File Clinic.md) (25-30 min, teams) | 1, 4 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 08 - File IO (Think Python Chapter 13 links) | 1-6 |
| Course-shell videos for Module 08 | 1-4 |
| Sections: File Open Modes; File Paths; Reading Line by Line vs All at Once; Error Handling; Serialization; Simple DB Concepts | 1-5 |
| Slides (Module 8 - File IO) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 09: Classes

**Overview:** Students define classes and objects, write methods and constructors, practice encapsulation and interfaces, and use inheritance to extend behavior.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Define a class with attributes and instantiate objects. | CLO4 |
| 2 | Write instance methods, including `__init__` and `__str__` where useful. | CLO4 |
| 3 | Use encapsulation to separate interface from implementation. | CLO4 |
| 4 | Extend a class with inheritance and override or reuse parent behavior. | CLO4 |
| 5 | Trace object state across method calls in a short program. | CLO4 |
| 6 | Submit a class-based practice solution via GitHub that meets the stated interface. | CLO4, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 9 - Classes) | Autograded | 1-5 |
| Tutorial (Module 9 - Classes) | Autograded | 1-3, 6 |
| Practice (Module 9 - Classes) | [Practice Rubric](#practice-rubric) | 1, 2, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Class Design Studio](Module 09 - Classes/Activity 1 - Class Design Studio.md) (25-30 min, teams) | 1, 3 |
| In-class: [Activity 2 - Inheritance Family Tree](Module 09 - Classes/Activity 2 - Inheritance Family Tree.md) (25 min, pairs) | 4, 5 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 09 - Classes (Think Python Chapters 14-17 links) | 1-6 |
| Course-shell videos for Module 09 | 1-4 |
| Section: Encapsulation and Interface Design | 3 |
| Slides (Module 9 - Classes) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 10: Random and Memory

**Overview:** Students generate pseudorandom values, reason about aliasing and copying, and use basic time/space complexity ideas plus simple algorithms and timing tools.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Use the `random` module to simulate chance events reproducibly with seeds when needed. | CLO1, CLO5 |
| 2 | Distinguish pseudorandom generation from true randomness at a conceptual level. | CLO5 |
| 3 | Predict aliasing effects and choose shallow vs deep copy appropriately. | CLO3, CLO5 |
| 4 | Classify simple algorithms with basic Big-O time and space intuition. | CLO5 |
| 5 | Time code snippets with the `time` module for rough comparison. | CLO5 |
| 6 | Implement a practice program that uses randomness and/or algorithmic patterns correctly. | CLO5, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 10 - Random and Memory) | Autograded | 1-5 |
| Tutorial (Module 10 - Random and Memory) | Autograded | 1, 3, 6 |
| Practice (Module 10 - Random and Memory) | [Practice Rubric](#practice-rubric) | 1, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Seeded Random Showdown](Module 10 - Random and Memory/Activity 1 - Seeded Random Showdown.md) (20-25 min, pairs) | 1, 2 |
| In-class: [Activity 2 - Complexity Sorting Cards](Module 10 - Random and Memory/Activity 2 - Complexity Sorting Cards.md) (25 min, teams) | 4 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 10 - Random and Memory (with Think Python links where present) | 1-6 |
| Course-shell videos for Module 10 | 1-5 |
| Sections: Random Module; Pseudorandom vs True Random; Aliasing and Deep Copy; Intro to Time and Space Complexity; Common Algorithms; Time Module Basics | 1-5 |
| Slides (Module 10 - Random and Memory) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 11: Python Tricks

**Overview:** Students write more concise Python using sets, comprehensions, conditional expressions, lambdas with `map`/`filter`, iterators/generators, and packing/unpacking patterns.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Use sets for membership tests and basic set operations. | CLO3 |
| 2 | Rewrite suitable loops as list, dict, or set comprehensions. | CLO3 |
| 3 | Use conditional expressions and simple lambdas with `map`/`filter` where clear. | CLO2, CLO3 |
| 4 | Explain iterators vs generators at an introductory level. | CLO3, CLO5 |
| 5 | Apply `zip` and unpacking (`*`, `**`) in practical examples. | CLO3 |
| 6 | Deliver a practice solution that uses at least one “trick” idiom correctly and readably. | CLO3, CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 11 - Python Tricks) | Autograded | 1-5 |
| Tutorial (Module 11 - Python Tricks) | Autograded | 1-3, 6 |
| Practice (Module 11 - Python Tricks) | [Practice Rubric](#practice-rubric) | 2, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Comprehension Translation Desk](Module 11 - Python Tricks/Activity 1 - Comprehension Translation Desk.md) (25 min, pairs) | 2 |
| In-class: [Activity 2 - Pythonic Rewrite Relay](Module 11 - Python Tricks/Activity 2 - Pythonic Rewrite Relay.md) (20-25 min, relay) | 3, 5 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 11 - Python Tricks (Think Python Chapter 18 links) | 1-6 |
| Course-shell videos for Module 11 | 1-5 |
| Sections: Sets; Comprehensions; Conditional Expressions; Lambda Functions and map filter; Iterators and Generators; zip and Unpacking | 1-5 |
| Slides (Module 11 - Python Tricks) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 12: Fancy Data Structures

**Overview:** Students connect algorithm analysis to structure choice, implement or trace linked lists and binary search trees, and compare growth rates that matter in practice.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Compare common sorting and searching algorithms by Big-O class. | CLO5 |
| 2 | Describe linked-list structure and basic insert/traverse operations. | CLO3, CLO5 |
| 3 | Explain binary search tree ordering rules and lookup behavior. | CLO3, CLO5 |
| 4 | Relate tree balance to performance (balanced vs degenerate cases). | CLO5 |
| 5 | Recognize exponential and factorial growth as impractical for large inputs. | CLO5 |
| 6 | Demonstrate understanding on the module quiz using vocabulary and worked examples. | CLO5 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 12 - Fancy Data Structures) | Autograded | 1-6 |
| Tutorial | Not offered this term | - |
| Practice | Not offered this term | - |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Build-a-BST Live](Module 12 - Fancy Data Structures/Activity 1 - Build-a-BST Live.md) (25-30 min, whole class) | 3, 4 |
| In-class: [Activity 2 - Algorithm Auction](Module 12 - Fancy Data Structures/Activity 2 - Algorithm Auction.md) (20-25 min, teams) | 1, 5 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 12 - Fancy Data Structures (with Think Python links where present) | 1-6 |
| Course-shell videos for Module 12 | 1-5 |
| Sections: Algorithm Analysis; Linked Lists; Binary Search Tree; Advanced Complexity | 1-5 |
| Slides (Module 12 - Fancy Data Structures) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

### Module 13: C C++ Primer

**Overview:** Students compare Python with C/C++ syntax and compilation, see why types and memory matter, and complete a first C++ practice that reinforces control flow in a compiled language.

**Module Learning Outcomes (MLOs)**

| MLO | Description | Aligned CLO(s) |
|-----|-------------|----------------|
| 1 | Contrast Python’s dynamic typing with C/C++ type declarations. | CLO1, CLO5 |
| 2 | Describe compile-then-run workflow versus interpreted Python execution. | CLO1 |
| 3 | Explain stack/heap and manual memory ideas at an introductory level. | CLO5 |
| 4 | Read short C++ snippets that mirror Python conditionals and loops. | CLO2 |
| 5 | Identify performance motivations for using C/C++ in hot paths. | CLO5 |
| 6 | Submit a working C++ practice program through the required GitHub workflow. | CLO6 |

**Assessments and Rubrics**

| Assessment | Rubric / Not graded | Aligned MLO(s) |
|------------|---------------------|----------------|
| Quiz (Module 13 - C C++ Primer) | Autograded | 1-5 |
| Tutorial | Not offered this term | - |
| Practice (Module 13 - C C++ Primer) | [Practice Rubric](#practice-rubric) | 4, 6 |

**Activities: Learner Interaction and Engagement**

| Activity | Aligned MLO(s) |
|----------|----------------|
| In-class: [Activity 1 - Python to C++ Translation Relay](Module 13 - C C++ Primer/Activity 1 - Python to C++ Translation Relay.md) (25-30 min, teams) | 1, 2, 4 |
| In-class: [Activity 2 - Compile Error Clinic](Module 13 - C C++ Primer/Activity 2 - Compile Error Clinic.md) (20-25 min, pairs) | 2, 6 |
| Course-shell participation activity (if present) | see MLOs |
| Watch module videos in the course shell | see MLOs |
| Work TxtBook module sections (includes Think Python links where provided) | see MLOs |
| Autograded quiz and tutorial (when offered) | see MLOs |
| Practice submission via GitHub (when offered) | see MLOs |


**Instructional Materials**

| Material | Aligned MLO(s) or Supplemental/Optional |
|----------|-----------------------------------------|
| TxtBook: Module 13 - C C++ Primer | 1-6 |
| Course-shell videos for Module 13 | 1-5 |
| Sections: Syntax Comparisons; Type Declarations and Compilation Model; Manual Memory Management; Performance Considerations | 1-5 |
| Slides (Module 13 - C C++ Primer) | Supplemental |

**Steps to complete this module**

1. Do the in-class interactive activity (or activities); see Activity handouts in this module folder.
2. Complete the participation activity if present.
3. Read and watch the module materials (TxtBook + Think Python links + course-shell videos).
4. Complete the Quiz (autograded).
5. Complete the Tutorial (autograded), when offered.
6. Complete Practice and submit through GitHub, when offered.


---

## Practice Rubric

Used for GitHub Practice assignments (and any similarly graded coding submissions). Quizzes and tutorials are autograded separately.

### Design goals

- **No granular partial credit.** This saves grader time. Students are trained to verify submissions before they mark work complete.
- Feedback focuses on **clear categories** (small defects vs major failure) rather than point-by-point line scoring.

### Grade outcomes

| Outcome | When it applies | Typical result |
|---------|-----------------|----------------|
| Full credit | Runs, meets major requirements, follows naming/format expectations aside from at most minor issues already covered below | 100% of practice points (before late/resubmit penalties) |
| Small deduction | One small bug, style/guideline miss, or incorrect filename/placement | **-10** |
| Multiple defects | Several small bugs and/or repeated guideline issues | **up to -30** (instructor judgment) |
| Educational comment instead of resubmit | Instructor judges a written comment sufficient for learning | Deduction as above; no resubmit required |
| Resubmit / incomplete | Missing a major requirement, or submission does not run | Treated as needing fix and resubmit (see policies below) |
| Zero | Submission cannot be graded as a serious attempt, or still fails after policy limits | **0**, with a specific fix list |

### What counts as a “small bug”

Examples (not exhaustive):

- Minor logic mistake that still leaves the program largely working
- Not following class formatting or coding guidelines
- Incorrect filenames or incorrect file placement in the repo

### What triggers a resubmit (or equivalent major failure)

- Missing a **major** assignment requirement
- Code **does not run** (crash on required cases, wrong language/tooling, empty submission, and similar)

### Zero grades: required feedback

If a submission will receive a **0**, the grader must list:

1. Specific reasons for the zero
2. Fixes required for a future attempt (when policy allows)

> NOTE: Feedback may include a disclaimer that **there may be more issues** beyond those listed. Students should re-verify the full assignment checklist, not only the named items.

### Late work, resubmits, and stacking penalties

**Reference class policy (unlimited resubmits with a late-resubmit cost):**

- Unlimited resubmissions are allowed.
- Any assignment received **after the initial grading round is complete** receives **-20%**.
- Late work that also has major issues can land near **50%** after stacked penalties, but a successful resubmit can still reach about **80%** (100% minus the -20% post-round penalty, assuming other deductions are cleared).

Late penalties and resubmit penalties **may stack**.

> NOTE: **If a course section does not allow resubmits, this map must be modified** (remove resubmit pathways, redefine zeros/major failures, and update student-facing instructions). Do not assume unlimited resubmits unless the syllabus matches the reference policy above.

### Grader workflow (summary)

1. Confirm the submission runs and includes major required pieces.
2. If it fails that gate: request resubmit (if allowed) or assign 0 with a concrete fix list.
3. If it passes that gate: apply -10 / up to -30 for small or multiple defects, or full credit.
4. Apply late and/or post-initial-round penalties according to the syllabus; note when they stack.
