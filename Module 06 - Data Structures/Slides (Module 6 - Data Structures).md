# Module 6 - Data Structures
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

**Iteration and Loops**
- `for` loops iterate through sequences
- `while` loops repeat while condition is true
- Loop control statements provide flexibility: `break`, `continue`, `pass`
- Accumulators and counters are essential tools for tracking information
- Choose between index-based and direct iteration based on program needs

**Basic Data Processing**
- Strings are sequences of characters
- File processing is manageable with loops
- Linear search is a fundamental algorithm
- Use built-in operators for efficient data processing

---

## Learning Objectives

By the end of this module, you will be able to:

1. **Create and manipulate lists** using indexing, slicing, and methods
2. **Understand mutability** and how it affects data structures
3. **Use list methods** for adding, removing, and organizing data
4. **Create and work with dictionaries** as key-value mappings
5. **Understand tuples** and their immutability characteristics
6. **Choose appropriate data structures** for different programming tasks
7. **Implement stacks and queues** using list methods
8. **Handle nested data structures** and complex data organization

---

## Key Terms

**Lists:**
- List, element, index, slice, mutable
- append, insert, remove, pop, sort

**Dictionaries:**
- Dictionary, key, value, mapping, item
- hashable, KeyError, nested dictionary

**Tuples:**
- Tuple, immutable, sequence, packing/unpacking
- hashable, single-element tuple

**Data Structure Concepts:**
- Mutability, immutability, shallow copy, deep copy
- Stack, queue, LIFO, FIFO

---

## Content: Lists - Basic Creation

**Creating Lists**
```python
# Empty list
empty = []

# List with elements
numbers = [42, 123]
cheeses = ['Cheddar', 'Edam', 'Gouda']

# Mixed types allowed
mixed = ['spam', 2.0, 5, [10, 20]]

# Nested lists
nested = [[1, 2], [3, 4], [5, 6]]
```

**List Properties**
- Lists are sequences (like strings)
- Elements can be any type
- Lists can contain other lists
- Length determined by `len()` function
- Zero-based indexing

---

## Content: List Indexing and Slicing

**Accessing Elements**
```python
fruits = ['apple', 'banana', 'orange', 'grape']

# Single element access
first = fruits[0]      # 'apple'
last = fruits[-1]      # 'grape'
second = fruits[1]     # 'banana'
```

**List Slicing**
```python
fruits = ['apple', 'banana', 'orange', 'grape']

# Slice from index 1 to 3 (exclusive)
middle = fruits[1:3]   # ['banana', 'orange']

# Slice from beginning
start = fruits[:2]      # ['apple', 'banana']

# Slice to end
end = fruits[2:]        # ['orange', 'grape']

# Slice with step
every_other = fruits[::2]  # ['apple', 'orange']
```

---

## Content: Lists are Mutable

**Modifying Lists**
```python
numbers = [42, 123, 17]

# Change element at index
numbers[1] = 999
print(numbers)  # [42, 999, 17]

# Add new element
numbers.append(50)
print(numbers)  # [42, 999, 17, 50]

# Remove element
numbers.remove(999)
print(numbers)  # [42, 17, 50]
```

**Key Point:**
- Lists can be changed after creation
- Multiple variables can reference the same list
- Changes affect all references to the list

---

## Content: List Methods - Adding Items

**append() - Add to End**
```python
fruits = ["apple", "banana"]
fruits.append("orange")
print(fruits)  # ['apple', 'banana', 'orange']
```

**insert() - Add at Position**
```python
fruits = ["apple", "banana"]
fruits.insert(1, "grape")  # Insert at position 1
print(fruits)  # ['apple', 'grape', 'banana']
```

**extend() - Add Multiple Items**
```python
fruits = ["apple", "banana"]
more_fruits = ["orange", "grape"]
fruits.extend(more_fruits)
print(fruits)  # ['apple', 'banana', 'orange', 'grape']
```

---

## Content: List Methods - Removing Items

**remove() - Remove by Value**
```python
fruits = ["apple", "banana", "orange", "banana"]
fruits.remove("banana")  # Removes first "banana"
print(fruits)  # ['apple', 'orange', 'banana']
```

**pop() - Remove by Position**
```python
fruits = ["apple", "banana", "orange"]
last_fruit = fruits.pop()  # Remove and return last item
print(f"Removed: {last_fruit}")  # Removed: orange
print(f"Remaining: {fruits}")    # Remaining: ['apple', 'banana']

first_fruit = fruits.pop(0)  # Remove and return first item
print(f"Removed: {first_fruit}")  # Removed: apple
```

