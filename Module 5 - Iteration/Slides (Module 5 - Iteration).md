# Module 5 - Iteration
## Programming I
### CPSI 17503
#### University of Arkansas at Little Rock

---

## Review from Previous Modules

**Function Basics**
- Functions are defined with `def` keyword
- Parameters receive arguments when called
- Functions can return values or perform actions
- Local variables exist only within functions

**Conditionals and Control Flow**
- `if`, `elif`, `else` statements control execution
- Boolean expressions use `and`, `or`, `not`
- Functions can have multiple return statements

**Basic Recursion**
- Functions can call themselves
- Must have base case to stop recursion
- Recursive functions can return values

---

## Learning Objectives

By the end of this module, you will be able to:

1. **Use `for` loops** to iterate through strings, lists, and other sequences
2. **Implement `while` loops** for conditional iteration
3. **Apply loop control statements** (`break`, `continue`, `pass`) to manage loop behavior
4. **Use accumulators and counters** to track information during iteration
5. **Choose between index-based and direct iteration** based on program needs
6. **Implement search algorithms** using linear search patterns
7. **Process file data** by iterating through file contents
8. **Write efficient loops** that avoid common iteration pitfalls

---

## Key Terms

**Loop Types:**
- `for` loop, `while` loop, loop variable
- Iteration, sequence, range function

**Loop Control:**
- `break`, `continue`, `pass`
- Loop termination, iteration skipping

**Search and Processing:**
- Linear search, accumulator, counter
- File object, method, update

**Iteration Patterns:**
- Index-based iteration, direct iteration
- Loop initialization, loop termination

---

## For Loops with Strings

**Iterating Through Characters**
```python
for letter in 'Gadsby':
    print(letter, end=' ')
# Output: G a d s b y
```

**Loop Variables**
- Variable name should be descriptive
- `i` for numbers, `letter` for characters, `word` for words
- Each iteration assigns next value to loop variable

**Checking for Specific Characters**
```python
def has_e(word):
    for letter in word:
        if letter == 'E' or letter == 'e':
            return True
    return False

print(has_e('Gadsby'))  # False
print(has_e('Emma'))    # True
```

---

## For Loops with range()

**Counting with range()**
```python
for i in range(3):
    print(i, end=' ')
# Output: 0 1 2
```

**range() Function Options**
```python
range(5)        # 0, 1, 2, 3, 4
range(1, 6)     # 1, 2, 3, 4, 5
range(0, 10, 2) # 0, 2, 4, 6, 8
```

**Common Patterns**
```python
# Count from 1 to n
for i in range(1, n + 1):
    print(i)

# Count backwards
for i in range(n, 0, -1):
    print(i)
```

---

## While Loops

**Conditional Iteration**
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

**Key Components:**
- **Condition**: Boolean expression that controls loop
- **Loop body**: Code that executes each iteration
- **Update**: Must change condition to avoid infinite loop

**Common Pattern:**
```python
# Initialize
variable = starting_value

# Loop condition
while condition:
    # Do something
    # Update variable
    variable = new_value
```

---

## Loop Control - break

**Stopping Loops Early**
```python
def find_first_vowel(word):
    for char in word:
        if char in "aeiou":
            return char  # Exit function immediately
    return None  # No vowels found
```

**break Statement**
```python
word = "programming"
for char in word:
    if char == 'a':
        print(f"Found: {char}")
        break  # Stop loop completely
    print(f"Checking {char}...")
```

**When to Use:**
- Found what you're looking for
- Error condition encountered
- Early termination needed

---

## Loop Control - continue

**Skipping Iterations**
```python
# Print only vowels
word = "programming"
for char in word:
    if char not in "aeiou":  # If not vowel
        continue              # Skip to next character
    print(f"Vowel: {char}")
```

**continue Statement**
- Skips rest of current iteration
- Goes to next iteration immediately
- Loop continues running

**Common Use Cases:**
- Skip invalid data
- Skip items that don't meet criteria
- Handle special cases separately

---

## Loop Control - pass

**Placeholder Statement**
```python
# Check character types
word = "Hello123"
for char in word:
    if char.isalpha():
        print(f"{char} is a letter")
    elif char.isdigit():
        print(f"{char} is a digit")
    else:
        pass  # Do nothing for other characters
```

**pass Statement**
- Does nothing
- Useful as placeholder
- Rarely needed in simple programs

**When to Use:**
- Empty function or class (temporary)
- Placeholder for future code
- Syntactically required but no action needed

---

## Accumulators and Counters

