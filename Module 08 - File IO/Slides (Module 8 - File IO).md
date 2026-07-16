# Module 8 - File I/O
## Programming I
### CPSI 17503
#### University of Arkansas at Little Rock

---

## Review from Previous Modules

### Variables and Data Types
- Understanding how data is stored in memory
- Different data types (strings, lists, dictionaries)
- How data persists only during program execution

### Functions and Scope
- How functions can work with data
- Local vs global variable scope
- Return values and data passing

### String Operations
- String methods and manipulation
- Working with text data
- String formatting and concatenation

---

## Learning Objectives

By the end of this module, you will be able to:

1. **Read and write text files** using Python's built-in file operations
2. **Understand file open modes** and choose the appropriate mode for different operations
3. **Compare line-by-line vs all-at-once reading** and choose the best approach
4. **Serialize and deserialize data** using Python's pickle module
5. **Handle file errors gracefully** using try-except blocks
6. **Work with file paths** and understand relative vs absolute paths
7. **Apply basic database concepts** for data persistence

---

## Key Terms

**File I/O** - Input/Output operations for reading and writing files

**File Handle** - A connection between your program and a file on disk

**File Mode** - Specifies how you want to open a file (read, write, append)

**Path** - The location of a file in the file system

**Relative Path** - A path relative to the current working directory

**Absolute Path** - A complete path from the root directory

**Serialization** - Converting Python objects to a format that can be stored or transmitted

**Deserialization** - Converting stored data back to Python objects

**Context Manager** - A Python construct that automatically manages resources (like files)

**Exception Handling** - Catching and responding to errors during program execution

---

## File Basics

### What are Files?
- **Persistent storage** - Data that survives program execution
- **Text files** - Human-readable content (like .txt, .py, .md)
- **Binary files** - Non-text data (like images, videos, .exe)

### Why Use Files?
- **Data persistence** - Save information between program runs
- **Configuration** - Store program settings
- **Logging** - Record program activity
- **Data processing** - Work with large datasets

---

## Opening and Closing Files

### Basic File Operations
```python
# Open a file for reading
file = open('data.txt', 'r')
content = file.read()
file.close()

# Better approach using context manager
with open('data.txt', 'r') as file:
    content = file.read()
# File automatically closes when exiting the block
```

### File Handle Methods
- **`read()`** - Read entire file content
- **`readline()`** - Read one line at a time
- **`readlines()`** - Read all lines into a list
- **`write()`** - Write data to file
- **`close()`** - Close the file handle

---

## File Open Modes

### Text File Modes
```python
'r'    # Read mode (default) - file must exist
'w'    # Write mode - creates new file, overwrites existing
'a'    # Append mode - adds to end of existing file
'r+'   # Read and write mode
'w+'   # Write and read mode
```

### Binary File Modes
```python
'rb'   # Read binary mode
'wb'   # Write binary mode
'ab'   # Append binary mode
```

### Mode Selection Guidelines
- **Reading existing files** → Use `'r'`
- **Creating new files** → Use `'w'`
- **Adding to existing files** → Use `'a'`
- **Binary files** → Add `'b'` to any mode

---

## Reading Files

### Reading All at Once
```python
with open('data.txt', 'r') as file:
    content = file.read()
    print(content)
```
**Pros:** Simple, fast for small files
**Cons:** Memory intensive for large files

### Reading Line by Line
```python
with open('data.txt', 'r') as file:
    for line in file:
        print(line.strip())
```
**Pros:** Memory efficient, good for large files
**Cons:** Slightly more complex code

### Reading Specific Lines
```python
with open('data.txt', 'r') as file:
    lines = file.readlines()
    first_line = lines[0]
    last_line = lines[-1]
```

---

## Writing Files

### Writing Text
```python
# Write mode - overwrites existing content
with open('output.txt', 'w') as file:
    file.write("Hello World!\n")
    file.write("This is line 2\n")

# Append mode - adds to existing content
with open('log.txt', 'a') as file:
    file.write("New entry: " + str(datetime.now()) + "\n")
```

### Writing Multiple Lines
```python
lines = ["Line 1", "Line 2", "Line 3"]
with open('output.txt', 'w') as file:
    for line in lines:
        file.write(line + "\n")

# Alternative using writelines
with open('output.txt', 'w') as file:
    file.writelines(line + "\n" for line in lines)
```

---

## File Paths

### Path Types
```python
import os

# Relative paths
'data.txt'           # File in current directory
'../data.txt'        # File in parent directory
'./subfolder/file.txt'  # File in subfolder

# Absolute paths
'/home/user/data.txt'    # Unix/Linux
'C:\\Users\\user\\data.txt'  # Windows
```

### Path Operations
```python
import os

# Get current working directory
current_dir = os.getcwd()

# Join paths safely
file_path = os.path.join('folder', 'subfolder', 'file.txt')

# Check if file exists
if os.path.exists('data.txt'):
    print("File exists!")

# Get absolute path
abs_path = os.path.abspath('data.txt')
```

