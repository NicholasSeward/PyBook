# Escape Characters

## Overview
Escape characters let you put special characters in strings that would otherwise be hard to type.

## Common Escape Characters

### New Lines and Tabs
```python
# \n creates a new line
print("Line 1\nLine 2\nLine 3")

# \t creates a tab
print("Name:\tAge:\tCity:")
print("Alice:\t25:\tNew York")
print("Bob:\t30:\tLos Angeles")
```

**Output:**
```
Line 1
Line 2
Line 3
Name:	Age:	City:
Alice:	25:	New York
Bob:	30:	Los Angeles
```

### Quotes Inside Strings
```python
# Use backslash to escape quotes
print("She said \"Hello!\"")
print('He said \'Goodbye!\'')

# Or use different quote types
print("She said 'Hello!'")
print('He said "Goodbye!"')
```

**Output:**
```
She said "Hello!"
He said 'Goodbye!'
She said 'Hello!'
He said "Goodbye!"
```

### Special Characters
```python
# Backslash
print("This is a backslash: \\")

# Dollar sign (in f-strings)
price = 10
print(f"The price is \\${price}")

# Percent sign
print("You got 85\\% on the test")
```

**Output:**
```
This is a backslash: \
The price is \$10
You got 85\% on the test
```

## Raw Strings

Use `r` prefix to treat backslashes literally.

```python
# Normal string - \n becomes new line
normal = "C:\new\file.txt"
print(f"Normal: {normal}")

# Raw string - \n stays as \n
raw = r"C:\new\file.txt"
print(f"Raw: {raw}")
```

**Output:**
```
Normal: C:
ew	ile.txt
Raw: C:\new\file.txt
```

## Real Example: File Paths

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

**Output:**
```
File path: C:\Users\Student\Documents\file.txt
File path (raw): C:\Users\Student\Documents\file.txt
Are they equal? True
```

## Multi-line Strings

### Using \n
```python
# Create multi-line text with \n
poem = "Roses are red,\nViolets are blue,\nPython is fun,\nAnd so are you!"
print(poem)
```

### Using Triple Quotes
```python
# Triple quotes for multi-line strings
poem = """Roses are red,
Violets are blue,
Python is fun,
And so are you!"""
print(poem)
```

**Output (both methods):**
```
Roses are red,
Violets are blue,
Python is fun,
And so are you!
```

## Common Use Cases

### Formatting Text
```python
# Create a formatted table
print("Name\t\tAge\tCity")
print("-" * 30)
print("Alice\t\t25\tNew York")
print("Bob\t\t30\tLos Angeles")
print("Charlie\t\t35\tChicago")
```

### File Paths
```python
# Windows file path
windows_path = "C:\\Program Files\\Python\\python.exe"

# Unix file path
unix_path = "/usr/bin/python3"

print(f"Windows: {windows_path}")
print(f"Unix: {unix_path}")
```

## Key Points

- **`\n`** - new line
- **`\t`** - tab
- **`\"`** - quote inside double quotes
- **`\'`** - quote inside single quotes
- **`\\`** - backslash
- **`r"..."`** - raw string (no escaping)

## Summary

✅ **`\n`** - new line  
✅ **`\t`** - tab  
✅ **`\"`** - quote inside string  
✅ **`\\`** - backslash  
✅ **`r"..."`** - raw string  

Escape characters help you create properly formatted strings!
