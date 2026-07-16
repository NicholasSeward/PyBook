# Quiz (Module 13 - C C++ Primer)

## Multiple Choice Questions (10 questions)

1. What is the main difference between Python and C++ memory management?
   a) Python uses more memory than C++
   b) Python automatically manages memory, C++ requires manual management
   c) C++ uses more memory than Python
   d) Both languages manage memory the same way

2. What is a memory leak in C++?
   a) When you delete memory twice
   b) When you forget to delete memory that was allocated with `new`
   c) When you use too much memory
   d) When you access memory after it's deleted

3. What is the main advantage of C++ over Python?
   a) C++ is typically faster
   b) C++ is easier to learn
   c) C++ gives low level access
   d) Both a and c

4. Why must you use the `#include <iostream>` directive before using `cout` in C++?
   a) It defines the main function
   b) It lets the compiler know about `cout` and related functionality
   c) It allocates memory for variables
   d) It optimizes the program

5. What is the output of the following C++ code?
   ```cpp
   int x = 5;
   int* ptr = &x;
   cout << *ptr;
   ```
   a) 5
   b) The memory address of x
   c) Error
   d) Undefined

6. What is the purpose of the `new` operator in C++?
   a) To create a new variable
   b) To allocate memory on the heap
   c) To create a new function
   d) To create a new class

7. What is the purpose of the `delete` operator in C++?
   a) To remove a variable
   b) To free memory allocated with `new`
   c) To remove a function
   d) To remove a class

8. What is the output of the following C++ code?
   ```cpp
   #include <vector>
   std::vector<int> arr = {1, 2, 3, 4, 5};
   cout << arr.at(2);
   ```
   a) 1
   b) 2
   c) 3
   d) 4

9. What is the purpose of specifying a type (like `int`, `double`, or `char`) before a variable in C++?
   a) To declare the variable's data type
   b) To allocate memory on the heap
   c) To free memory when done
   d) To perform logical comparison

10. What is the main difference between `++` in C++ and how you increment a variable in Python?
    a) `++` works in both C++ and Python
    b) `++` is used to increment variables in C++, but Python uses `+= 1`
    c) Both languages use `i++` to increment
    d) You cannot increment variables in C++

## Matching Questions (2 questions)

**Question 11:** Match each C++ concept with its Python equivalent.

| C++ Concept      | Python Equivalent     |
|------------------|----------------------|
| A) `cout`        | 1) `print()`         |
| B) `int x{5};`   | 2) `x = 5`           |
| C) `#include`    | 3) `import`          |
| D) `;`           | 4) (not used in Python) |


**Question 12:** Match each memory management concept with its description.

| Concept | Description |
|---------|-------------|
| A) Stack memory | 1) Automatically managed memory |
| B) Heap memory | 2) Manually managed memory |
| C) Memory leak | 3) Forgotten allocated memory |
| D) Dangling pointer | 4) Pointer to freed memory |

## True/False Questions (3 questions)

13. C++ programs must be compiled before they can run. (True/False)

14. Python is always slower than C++. (True/False)

15. Memory leaks can cause programs to crash. (True/False)

## Fill in the Blank Questions (5 questions)

16. The `_____` statement is used to print output to the console in C++.

17. The `_____` loop is commonly used in C++ to repeat a block of code a specific number of times.

18. Curly `_____` are used to group related statements in C++.

19. The `_____` type is used to store a single character in C++.

20. The function `_____()` is the entry point of every C++ program.

## Answer Key

**Multiple Choice:**
1. b) Python automatically manages memory, C++ requires manual management
2. b) When you forget to delete memory that was allocated with `new`
3. d) Both a and c
4. b) It lets the compiler know about `cout` and related functionality
5. a) 5
6. b) To allocate memory on the heap
7. b) To free memory allocated with `new`
8. c) 3
9. a) To declare the variable's data type
10. b) `++` is used to increment variables in C++, but Python uses `+= 1`

**Matching:**
11. A-1, B-2, C-3, D-4
12. A-1, B-2, C-3, D-4

**True/False:**
13. True
14. False
15. True

**Fill in the Blank:**
16. `cout`
17. `for`
18. `braces`
19. `char`
20. `main`
