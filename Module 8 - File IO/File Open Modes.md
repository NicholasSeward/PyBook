# File Open Modes

## Overview
File open modes tell Python how you want to work with a file. Different modes let you read, write, or append data in different ways.

## Basic Modes

### Read Mode (`'r'`)
```python
# Read existing file
with open('data.txt', 'r') as file:
    content = file.read()
    print(content)

# File must exist, or you'll get an error
```

### Write Mode (`'w'`)
```python
# Create new file or overwrite existing
with open('output.txt', 'w') as file:
    file.write("Hello World!")
    file.write("\nThis is a new line")

# WARNING: This deletes existing content!
```

### Append Mode (`'a'`)
```python
# Add to end of existing file
with open('log.txt', 'a') as file:
    file.write("New entry added\n")
    file.write("Another entry\n")

# Creates file if it doesn't exist
```

## Binary Modes

### Read Binary (`'rb'`)
```python
# Read binary files (images, videos, etc.)
with open('image.jpg', 'rb') as file:
    binary_data = file.read()
    print(f"Read {len(binary_data)} bytes")

# Also used for pickle files
import pickle
with open('data.pkl', 'rb') as file:
    data = pickle.load(file)
```

### Write Binary (`'wb'`)
```python
# Write binary data
with open('output.bin', 'wb') as file:
    file.write(b'\x48\x65\x6c\x6c\x6f')  # "Hello" in hex

# Also used for pickle files
import pickle
data = {"name": "Alice", "age": 25}
with open('data.pkl', 'wb') as file:
    pickle.dump(data, file)
```

## Combined Modes (Rarely Used)

### Read and Write (`'r+'`)
```python
# Read and write to same file
with open('data.txt', 'r+') as file:
    # Read first
    content = file.read()
    print(f"Current content: {content}")
    
    # Go to beginning and write
    file.seek(0)
    file.write("Updated content\n")
```

### Write and Read (`'w+'`)
```python
# Create new file for reading and writing
with open('newfile.txt', 'w+') as file:
    # Write first
    file.write("Initial content\n")
    
    # Go to beginning to read
    file.seek(0)
    content = file.read()
    print(f"What we wrote: {content}")
```

## Append Binary (`'ab'`)
```python
# Append binary data to existing file
with open('data.bin', 'ab') as file:
    file.write(b'\x05\x06\x07\x08')

# Creates file if it doesn't exist
```

## Common Use Cases

### Text Files
- **`'r'`** - Reading configuration files, logs, data files
- **`'w'`** - Creating new files, overwriting old data
- **`'a'`** - Adding to log files, appending data

### Binary Files
- **`'rb'** - Reading images, videos, documents, pickle files
- **`'wb'** - Creating new binary files, saving pickle data
- **`'ab'** - Appending to binary files (rare)

### Combined Modes (Rarely Used)
- **`'r+'`** - Updating existing files
- **`'w+'`** - Creating new files for reading/writing

## Key Points

- **`'r'`** - read existing file (default mode)
- **`'w'`** - write new file (overwrites existing)
- **`'a'`** - append to existing file
- **`'rb'`** - read binary file
- **`'wb'`** - write binary file
- **Reading/writing modes** - `'r+'` and `'w+'` are rarely used
- **Most common** - `'r'`, `'w'`, `'a'`, `'rb'`, `'wb'`, or rarely `'ab'`
- **Binary modes** - use `'b'` for non-text files
- **Context managers** - use `with` for automatic cleanup

## Summary

✅ **Read modes** - `'r'` and `'rb'` for reading files  
✅ **Write modes** - `'w'` and `'wb'` for creating/overwriting  
✅ **Append modes** - `'a'` and `'ab'` for adding to files  
✅ **Combined modes** - rarely used in practice  
✅ **Binary modes** - add `'b'` for non-text files  
✅ **Context managers** - use `with` for safe file handling  

Understanding file modes helps you work with files correctly!