---

## Error Handling

### Basic Try-Except
```python
try:
    with open('data.txt', 'r') as file:
        content = file.read()
except FileNotFoundError:
    print("File not found!")
except PermissionError:
    print("Permission denied!")
except Exception as e:
    print(f"Unexpected error: {e}")
```

### File-Specific Error Handling
```python
def read_file_safely(filename):
    try:
        with open(filename, 'r') as file:
            return file.read()
    except FileNotFoundError:
        print(f"File '{filename}' not found")
        return None
    except PermissionError:
        print(f"Permission denied for '{filename}'")
        return None
    except UnicodeDecodeError:
        print(f"Cannot read '{filename}' as text")
        return None
```

---

## Serialization with Pickle

### What is Pickle?
- **Python-specific** serialization format
- **Converts Python objects** to byte streams
- **Preserves object structure** and data types
- **Not human-readable** or portable to other languages

### Basic Pickle Operations
```python
import pickle

# Serialize (save) data
data = {"name": "Alice", "scores": [85, 92, 78]}
with open('data.pkl', 'wb') as file:
    pickle.dump(data, file)

# Deserialize (load) data
with open('data.pkl', 'rb') as file:
    loaded_data = pickle.load(file)
print(loaded_data)  # {'name': 'Alice', 'scores': [85, 92, 78]}
```

---

## Simple Database Concepts

### Key-Value Storage
```python
# Simple database using dictionary and file
import json

def save_database(data, filename):
    with open(filename, 'w') as file:
        json.dump(data, file, indent=2)

def load_database(filename):
    try:
        with open(filename, 'r') as file:
            return json.load(file)
    except FileNotFoundError:
        return {}

# Usage
db = load_database('users.json')
db['user1'] = {'name': 'Alice', 'age': 25}
save_database(db, 'users.json')
```

### SQLite Database
```python
import sqlite3

# Create/connect to database
conn = sqlite3.connect('users.db')
cursor = conn.cursor()

# Create table
cursor.execute('''
    CREATE TABLE IF NOT EXISTS users (
        id INTEGER PRIMARY KEY,
        name TEXT NOT NULL,
        age INTEGER
    )
''')

# Insert data
cursor.execute('INSERT INTO users (name, age) VALUES (?, ?)', ('Alice', 25))

# Query data
cursor.execute('SELECT * FROM users WHERE age > 20')
results = cursor.fetchall()

# Close connection
conn.commit()
conn.close()
```

### Data Storage Comparison

| Feature | JSON | Pickle | SQLite |
|---------|------|--------|--------|
| **Readability** | Human-readable | Binary (not readable) | Structured tables |
| **Portability** | Cross-language | Python only | Cross-language |
| **Data Types** | Basic types only | All Python types | Structured data |
| **Performance** | Fast for small data | Fast for Python objects | Fast for queries |
| **Use Case** | Configuration, APIs | Python objects | Relational data |
| **Security** | Safe | Security risk | Safe |
| **File Size** | Larger | Smaller | Optimized |

---

## Dos and Don'ts

### ✅ DO:
- **Use context managers** (`with` statements) for file operations
- **Handle file errors** with try-except blocks
- **Choose appropriate file modes** for your operations
- **Close files explicitly** if not using context managers
- **Use absolute paths** when you need specific file locations
- **Validate file existence** before operations
- **Use appropriate encoding** for text files

### ❌ DON'T:
- **Forget to close files** (leads to resource leaks)
- **Use hardcoded file paths** in your code
- **Ignore file operation errors**
- **Use write mode** when you want to append
- **Assume files exist** without checking
- **Use pickle for untrusted data** (security risk)
- **Mix text and binary modes** inappropriately

---

## Key Takeaways

### File Operations
- **Files provide persistent storage** for your programs
- **Context managers** automatically handle file cleanup
- **Choose file modes carefully** based on your needs
- **Always handle potential errors** in file operations

### Data Persistence
- **Text files** are good for human-readable data
- **Binary files** are efficient for complex data structures
- **Pickle** preserves Python object structure
- **JSON** provides portable, human-readable storage

### Best Practices
- **Error handling** makes programs robust
- **Proper file paths** ensure portability
- **Resource management** prevents memory leaks
- **Appropriate file modes** prevent data loss

---

## Further Explorations

### Advanced File Operations
- **File locking** for concurrent access
- **Memory-mapped files** for large datasets
- **Compression** (gzip, zip) for file storage
- **Regular expressions** for text file processing

### Database Systems
- **SQLite** for embedded databases
- **CSV processing** with pandas
- **XML and JSON** parsing libraries
- **NoSQL databases** (MongoDB, Redis)

### System Integration
- **Command line arguments** for file processing
- **File watching** for automated processing
- **Logging frameworks** for application logs
- **Configuration file** management

### Performance Optimization
- **Buffered I/O** for large files
- **Async file operations** for concurrent processing
- **Memory-efficient** file processing
- **File caching** strategies
