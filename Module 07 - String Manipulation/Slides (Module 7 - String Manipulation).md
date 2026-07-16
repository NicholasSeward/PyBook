# Module 7 - String Manipulation
## Programming I
### CPSI 17503
#### University of Arkansas at Little Rock

---

## Review from Previous Modules

**Data Structures**
- Lists are ordered, modifiable sequences
- Dictionaries provide key-value mappings
- Tuples are immutable sequences
- Choose appropriate structure for your needs

**Iteration and Processing**
- Loops iterate through sequences
- File processing with loops
- Search algorithms and patterns
- Data processing pipelines

**Function Design**
- Functions can return multiple values
- Parameters and arguments
- Local vs global scope
- Function composition

---

## Learning Objectives

By the end of this module, you will be able to:

1. **Understand strings as sequences** and access individual characters using indexing
2. **Use string slicing** to extract portions of strings efficiently
3. **Apply string methods** for common text manipulation tasks
4. **Work with regular expressions** to find and replace text patterns
5. **Understand ASCII and Unicode** encoding systems
6. **Use escape characters** to represent special characters in strings
7. **Process text files** using string operations and methods
8. **Implement pattern matching** for text analysis and manipulation

---

## Key Terms

**String Fundamentals:**
- String, sequence, character, index, slice
- Immutable, empty string, string methods

**String Operations:**
- Concatenation, comparison, slicing
- startswith, endswith, replace, count

**Regular Expressions:**
- Pattern, regex, search, match, substitution
- Special characters, metacharacters

**Encoding and Characters:**
- ASCII, Unicode, UTF-8, escape characters
- ord(), chr(), encoding, decoding

---

## Content: Strings as Sequences

**What is a String?**
```python
# String is a sequence of characters
fruit = 'banana'
print(f"Length: {len(fruit)}")  # 6
print(f"Type: {type(fruit)}")   # <class 'str'>
```

**Character Access with Indexing**
```python
fruit = 'banana'

# Access individual characters
first = fruit[0]      # 'b'
second = fruit[1]     # 'a'
last = fruit[-1]      # 'a' (last character)
second_last = fruit[-2]  # 'n'
```

**Key Points:**
- Strings are sequences (like lists)
- Zero-based indexing: first character is at index 0
- Negative indices count from the end
- Index must be an integer

---

## Content: String Indexing Examples

**Positive and Negative Indices**
```python
word = 'Python'

# Positive indices
print(f"word[0]: {word[0]}")    # P
print(f"word[1]: {word[1]}")    # y
print(f"word[5]: {word[5]}")    # n

# Negative indices
print(f"word[-1]: {word[-1]}")  # n
print(f"word[-2]: {word[-2]}")  # o
print(f"word[-6]: {word[-6]}")  # P
```

**Index Bounds**
```python
word = 'Python'
length = len(word)  # 6

# Valid indices: 0 to 5
print(f"First: {word[0]}")      # P
print(f"Last: {word[length-1]}") # n
print(f"Last: {word[-1]}")      # n (easier way)

# This would cause IndexError:
# word[6]  # Index out of range
```

---

## Content: String Slicing

**Basic Slicing**
```python
fruit = 'banana'

# Slice from index 0 to 3 (exclusive)
print(fruit[0:3])    # 'ban'

# Slice from index 3 to end
print(fruit[3:])     # 'ana'

# Slice from beginning to index 3
print(fruit[:3])     # 'ban'

# Slice entire string
print(fruit[:])      # 'banana'
```

**Slicing with Steps**
```python
word = 'Python'

# Every second character
print(word[::2])     # 'Pto'

# Reverse the string
print(word[::-1])    # 'nohtyP'

# Every third character
print(word[::3])     # 'Ph'
```

---

## Content: String Slicing Visualization

**Understanding Slice Indices**
```python
fruit = 'banana'
# Indices: 0 1 2 3 4 5
#         b a n a n a

# fruit[1:4] means:
# - Start at index 1 (after 'b')
# - End at index 4 (before second 'n')
# - Result: 'ana'

print(fruit[1:4])    # 'ana'
print(fruit[2:5])    # 'nan'
print(fruit[0:2])    # 'ba'
```

