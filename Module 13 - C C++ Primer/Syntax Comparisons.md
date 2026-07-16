# Syntax Comparisons: Python vs C/C++

## Overview
Python and C/C++ have very different syntax. Understanding these differences helps you learn both languages.

## Basic Structure

### Hello World
```python
# Python
print("Hello, World!")

# C++
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!" << endl;
    return 0;
}
```

### Variables
```python
# Python - no type declaration needed
name = "Alice"
age = 25
height = 5.6
is_student = True

# C++ - must declare types
string name = "Alice";
int age = 25;
double height = 5.6;
bool is_student = true;
```

## Control Structures

### If Statements
```python
# Python
if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teenager")
else:
    print("Child")

# C++
if (age >= 18) {
    cout << "Adult" << endl;
} else if (age >= 13) {
    cout << "Teenager" << endl;
} else {
    cout << "Child" << endl;
}
```

### Loops
```python
# Python - for loop
for i in range(5):
    print(i)

# Python - while loop
i = 0
while i < 5:
    print(i)
    i += 1

# C++ - for loop
for (int i = 0; i < 5; i++) {
    cout << i << endl;
}

# C++ - while loop
int i = 0;
while (i < 5) {
    cout << i << endl;
    i++;
}
```

## Functions

### Function Definition
```python
# Python
def add_numbers(a, b):
    return a + b

# C++
int add_numbers(int a, int b) {
    return a + b;
}
```

### Function Call
```python
# Python
result = add_numbers(5, 3)
print(result)

# C++
int result = add_numbers(5, 3);
cout << result << endl;
```

## Data Structures

### Arrays/Lists
```python
# Python - list
numbers = [1, 2, 3, 4, 5]
numbers.append(6)
print(numbers[0])

# C++ - array
int numbers[5] = {1, 2, 3, 4, 5};
// Can't change size after creation
cout << numbers[0] << endl;
```

### Strings
```python
# Python
name = "Alice"
greeting = "Hello, " + name
print(greeting)

# C++
string name = "Alice";
string greeting = "Hello, " + name;
cout << greeting << endl;
```

## Real Example: Student Grade Calculator

### Python Version
```python
def calculate_grade(scores):
    if not scores:
        return 0
    
    total = sum(scores)
    average = total / len(scores)
    
    if average >= 90:
        return 'A'
    elif average >= 80:
        return 'B'
    elif average >= 70:
        return 'C'
    elif average >= 60:
        return 'D'
    else:
        return 'F'

# Test the function
student_scores = [85, 92, 78, 96, 88]
grade = calculate_grade(student_scores)
print(f"Grade: {grade}")

# Calculate average
average = sum(student_scores) / len(student_scores)
print(f"Average: {average:.1f}")
```

### C++ Version
```cpp
#include <iostream>
#include <vector>
using namespace std;

char calculate_grade(vector<int> scores) {
    if (scores.empty()) {
        return 'F';
    }
    
    int total = 0;
    for (int score : scores) {
        total += score;
    }
    
    double average = static_cast<double>(total) / scores.size();
    
    if (average >= 90) {
        return 'A';
    } else if (average >= 80) {
        return 'B';
    } else if (average >= 70) {
        return 'C';
    } else if (average >= 60) {
        return 'D';
    } else {
        return 'F';
    }
}

int main() {
    vector<int> student_scores = {85, 92, 78, 96, 88};
    char grade = calculate_grade(student_scores);
    cout << "Grade: " << grade << endl;
    
    // Calculate average
    int total = 0;
    for (int score : student_scores) {
        total += score;
    }
    double average = static_cast<double>(total) / student_scores.size();
    cout << "Average: " << fixed << setprecision(1) << average << endl;
    
    return 0;
}
```

## Key Differences

### Python:
- **No semicolons** needed
- **No curly braces** - uses indentation
- **No type declarations** - types are inferred
- **Simpler syntax** - less punctuation
- **Dynamic typing** - variables can change types

### C++:
- **Semicolons** required at end of statements
- **Curly braces** for code blocks
- **Type declarations** required
- **More punctuation** - `#include`, `using namespace`
- **Static typing** - types must match

## Memory Management

### Python:
```python
# Automatic memory management
name = "Alice"
name = "Bob"  # Old "Alice" string is automatically cleaned up
```

### C++:
```cpp
// Manual memory management
string* name = new string("Alice");
// ... use name ...
delete name;  // Must clean up manually
```

## Summary

✅ **Python** - simpler syntax, automatic memory management  
✅ **C++** - more control, manual memory management  
✅ **Python** - no types, no semicolons, indentation-based  
✅ **C++** - types required, semicolons, curly braces  
✅ **Both** - powerful languages with different strengths  

Understanding syntax differences helps you learn both languages effectively!