**Counters - Track Occurrences**
```python
# Count vowels in a word
word = "programming"
vowel_count = 0  # Initialize counter

for letter in word:
    if letter in "aeiou":
        vowel_count += 1  # Increment counter

print(f"Found {vowel_count} vowels")
```

**Accumulators - Sum Values**
```python
# Sum digits in a number
number = 12345
total = 0  # Initialize accumulator

for digit in str(number):
    total += int(digit)  # Add to accumulator

print(f"Sum of digits: {total}")
```

---

## Finding Maximum/Minimum

**Finding Maximum Character**
```python
word = "programming"
highest = word[0]  # Start with first character

for char in word:
    if char > highest:
        highest = char  # Update if higher found

print(f"Highest character: {highest}")
```

**Finding Minimum Character**
```python
word = "programming"
lowest = word[0]  # Start with first character

for char in word:
    if char < lowest:
        lowest = char  # Update if lower found

print(f"Lowest character: {lowest}")
```

**Key Points:**
- Initialize with first item (not 0)
- Compare and update in loop
- Works for any comparable data type

---

## Building Strings During Iteration

**Collecting Characters**
```python
# Collect vowels from a word
word = "programming"
vowels = ""  # Start with empty string

for char in word:
    if char in "aeiou":
        vowels += char  # Add to string

print(f"Vowels found: {vowels}")
```

**Filtering Characters**
```python
# Find uppercase letters
text = "Hello World"
uppercase = ""

for char in text:
    if char.isupper():
        uppercase += char

print(f"Uppercase letters: {uppercase}")
```

**Key Points:**
- Start with empty string `""`
- Use `+=` to add characters
- Apply conditions to filter data

---

## Index-based vs Direct Iteration

**Direct Iteration (Recommended)**
```python
word = "python"

# Loop through characters directly
for char in word:
    print(f"Character: {char}")
```

**Index-based Iteration**
```python
word = "python"

# Loop through indexes
for i in range(len(word)):
    print(f"Position {i}: {word[i]}")
```

**When to Use Each:**
- **Direct**: When you just need the characters
- **Index-based**: When you need position or control

---

## Comparing Strings Character by Character

**Comparing Two Strings**
```python
word1 = "hello"
word2 = "hello"

same = True
for i in range(len(word1)):
    if word1[i] != word2[i]:
        same = False
        break

print(f"Strings are identical: {same}")
```

**Finding Differences**
```python
word1 = "hello"
word2 = "hallo"

for i in range(len(word1)):
    if word1[i] != word2[i]:
        print(f"Difference at position {i}: '{word1[i]}' vs '{word2[i]}'")
```

**Benefits of Character Comparison:**
- Useful for text analysis
- Helps find specific differences
- Foundation for string processing

---

## File Processing with Loops

**Reading Files Line by Line**
```python
# Open and read file
file_object = open('words.txt')

# Read first line
first_line = file_object.readline()
print(first_line)  # "aah\n"

# Remove newline character
word = first_line.strip()
print(word)  # "aah"
```

**Processing Entire File**
```python
# Loop through all lines in file
for line in open('words.txt'):
    word = line.strip()
    print(word)
```

**File Object Methods:**
- `readline()`: Read one line
- `strip()`: Remove whitespace/newlines
- File objects are iterable in for loops

---

## Linear Search Pattern

**Searching for Elements**
```python
def uses_any(word, letters):
    """Check if word uses any of the letters."""
    for letter in word.lower():
        if letter in letters.lower():
            return True  # Found one!
    return False  # Checked all, found none

# Test the function
print(uses_any('banana', 'aeiou'))  # True
print(uses_any('apple', 'xyz'))     # False
```

**Linear Search Characteristics:**
- Check each element one by one
- Stop when found (early return)
- Return False if not found after checking all
- Time complexity: O(n)

---

## The 'in' Operator

**Simplified String Search**
```python
word = 'Gadsby'

# Check if letter exists
print('e' in word)      # False
print('a' in word)      # True

# Case-insensitive search
print('E' in word.upper())  # False
print('A' in word.upper())  # True
```

**Rewriting has_e Function**
```python
def has_e(word):
    return 'e' in word.lower()

# Much simpler than loop version!
print(has_e('Gadsby'))  # False
print(has_e('Emma'))    # True
```

**Benefits:**
- More readable
- More efficient
- Built-in Python functionality

---

## Processing Word Lists

**Counting Words with 'e'**
```python
def count_words_with_e(filename):
    count = 0
    total = 0
    
    for line in open(filename):
        word = line.strip()
        total += 1
        
        if has_e(word):
            count += 1
    
    return count, total

# Calculate percentage
e_count, total_words = count_words_with_e('words.txt')
percentage = (e_count / total_words) * 100
print(f"{percentage:.1f}% of words contain 'e'")
```

