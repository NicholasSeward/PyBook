# Quiz (Module 4 - Functions and Recursion)

## Multiple Choice Questions (10 questions)

1. What is the purpose of the `return` statement in a function?
   a) To stop the function from running
   b) To send a value back to the caller
   c) To print output to the screen
   d) To define the function parameters

2. What happens when a function doesn't have a `return` statement?
   a) It causes an error
   b) It returns `None`
   c) It returns `True`
   d) It returns `False`

3. What is the call stack principle?
   a) First In, First Out (FIFO)
   b) Last In, First Out (LIFO)
   c) Random order
   d) No specific order

4. What is the output of the following code?
   ```python
   def add_numbers(a, b=0):
       return a + b
   
   result = add_numbers(5)
   print(result)
   ```
   a) 5
   b) 0
   c) Error
   d) None

5. What is a function signature?
   a) The function's name
   b) The function's body
   c) The function's name and parameters
   d) The function's return value

6. What is the purpose of default arguments?
   a) To make arguments optional
   b) To make arguments required
   c) To change argument types
   d) To rename arguments

7. What is the output of the following code?
   ```python
   def square(x):
       return x * x

   print(square(3))
   ```
   a) 6  
   b) 9  
   c) 3  
   d) Error

8. What is the purpose of function annotations?
   a) To make code run faster
   b) To provide hints about parameter and return types
   c) To make functions required
   d) To create documentation

9. What is the result of calling a function with the wrong number of arguments?
   a) The function runs normally
   b) A TypeError occurs
   c) The function returns None
   d) The function uses default values

10. What is the purpose of the `pass` statement?
    a) To skip the next line
    b) To do nothing (placeholder)
    c) To stop the function
    d) To return a value

## Matching Questions (2 questions)

**Question 11:** Match each function concept with its description.

| Concept | Description |
|---------|-------------|
| A) Parameter | 1) A value passed to a function |
| B) Argument | 2) A variable in the function definition |
| C) Return value | 3) A value sent back from a function |
| D) Function call | 4) The act of executing a function |

**Question 12:** Match each recursion concept with its description.

| Concept | Description |
|---------|-------------|
| A) Base case | 1) The recursive call to the same function |
| B) Recursive case | 2) The condition that stops recursion |
| C) Call stack | 3) The structure that tracks function calls |
| D) Infinite recursion | 4) When recursion never reaches a base case |

## True/False Questions (3 questions)

13. A function can have multiple `return` statements. (True/False)

14. Default arguments must come after non-default arguments in a function definition. (True/False)

15. Recursion typically uses more memory than iteration. (True/False)

## Fill in the Blank Questions (5 questions)

16. The `_____` statement sends a value back from a function to the caller.

17. A `_____` function is a function that calls itself.

18. The call `_____` tracks all the function calls that are currently active.

19. A `_____` is a parameter that has a value specified in the function signature.

20. The `_____` of a function includes its name and parameters.

## Answer Key

**Multiple Choice:**
1. b) To send a value back to the caller
2. b) It returns `None`
3. b) Last In, First Out (LIFO)
4. a) 5
5. c) The function's name and parameters
6. a) To make arguments optional
7. b) 9
8. b) To provide hints about parameter and return types
9. b) A TypeError occurs
10. b) To do nothing (placeholder)

**Matching:**
11. A-2, B-1, C-3, D-4
12. A-2, B-1, C-3, D-4

**True/False:**
13. True
14. True
15. False

**Fill in the Blank:**
16. `return`
17. `recursive`
18. `stack`
19. `default`
20. `signature`