**del - Remove by Position**
```python
fruits = ["apple", "banana", "orange"]
del fruits[1]  # Remove item at position 1
print(fruits)  # ['apple', 'orange']
```

---

## Content: List Methods - Finding and Organizing

**Finding Items**
```python
fruits = ["apple", "banana", "orange"]

# Find position
position = fruits.index("banana")  # 1

# Count occurrences
apple_count = fruits.count("apple")  # 1

# Check if exists
if "banana" in fruits:
    print("We have bananas!")
```

**Sorting and Reversing**
```python
numbers = [3, 1, 4, 1, 5, 9, 2, 6]
numbers.sort()  # Sort in place
print(numbers)  # [1, 1, 2, 3, 4, 5, 6, 9]

fruits = ["banana", "apple", "cherry"]
fruits.sort()
print(fruits)  # ['apple', 'banana', 'cherry']

# Reverse order
numbers.reverse()
print(numbers)  # [9, 6, 5, 4, 3, 2, 1, 1]
```

---

## Content: Stacks and Queues with Lists

**Stack (LIFO - Last In, First Out)**
```python
# Stack operations using list methods
stack = []

# Push (add to top)
stack.append("first")
stack.append("second")
stack.append("third")

# Pop (remove from top)
top_item = stack.pop()  # "third"
next_item = stack.pop() # "second"

print(f"Stack: {stack}")  # ['first']
```

**Queue (FIFO - First In, First Out)**
```python
# Queue operations using list methods
queue = []

# Enqueue (add to end)
queue.append("first")
queue.append("second")
queue.append("third")

# Dequeue (remove from front)
first_item = queue.pop(0)  # "first"
next_item = queue.pop(0)   # "second"

print(f"Queue: {queue}")  # ['third']
```

---

## Content: Dictionaries - Basic Concepts

**What is a Dictionary?**
```python
# Dictionary maps keys to values
student = {
    "name": "Alice",
    "age": 20,
    "grade": 85.5,
    "courses": ["Math", "Physics"]
}

# Keys can be strings, numbers, or tuples
# Values can be any type
```

**Creating Dictionaries**
```python
# Empty dictionary
empty = {}

# Dictionary with initial values
numbers = {'zero': 0, 'one': 1, 'two': 2}

# Using dict() function
another = dict()
copy = dict(numbers)
```

---

## Content: Dictionary Operations

**Adding and Modifying**
```python
student = {}

# Add new key-value pair
student["name"] = "Alice"
student["age"] = 20

# Modify existing value
student["age"] = 21

# Add multiple items
student.update({"grade": 85, "major": "Computer Science"})

print(student)  # {'name': 'Alice', 'age': 21, 'grade': 85, 'major': 'Computer Science'}
```

**Accessing Values**
```python
student = {"name": "Alice", "age": 20, "grade": 85}

# Get value by key
name = student["name"]  # "Alice"

# Check if key exists
if "age" in student:
    age = student["age"]

# Get with default value
phone = student.get("phone", "Not provided")
```

---

## Content: Dictionary Methods

**Common Dictionary Methods**
```python
student = {"name": "Alice", "age": 20, "grade": 85}

# Get all keys
keys = list(student.keys())  # ['name', 'age', 'grade']

# Get all values
values = list(student.values())  # ['Alice', 20, 85]

# Get all items
items = list(student.items())  # [('name', 'Alice'), ('age', 20), ('grade', 85)]

# Remove item
removed_grade = student.pop("grade")  # 85

# Clear all items
student.clear()  # {}
```

**Iterating Through Dictionaries**
```python
student = {"name": "Alice", "age": 20, "grade": 85}

# Iterate through keys
for key in student:
    print(f"{key}: {student[key]}")

# Iterate through items
for key, value in student.items():
    print(f"{key}: {value}")
```

---

## Content: Nested Dictionaries

**Complex Data Structures**
```python
# Student with nested information
student = {
    "name": "Alice",
    "contact": {
        "email": "alice@email.com",
        "phone": "555-1234"
    },
    "grades": {
        "Math": 85,
        "Physics": 92,
        "English": 78
    }
}

# Access nested values
email = student["contact"]["email"]  # "alice@email.com"
math_grade = student["grades"]["Math"]  # 85

# Modify nested values
student["grades"]["English"] = 80
```

**Real-world Example**
```python
# Library catalog system
books = {
    "1984": {
        "author": "George Orwell",
        "year": 1949,
        "copies": 3,
        "available": True
    },
    "Brave New World": {
        "author": "Aldous Huxley",
        "year": 1932,
        "copies": 2,
        "available": False
    }
}
```