**Key Patterns:**
- Initialize counters before loop
- Process each line/word
- Update counters during iteration
- Calculate results after loop

---

## Nested Loops

**Loops Inside Loops**
```python
# Print character patterns
word = "ABC"
for i in range(len(word)):
    for j in range(i + 1):
        print(word[j], end="")
    print()  # New line after each row
```

**Processing Character Combinations**
```python
# Find all character pairs
word = "ABC"
for i in range(len(word)):
    for j in range(i + 1, len(word)):
        print(f"{word[i]}{word[j]}")
```

**Important Considerations:**
- Inner loop runs completely for each outer iteration
- Can be computationally expensive
- Use when you need to process all combinations

---

## Loop Efficiency

**Avoiding Unnecessary Work**
```python
# Good: Early return when found
def find_vowel(word):
    for char in word:
        if char in "aeiou":
            return char  # Stop immediately
    return None

# Less efficient: Always check all characters
def find_vowel_slow(word):
    result = None
    for char in word:
        if char in "aeiou":
            result = char
    return result
```

**Efficiency Tips:**
- Use `break` or early `return` when possible
- Avoid unnecessary iterations
- Choose appropriate loop type
- Consider data structure for search operations

---

## Common Loop Patterns

**Pattern 1: Count and Accumulate**
```python
word = "hello"
count = 0
total = 0

for char in word:
    count += 1
    total += ord(char)  # ASCII value

average = total / count
print(f"Average ASCII: {average}")
```

**Pattern 2: Find and Replace Characters**
```python
word = "hello"
new_word = ""

for char in word:
    if char == "l":
        new_word += "x"
    else:
        new_word += char

print(new_word)
```

**Pattern 3: Validate All Characters**
```python
word = "Hello123"
all_letters = True

for char in word:
    if not char.isalpha():
        all_letters = False
        break

print(f"All characters are letters: {all_letters}")
```

---

## Debugging Loops

**Common Loop Issues**
```python
# Issue 1: Forgetting to initialize
total = 0  # Don't forget this!
for num in numbers:
    total += num

# Issue 2: Infinite while loops
count = 0
while count < 5:  # Make sure condition changes!
    print(count)
    count += 1    # Don't forget this!

# Issue 3: Off-by-one errors
for i in range(5):  # 0, 1, 2, 3, 4 (not 1, 2, 3, 4, 5)
    print(i)
```

**Debugging Strategies:**
- Add print statements to see loop progress
- Check loop variable values
- Verify loop termination conditions
- Test with small, known data sets

---

## Dos and Don'ts

**DO:**
- ✅ Initialize counters and accumulators before loops
- ✅ Use descriptive loop variable names
- ✅ Use `break` for early termination when appropriate
- ✅ Choose direct iteration when you don't need indexes
- ✅ Use `zip()` for multiple lists
- ✅ Test loops with small data sets first
- ✅ Consider loop efficiency for large datasets

**DON'T:**
- ❌ Forget to update loop variables in while loops
- ❌ Use index-based iteration when direct iteration suffices
- ❌ Nest loops unnecessarily
- ❌ Forget to handle edge cases (empty lists, etc.)
- ❌ Use loops when built-in functions would work
- ❌ Ignore loop termination conditions
- ❌ Process data multiple times in the same loop

---

## Key Takeaways

**Loops are Fundamental:**
- `for` loops iterate through sequences
- `while` loops repeat while condition is true
- Loop control statements provide flexibility

**Patterns Matter:**
- Accumulators and counters are essential tools
- Linear search is a fundamental algorithm
- Choose iteration method based on needs

**Efficiency Considerations:**
- Early termination improves performance
- Appropriate loop type matters
- Built-in operators often better than custom loops

**File Processing:**
- Loops make file processing manageable
- Text processing benefits from iteration
- Word analysis demonstrates loop power

---

## Next Steps

**Practice Exercises:**
1. Write functions that search through word lists
2. Implement different counting and accumulation patterns
3. Process real data files with loops
4. Create nested loop solutions for complex problems

**Advanced Topics to Explore:**
- List comprehensions (more Pythonic loops)
- Generator expressions and iterators
- Functional programming with map/filter/reduce
- Performance optimization techniques

**Real-world Applications:**
- Data analysis and processing
- Text analysis and natural language processing
- Game development and simulation
- Scientific computing and research

**Resources:**
- Python documentation on loops and iteration
- Practice problems on coding platforms
- Data processing libraries (pandas, numpy)
- Algorithm analysis and complexity theory