**Empty Slices**
```python
fruit = 'banana'

# When start >= end, result is empty string
print(fruit[3:3])    # '' (empty string)
print(fruit[5:2])    # '' (empty string)

# Useful for checking if slice is valid
if fruit[3:3]:  # This is False (empty string)
    print("Slice has content")
else:
    print("Slice is empty")
```

---

## Content: Strings are Immutable

**Cannot Modify Strings**
```python
greeting = 'Hello, world!'

# This would cause TypeError:
# greeting[0] = 'J'  # TypeError!

# Instead, create a new string
new_greeting = 'J' + greeting[1:]
print(f"Original: {greeting}")      # Hello, world!
print(f"Modified: {new_greeting}")  # Jello, world!
```

**Creating New Strings**
```python
name = 'Alice'

# Change first letter
new_name = 'B' + name[1:]           # 'Blice'

# Change last letter
new_name = name[:-1] + 'y'          # 'Alicy'

# Insert character
new_name = name[:2] + 'x' + name[2:] # 'Alxice'

# Original string unchanged
print(f"Original: {name}")          # Alice
```

---

## Content: String Comparison

**Relational Operators**
```python
word = 'banana'

# Equality
if word == 'banana':
    print('All right, banana.')

# Less than (alphabetical order)
if word < 'apple':
    print('banana comes before apple')
elif word > 'apple':
    print('banana comes after apple')
```

**Case Sensitivity**
```python
# Uppercase comes before lowercase in ASCII
print('Pineapple' < 'banana')  # True
print('pineapple' < 'banana')  # False

# Convert to same case for comparison
word1 = 'Pineapple'.lower()
word2 = 'banana'.lower()
print(word1 < word2)  # True
```

---

## Content: String Methods - Basic Operations

**Case Conversion**
```python
word = 'banana'

# Convert to uppercase
upper_word = word.upper()      # 'BANANA'

# Convert to lowercase
lower_word = word.lower()      # 'banana'

# Capitalize first letter
title_word = word.title()      # 'Banana'

# Swap case
swap_word = word.swapcase()    # 'BANANA' (if word was 'BANANA')
```

**String Information**
```python
text = 'Hello, World!'

# Check if starts with pattern
print(text.startswith('Hello'))    # True
print(text.startswith('World'))    # False

# Check if ends with pattern
print(text.endswith('!'))          # True
print(text.endswith('World'))      # False

# Count occurrences
print(text.count('l'))             # 3
```

---

## Content: String Methods - Search and Replace

**Finding Substrings**
```python
text = 'Hello, World!'

# Find position of substring
position = text.find('World')      # 7
not_found = text.find('Python')    # -1

# Check if substring exists
if 'World' in text:
    print('Found "World"')

# Replace substring
new_text = text.replace('World', 'Python')
print(f"Original: {text}")         # Hello, World!
print(f"Modified: {new_text}")     # Hello, Python!
```

**Multiple Replacements**
```python
sentence = 'The cat and the dog are friends.'

# Replace multiple words
new_sentence = sentence.replace('cat', 'kitten')
new_sentence = new_sentence.replace('dog', 'puppy')

print(f"Original: {sentence}")
print(f"Modified: {new_sentence}")
# Output: The kitten and the puppy are friends.
```

---

## Content: String Methods - Cleaning and Formatting

**Removing Whitespace**
```python
text = '  Hello, World!  '

# Remove leading/trailing whitespace
cleaned = text.strip()              # 'Hello, World!'

# Remove only leading whitespace
left_cleaned = text.lstrip()        # 'Hello, World!  '

# Remove only trailing whitespace
right_cleaned = text.rstrip()       # '  Hello, World!'
```