---

## Content: Tuples - Immutable Sequences

**Creating Tuples**
```python
# Tuple with multiple elements
coordinates = (10, 20)
colors = ('red', 'green', 'blue')

# Single element tuple (note the comma)
single = (42,)

# Tuple from sequence
letters = tuple('hello')  # ('h', 'e', 'l', 'l', 'o')

# Empty tuple
empty = ()
```

**Tuple Operations**
```python
t = ('a', 'b', 'c')

# Indexing and slicing work like lists
first = t[0]      # 'a'
middle = t[1:3]   # ('b', 'c')

# Concatenation
combined = t + ('d', 'e')  # ('a', 'b', 'c', 'd', 'e')

# Repetition
repeated = t * 2   # ('a', 'b', 'c', 'a', 'b', 'c')
```

---

## Content: Tuples are Immutable

**Cannot Modify Tuples**
```python
coordinates = (10, 20)

# This would cause an error:
# coordinates[0] = 15  # TypeError!

# Instead, create a new tuple
new_coordinates = (15, 20)

# Or modify a copy
coords_list = list(coordinates)
coords_list[0] = 15
new_coords = tuple(coords_list)
```

**Why Immutability Matters**
```python
# Tuples can be used as dictionary keys
point_counts = {}
point_counts[(1, 2)] = 5
point_counts[(3, 4)] = 10

# Lists cannot be keys (they're mutable)
# This would cause an error:
# point_counts[[1, 2]] = 5  # TypeError!
```

---

## Content: Tuple Packing and Unpacking

**Packing Values into Tuples**
```python
# Multiple values automatically packed into tuple
point = 10, 20
print(point)  # (10, 20)
print(type(point))  # <class 'tuple'>

# Function returning multiple values
def get_coordinates():
    x = 10
    y = 20
    return x, y  # Automatically packed into tuple

coords = get_coordinates()  # (10, 20)
```

**Unpacking Tuples**
```python
# Unpack tuple into variables
x, y = (10, 20)
print(f"x: {x}, y: {y}")  # x: 10, y: 20

# Multiple assignment
a, b, c = (1, 2, 3)

# Swap variables
a, b = 1, 2
a, b = b, a  # Swap using tuple unpacking
print(f"a: {a}, b: {b}")  # a: 2, b: 1
```

---

## Content: Immutable vs Mutable

**Mutable Types (Can Change)**
```python
# Lists - can be modified
fruits = ["apple", "banana"]
fruits[0] = "orange"  # Change first item
fruits.append("grape")  # Add new item

# Dictionaries - can be modified
student = {"name": "Alice", "grade": 85}
student["grade"] = 90  # Change value
student["age"] = 20    # Add new key
```

**Immutable Types (Cannot Change)**
```python
# Strings - cannot be modified
name = "Alice"
# name[0] = "B"  # This would cause an error!

# Tuples - cannot be modified
coordinates = (10, 20)
# coordinates[0] = 15  # This would cause an error!

# Numbers - cannot be modified
x = 5
# x = 6  # This creates a new number, doesn't change 5
```

---

## Content: Understanding References

**Multiple References to Same Object**
```python
# Two variables point to the same list
list1 = [1, 2, 3]
list2 = list1  # Both point to the same list

list2.append(4)  # Change the list
print(f"list1: {list1}")  # [1, 2, 3, 4]
print(f"list2: {list2}")  # [1, 2, 3, 4]
```

**Creating Copies**
```python
# Shallow copy
original = [1, 2, 3]
copy = original.copy()  # or list(original)

copy.append(4)
print(f"Original: {original}")  # [1, 2, 3]
print(f"Copy: {copy}")          # [1, 2, 3, 4]

# Deep copy for nested structures
import copy
nested = [[1, 2], [3, 4]]
deep_copy = copy.deepcopy(nested)
```

---

## Content: Choosing Data Structures

**When to Use Lists**
```python
# Use lists when you need:
# - Ordered collection of items
# - Ability to modify items
# - Index-based access
# - Stack or queue operations

# Examples:
shopping_list = ["milk", "bread", "eggs"]
scores = [85, 92, 78, 96, 88]
```

**When to Use Dictionaries**
```python
# Use dictionaries when you need:
# - Key-value associations
# - Fast lookups by key
# - Unordered collection
# - Complex data relationships

# Examples:
student_info = {"name": "Alice", "id": "12345"}
word_count = {"the": 150, "and": 120, "is": 100}
```

**When to Use Tuples**
```python
# Use tuples when you need:
# - Immutable sequence
# - Dictionary keys
# - Function return values
# - Data that shouldn't change

# Examples:
coordinates = (10, 20)
rgb_color = (255, 128, 0)
date = (2024, 1, 15)
```

