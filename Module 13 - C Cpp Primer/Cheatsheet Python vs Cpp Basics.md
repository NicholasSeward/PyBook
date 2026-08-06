# Cheatsheet: Python vs Cpp Basics

Quick side-by-side for common tasks: variables, printing, input, `if`, `for`, vectors/arrays, and bounds-checked access with `at`.

Use this while you work through the rest of Module 13 and the Practice.

## Types and variables

### Python

```py
# dynamic typing
x = 42           # int
pi = 3.14        # float
name = "Ada"     # str
ok = True        # bool

# optional type hints (not enforced at runtime)
age: int = 20
```

### C++

```cpp
#include <string>

int x = 42;                 // int
double pi = 3.14;           // floating-point
std::string name = "Ada";   // string
bool ok = true;             // bool
```

## C++ boilerplate program

```cpp
#include <iostream>
#include <string>
#include <vector>

int main() {
    // Your code here
    std::cout << "Hello, world!\n";
    return 0;
}
```

## Printing

### Python

```py
print("Hello")
name = "Ada"
score = 9.4567
print(f"{name} - {score:.2f}/10")  # f-strings and format specifiers
```

### C++

```cpp
#include <iostream>
#include <iomanip>
#include <string>

std::cout << "Hello\n";
std::string name = "Ada";
double score = 9.4567;
std::cout << name << " - " << score << "/10\n";  // format with iomanip
// newline: "\n" or std::endl (which also flushes)
```

## Input

### Python

```py
# integers
n = int(input("Enter an int: "))     # input() returns str; cast to int

# floats
price = float(input("Enter a price: "))

# multiple ints from one line
a, b = map(int, input("Enter two ints: ").split())

# words (tokens) from one line
line = input("Enter two words: ")
w1, w2 = line.split()
```

### C++

```cpp
#include <iostream>
#include <string>

// integers
int n{};
std::cout << "Enter an int: ";
std::cin >> n;                        // reads an int

// doubles
double price{};
std::cout << "Enter a price: ";
std::cin >> price;                    // reads a double

// two tokens (words)
std::cout << "Enter two words: ";
std::string a, b;
std::cin >> a >> b;                   // reads two whitespace-separated words

// Whole line input
std::cout << "Enter a full line: ";
std::string line;
std::getline(std::cin >> std::ws, line); // eat leading whitespace, then read line
```

## if / elif / else

### Python

```py
x = 7
if x > 10:
    print("big")
elif x == 10:
    print("ten")
else:
    print("small")
```

### C++

```cpp
int x = 7;
if (x > 10) {
    std::cout << "big\n";
} else if (x == 10) {
    std::cout << "ten\n";
} else {
    std::cout << "small\n";
}
```

## for loops

### Python (range and iterate items)

```py
# range-based counting (0..4)
for i in range(5):
    print(i)

# iterating a list
nums = [10, 20, 30]
for n in nums:
    print(n)

# index and value
for i, n in enumerate(nums):
    print(i, n)
```

### C++ (range-based for and classic for)

```cpp
#include <iostream>
#include <vector>

// counting (0..4)
for (int i = 0; i < 5; ++i) {
    std::cout << i << "\n";
}

std::vector<int> nums{10, 20, 30};

// range-based for
for (int n : nums) {
    std::cout << n << "\n";
}

// index and value
for (int i = 0; i < static_cast<int>(nums.size()); ++i) {
    std::cout << i << " " << nums.at(i) << "\n";
}
```

## Lists (Python) vs std::vector (C++)

### Python list

```py
nums = [1, 2, 3]
nums.append(4)      # push back
print(len(nums))    # size
print(nums[0])      # index (IndexError if out of range)
```

### C++ vector

```cpp
#include <vector>
#include <iostream>

std::vector<int> nums{1, 2, 3};
nums.push_back(4);                 // push back
std::cout << nums.size();          // size
std::cout << nums[0];              // unchecked access
```

## Using at() for bounds-checked access

### Python (IndexError on out-of-range)

```py
nums = [10, 20, 30]
try:
    print(nums[10])
except IndexError:
    print("out of range")
```

### C++ vector::at (throws std::out_of_range)

```cpp
#include <vector>
#include <stdexcept>
#include <iostream>

std::vector<int> nums{10, 20, 30};
try {
    std::cout << nums.at(10);
} catch (const std::out_of_range&) {
    std::cout << "out of range\n";
}
```

### Bonus: string::at works similarly

```cpp
#include <string>
#include <stdexcept>
#include <iostream>

std::string s = "abc";
try {
    char ch = s.at(5);
    std::cout << ch;
} catch (const std::out_of_range&) {
    std::cout << "out of range\n";
}
```

## Quick reference

| Python | C++ |
|--------|-----|
| `list.append(x)` | `vector.push_back(x)` |
| `len(list)` | `vector.size()` |
| `for x in items` | `for (auto x : items)` |
| `for i in range(n)` | `for (int i = 0; i < n; ++i)` |
| `IndexError` | `vector::at` throws `std::out_of_range` |

## Try it now

**Prompt:** In C++, write a tiny `main` that reads an integer `n`, stores the numbers `1..n` in a `std::vector<int>`, then prints them with a range-based `for` loop.

```cpp
#include <iostream>
#include <vector>

int main() {
    // TODO: read n, fill vector with 1..n, print each value
    return 0;
}
```

:::details Hint

Use `push_back` in a counting loop, then `for (int x : nums)`.

:::

:::details Solution

**Reasoning:** Build the vector with a classic `for`, then print with a range-based `for`.

```cpp
#include <iostream>
#include <vector>

int main() {
    int n{};
    std::cin >> n;
    std::vector<int> nums;
    for (int i = 1; i <= n; ++i) {
        nums.push_back(i);
    }
    for (int x : nums) {
        std::cout << x << "\n";
    }
    return 0;
}
```

:::