**Splitting and Joining**
```python
sentence = 'Hello, World, Python'

# Split into list
words = sentence.split(', ')        # ['Hello', 'World', 'Python']

# Join list back into string
new_sentence = ' - '.join(words)    # 'Hello - World - Python'

# Split by spaces
word_list = sentence.split()        # ['Hello,', 'World,', 'Python']
```

---

## Content: File Processing with Strings

**Reading Text Files**
```python
# Open file for reading
reader = open('pg345.txt')

# Process each line
for line in reader:
    # Remove newline character
    line = line.strip()
    
    # Check if line starts with pattern
    if line.startswith('*** '):
        print(f"Special line: {line}")
    
    # Check if line contains pattern
    if 'Dracula' in line:
        print(f"Found Dracula: {line}")

reader.close()
```

**Writing Text Files**
```python
# Open file for writing
writer = open('output.txt', 'w')

# Write lines to file
lines = ['Line 1', 'Line 2', 'Line 3']
for line in lines:
    writer.write(line + '\n')

writer.close()
```

---

## Content: Regular Expressions - Basic Patterns

**Simple Pattern Matching**
```python
import re

text = "I am Dracula; and I bid you welcome, Mr. Harker, to my house."

# Search for pattern
pattern = 'Dracula'
result = re.search(pattern, text)

if result:
    print(f"Found: {result.group()}")      # Found: Dracula
    print(f"Position: {result.span()}")    # Position: (5, 12)
    print(f"Text: {result.string}")        # Full text
else:
    print("Pattern not found")
```

**Pattern Not Found**
```python
import re

text = "I am Dracula; and I bid you welcome, Mr. Harker, to my house."

# Search for pattern that doesn't exist
result = re.search('Count', text)
if result is None:
    print("Pattern not found")
```

---

## Content: Regular Expressions - Special Characters

**Alternation with |**
```python
import re

text = "Mina Murray is a character in Dracula."

# Match either 'Mina' or 'Murray'
pattern = 'Mina|Murray'
result = re.search(pattern, text)

if result:
    print(f"Found: {result.group()}")  # Found: Mina
```

**Anchors: ^ and $**
```python
import re

# Match beginning of string
result1 = re.search('^Dracula', "Dracula is a vampire")
print(f"Starts with Dracula: {result1 is not None}")  # True

# Match end of string
result2 = re.search('Harker$', "The character is Harker")
print(f"Ends with Harker: {result2 is not None}")    # True
```

---

## Content: Regular Expressions - Character Classes

**Optional Characters with ?**
```python
import re

# Match 'colour' or 'color'
pattern = 'colou?r'

text1 = "British spelling: colour"
text2 = "American spelling: color"

result1 = re.search(pattern, text1)  # Matches 'colour'
result2 = re.search(pattern, text2)  # Matches 'color'

print(f"Text1 match: {result1.group() if result1 else 'None'}")
print(f"Text2 match: {result2.group() if result2 else 'None'}")
```

**Grouping with Parentheses**
```python
import re

# Match 'centre' or 'center'
pattern = 'cent(er|re)'

text1 = "British: centre"
text2 = "American: center"

result1 = re.search(pattern, text1)  # Matches 'centre'
result2 = re.search(pattern, text2)  # Matches 'center'
```

---

## Content: Regular Expressions - String Substitution

**Replacing Patterns**
```python
import re

text = "The colour of the centre is beautiful."

# Replace British spelling with American
pattern = 'colou?r'
new_text = re.sub(pattern, 'color', text)

print(f"Original: {text}")
print(f"Modified: {new_text}")
# Output: The color of the centre is beautiful.
```

**Multiple Replacements**
```python
import re

text = "centre colour favour"

# Replace multiple British spellings
patterns = [
    ('cent(er|re)', 'center'),
    ('colou?r', 'color'),
    ('favou?r', 'favor')
]

for pattern, replacement in patterns:
    text = re.sub(pattern, replacement, text)

print(f"Americanized: {text}")
# Output: center color favor
```

---

## Content: ASCII and Unicode - Character Encoding