---

## Content: Common Patterns and Use Cases

**Data Processing Pipeline**
```python
# Process student grades
students = [
    {"name": "Alice", "grades": [85, 92, 78]},
    {"name": "Bob", "grades": [90, 88, 95]},
    {"name": "Charlie", "grades": [75, 80, 82]}
]

# Calculate averages
for student in students:
    grades = student["grades"]
    average = sum(grades) / len(grades)
    student["average"] = round(average, 1)

# Sort by average
students.sort(key=lambda s: s["average"], reverse=True)

# Display results
for student in students:
    print(f"{student['name']}: {student['average']}")
```

**Word Frequency Analysis**
```python
# Count word frequencies
text = "the quick brown fox jumps over the lazy dog"
words = text.split()

word_count = {}
for word in words:
    if word in word_count:
        word_count[word] += 1
    else:
        word_count[word] = 1

# Sort by frequency
sorted_words = sorted(word_count.items(), key=lambda x: x[1], reverse=True)
print(sorted_words)
```

---

## Content: Error Handling and Best Practices

**Common Dictionary Errors**
```python
student = {"name": "Alice", "grade": 85}

# KeyError when key doesn't exist
try:
    age = student["age"]  # KeyError!
except KeyError:
    print("Age not found")

# Safe way to access
age = student.get("age", "Not provided")
phone = student.get("phone", "No phone")
```

**List Index Errors**
```python
fruits = ["apple", "banana", "orange"]

# IndexError when index out of range
try:
    fruit = fruits[5]  # IndexError!
except IndexError:
    print("Index out of range")

# Safe way to access
if len(fruits) > 5:
    fruit = fruits[5]
else:
    print("Index too large")
```

---

## Content: Performance Considerations

**List Operations Complexity**
```python
# Fast operations (O(1))
fruits = ["apple", "banana", "orange"]
first = fruits[0]        # Indexing
fruits.append("grape")   # Append to end
last = fruits[-1]        # Last element

# Slower operations (O(n))
fruits.insert(0, "kiwi")  # Insert at beginning
fruits.remove("banana")    # Remove by value
"apple" in fruits          # Search
```

**Dictionary Operations**
```python
# Fast operations (O(1) average case)
student = {"name": "Alice", "grade": 85}
name = student["name"]     # Lookup by key
student["age"] = 20        # Add/modify
"name" in student          # Check key exists

# Slower operations (O(n))
values = list(student.values())  # Get all values
items = list(student.items())    # Get all items
```

---

## Dos and Don'ts

**DO:**
- ✅ Use lists for ordered, modifiable collections
- ✅ Use dictionaries for key-value mappings
- ✅ Use tuples for immutable sequences
- ✅ Create copies when you need independent data
- ✅ Handle missing keys safely with `.get()` method
- ✅ Choose appropriate data structure for your needs
- ✅ Use list methods for common operations

**DON'T:**
- ❌ Modify lists while iterating through them
- ❌ Use lists as dictionary keys
- ❌ Forget that dictionaries are unordered (before Python 3.7)
- ❌ Assume all references point to different objects
- ❌ Use wrong data structure for the task
- ❌ Ignore error handling for missing keys/indices

---

## Key Takeaways

**Data Structure Selection:**
- Lists: Ordered, modifiable sequences
- Dictionaries: Key-value mappings with fast lookups
- Tuples: Immutable sequences, good for keys

**Mutability Matters:**
- Mutable objects can be changed after creation
- Immutable objects cannot be changed
- Multiple references to mutable objects share the same data

**Common Patterns:**
- Stacks and queues using list methods
- Nested data structures for complex information
- Data processing pipelines with multiple structures

**Performance Considerations:**
- Choose appropriate structure for your operations
- Understand complexity of common operations
- Use built-in methods when possible

---

## Further Explorations

- **Advanced Data Structures:** Explore data structures like sets, heaps, and graphs to understand their use cases and performance benefits.
- **Data Structure Libraries:** Investigate Python libraries such as `collections` and `numpy` for specialized data structures and operations.
- **Algorithm Efficiency:** Study how different data structures affect the efficiency of algorithms, focusing on time and space complexity.
- **Data Persistence:** Learn about data serialization and persistence techniques using formats like JSON, CSV, and databases.
- **Functional Programming:** Delve into functional programming paradigms and how they can be applied to data processing tasks.
- **Concurrency and Parallelism:** Explore how data structures can be used in concurrent and parallel programming to improve performance.

---


