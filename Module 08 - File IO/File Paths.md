# File Paths

## What is a File Path?

A file path tells your computer where to find a file. It's like an address for your computer's file system.

## Types of Paths

### Absolute Paths
Absolute paths start from the root directory and give the complete location:

```python
# Windows absolute path
windows_path = "C:\\Users\\Student\\Documents\\file.txt"

# Unix/Linux/Mac absolute path
unix_path = "/home/student/documents/file.txt"

print(f"Windows: {windows_path}")
print(f"Unix: {unix_path}")
```

### Relative Paths
Relative paths start from your current location:

```python
# Current folder
current_file = "data.txt"

# Subfolder
subfolder_file = "data/input.txt"

# Parent folder
parent_file = "../config.txt"

print(f"Current: {current_file}")
print(f"Subfolder: {subfolder_file}")
print(f"Parent: {parent_file}")
```

## Python Tools for Paths

### Using `os.path`
```python
import os

# Join paths (works on all operating systems)
folder = "documents"
filename = "report.txt"
full_path = os.path.join(folder, filename)
print(f"Full path: {full_path}")

# Get current working directory
current_dir = os.getcwd()
print(f"Current directory: {current_dir}")

# Check if file exists
if os.path.exists(full_path):
    print(f"File exists: {full_path}")
else:
    print(f"File does not exist: {full_path}")
```

### Using `pathlib` (Modern approach)
```python
from pathlib import Path

# Create path objects
current_dir = Path.cwd()
documents = current_dir / "documents"
report_file = documents / "report.txt"

print(f"Current directory: {current_dir}")
print(f"Documents folder: {documents}")
print(f"Report file: {report_file}")

# Check if path exists
if report_file.exists():
    print(f"File exists: {report_file}")
else:
    print(f"File does not exist: {report_file}")
```

## Simple Examples

### Basic Path Operations
```python
from pathlib import Path

# Create a path
file_path = Path("documents/reports/report.txt")

# Get parts of the path
print(f"Full path: {file_path}")
print(f"Name: {file_path.name}")
print(f"Extension: {file_path.suffix}")
print(f"Parent folder: {file_path.parent}")

# Check properties
print(f"Is file? {file_path.is_file()}")
print(f"Exists? {file_path.exists()}")
```

### Cross-Platform Paths
```python
import os
from pathlib import Path

# Bad - hardcoded separators
windows_style = "folder\\file.txt"      # Windows only
unix_style = "folder/file.txt"          # Unix only

# Good - use Python tools
good_path = os.path.join("folder", "file.txt")
better_path = Path("folder") / "file.txt"

print(f"Good path: {good_path}")
print(f"Better path: {better_path}")
# These work on all operating systems!
```

## Key Points

- **Absolute paths** - start from root directory
- **Relative paths** - start from current directory
- **`os.path.join()`** - join path parts safely
- **`pathlib.Path`** - modern path handling
- **Cross-platform** - works on Windows, Mac, and Linux

## Summary

✅ **Absolute paths** - complete location from root  
✅ **Relative paths** - location from current folder  
✅ **`os.path`** - basic path operations  
✅ **`pathlib`** - modern path handling  
✅ **Cross-platform** - works everywhere  

Understanding paths helps you work with files anywhere on your computer!