**ASCII Character Codes**
```python
# ASCII values for common characters
print(f"A = {ord('A')}")      # A = 65
print(f"a = {ord('a')}")      # a = 97
print(f"0 = {ord('0')}")      # 0 = 48
print(f"! = {ord('!')}")      # ! = 33
print(f"space = {ord(' ')}")  # space = 32

# Convert numbers back to characters
print(f"65 = {chr(65)}")      # 65 = A
print(f"97 = {chr(97)}")      # 97 = a
```

**Unicode Support**
```python
# Unicode supports many languages
print(f"English A: {ord('A')}")           # English A: 65
print(f"Greek α: {ord('α')}")             # Greek α: 945
print(f"Chinese 中: {ord('中')}")          # Chinese 中: 20013
print(f"Emoji 😀: {ord('😀')}")           # Emoji 😀: 128512
```

---

## Content: Working with Character Codes

**Character Type Checking**
```python
# Check if character is a letter
def is_letter(char):
    code = ord(char)
    return (65 <= code <= 90) or (97 <= code <= 122)

print(f"Is 'A' a letter? {is_letter('A')}")      # True
print(f"Is '5' a letter? {is_letter('5')}")      # False
print(f"Is '!' a letter? {is_letter('!')}")      # False
```

**Case Conversion with ASCII**
```python
# Convert lowercase to uppercase using ASCII
def to_upper(char):
    if 'a' <= char <= 'z':
        # ASCII: 'a' = 97, 'A' = 65, difference = 32
        return chr(ord(char) - 32)
    return char

print(f"a -> {to_upper('a')}")  # a -> A
print(f"z -> {to_upper('z')}")  # z -> Z
print(f"A -> {to_upper('A')}")  # A -> A
```

---

## Content: Escape Characters - Special Characters

**New Lines and Tabs**
```python
# \n creates a new line
print("Line 1\nLine 2\nLine 3")

# \t creates a tab
print("Name:\tAge:\tCity:")
print("Alice:\t25:\tNew York")
print("Bob:\t30:\tLos Angeles")
```

**Quotes Inside Strings**
```python
# Use backslash to escape quotes
print("She said \"Hello!\"")
print('He said \'Goodbye!\'')

# Or use different quote types
print("She said 'Hello!'")
print('He said "Goodbye!"')
```

**Special Characters**
```python
# Backslash
print("This is a backslash: \\")

# Dollar sign (in f-strings)
price = 10
print(f"The price is \\${price}")

# Percent sign
print("You got 85\\% on the test")
```

---

## Content: Raw Strings and File Paths

**Raw Strings**
```python
# Normal string - \n becomes new line
normal = "C:\new\file.txt"
print(f"Normal: {normal}")

# Raw string - \n stays as \n
raw = r"C:\new\file.txt"
print(f"Raw: {raw}")
```

**File Paths**
```python
# File path with escape characters
file_path = "C:\\Users\\Student\\Documents\\file.txt"
print(f"File path: {file_path}")

# Or use raw string
file_path_raw = r"C:\Users\Student\Documents\file.txt"
print(f"File path (raw): {file_path_raw}")

# Both are the same
print(f"Are they equal? {file_path == file_path_raw}")
```

---

## Content: Multi-line Strings

**Using \n for Multi-line**
```python
# Create multi-line text with \n
poem = "Roses are red,\nViolets are blue,\nPython is fun,\nAnd so are you!"
print(poem)
```

**Using Triple Quotes**
```python
# Triple quotes for multi-line strings
poem = """Roses are red,
Violets are blue,
Python is fun,
And so are you!"""
print(poem)
```

**Formatted Tables**
```python
# Create a formatted table
print("Name\t\tAge\tCity")
print("-" * 30)
print("Alice\t\t25\tNew York")
print("Bob\t\t30\tLos Angeles")
print("Charlie\t\t35\tChicago")
```

---

## Content: Real-world Applications

**Text Processing Pipeline**
```python
def process_text_file(filename):
    """Process a text file and extract information."""
    word_count = {}
    
    with open(filename, 'r') as file:
        for line in file:
            # Clean the line
            line = line.strip().lower()
            
            # Skip empty lines
            if not line:
                continue
                
            # Split into words
            words = line.split()
            
            # Count words
            for word in words:
                word_count[word] = word_count.get(word, 0) + 1
    
    return word_count

# Usage
word_freq = process_text_file('sample.txt')
for word, count in sorted(word_freq.items()):
    print(f"{word}: {count}")
```

**Pattern Matching for Data Extraction**
```python
import re

def extract_phone_numbers(text):
    """Extract phone numbers from text."""
    # Pattern for phone numbers: (XXX) XXX-XXXX
    pattern = r'\(\d{3}\) \d{3}-\d{4}'
    
    matches = re.findall(pattern, text)
    return matches

# Test
text = "Call me at (555) 123-4567 or (555) 987-6543"
phone_numbers = extract_phone_numbers(text)
print(f"Found phone numbers: {phone_numbers}")
```

---

## Content: Debugging String Operations

**Common String Issues**
```python
# Issue 1: Index out of range
text = "Hello"
try:
    char = text[10]  # IndexError!
except IndexError:
    print("Index out of range")

# Issue 2: Immutability
text = "Hello"
# text[0] = 'h'  # TypeError!

# Issue 3: String vs list confusion
text = "Hello"
# text.append('!')  # AttributeError!
```

**Debugging Strategies**
```python
# Add print statements to see string state
text = "Hello, World!"
print(f"Original: '{text}'")
print(f"Length: {len(text)}")
print(f"First char: '{text[0]}'")
print(f"Last char: '{text[-1]}'")

# Check string properties
print(f"Starts with 'Hello': {text.startswith('Hello')}")
print(f"Contains 'World': {'World' in text}")
print(f"Ends with '!': {text.endswith('!')}")
```

---

## Dos and Don'ts

**DO:**
- ✅ Use string methods instead of manual character manipulation
- ✅ Use raw strings (r"...") for file paths and regex patterns
- ✅ Handle encoding properly when working with international text
- ✅ Use appropriate string methods for common operations
- ✅ Test string operations with edge cases (empty strings, special characters)
- ✅ Use regular expressions for complex pattern matching

**DON'T:**
- ❌ Try to modify strings directly (they're immutable)
- ❌ Forget that string indices start at 0
- ❌ Ignore case sensitivity in string comparisons
- ❌ Use string operations when regex would be more appropriate
- ❌ Forget to handle encoding issues with non-ASCII text
- ❌ Use complex string operations when built-in methods exist

---

## Key Takeaways

**String Fundamentals:**
- Strings are immutable sequences of characters
- Use indexing and slicing to access parts of strings
- String methods provide powerful text manipulation capabilities

**Pattern Matching:**
- Regular expressions offer flexible pattern matching
- Use regex for complex text search and replacement
- Understand special characters and metacharacters

**Text Processing:**
- Combine string operations for text analysis
- Handle encoding properly for international text
- Use appropriate tools for the task at hand

**Best Practices:**
- Choose string methods over manual manipulation
- Use raw strings for patterns and file paths
- Test with various input types and edge cases

---

## Further Explorations

**Advanced Regular Expressions:**
- Explore more complex regex patterns and quantifiers
- Learn about lookahead and lookbehind assertions
- Study regex optimization and performance considerations

**Text Processing Libraries:**
- Investigate libraries like `nltk` for natural language processing
- Explore `BeautifulSoup` for HTML/XML parsing
- Learn about `pandas` for structured text data analysis

**Internationalization:**
- Study Unicode normalization and text comparison
- Learn about locale-specific string operations
- Explore text processing in different languages and scripts

**Performance and Optimization:**
- Understand string concatenation efficiency
- Learn about string interning and memory optimization
- Study regex compilation and caching strategies

**Real-world Applications:**
- Web scraping and data extraction
- Natural language processing and text analysis
- Data cleaning and preprocessing
- Configuration file parsing and generation
