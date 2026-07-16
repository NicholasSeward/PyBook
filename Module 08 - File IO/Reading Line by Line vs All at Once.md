# Reading Line by Line vs All at Once

## Overview
There are different ways to read files depending on what you need to do with the data.

## Reading All at Once

### `read()` - Read Entire File
```python
# Read the entire file into memory
with open('data.txt', 'r') as file:
    content = file.read()
    print(f"File size: {len(content)} characters")
    print("Content:")
    print(content)
```

**Use when:**
- File is small
- You need the entire content
- You want to process all data together

## Reading Line by Line

### `readline()` - Read One Line
```python
# Read one line at a time
with open('data.txt', 'r') as file:
    line1 = file.readline()
    line2 = file.readline()
    print(f"Line 1: {line1.strip()}")
    print(f"Line 2: {line2.strip()}")
```

### `readlines()` - Read All Lines into List
```python
# Read all lines into a list
with open('data.txt', 'r') as file:
    lines = file.readlines()
    print(f"Number of lines: {len(lines)}")
    for i, line in enumerate(lines):
        print(f"Line {i+1}: {line.strip()}")
```

### Loop Through File (Recommended)
```python
# Most efficient way to process line by line
with open('data.txt', 'r') as file:
    for line_number, line in enumerate(file, 1):
        print(f"Line {line_number}: {line.strip()}")
```

## Memory Comparison

### Small File (All at Once)
```python
# Good for small files
with open('small_file.txt', 'r') as file:
    content = file.read()
    words = content.split()
    print(f"Total words: {len(words)}")
```

### Large File (Line by Line)
```python
# Better for large files
word_count = 0
with open('large_file.txt', 'r') as file:
    for line in file:
        words = line.split()
        word_count += len(words)
        # Process each line without loading everything into memory
print(f"Total words: {word_count}")
```

## Real Example: Processing Student Grades

```python
# Process grades from a file
def process_grades_all_at_once(filename):
    """Read all grades at once - good for small files"""
    with open(filename, 'r') as file:
        content = file.read()
        lines = content.split('\n')
        
        grades = []
        for line in lines:
            if line.strip():  # Skip empty lines
                try:
                    grade = int(line)
                    grades.append(grade)
                except ValueError:
                    print(f"Invalid grade: {line}")
        
        if grades:
            average = sum(grades) / len(grades)
            print(f"All grades: {grades}")
            print(f"Average: {average:.1f}")
        else:
            print("No valid grades found")

def process_grades_line_by_line(filename):
    """Process grades line by line - good for large files"""
    grades = []
    line_count = 0
    
    with open(filename, 'r') as file:
        for line in file:
            line_count += 1
            line = line.strip()
            
            if line:  # Skip empty lines
                try:
                    grade = int(line)
                    grades.append(grade)
                except ValueError:
                    print(f"Invalid grade on line {line_count}: {line}")
    
    if grades:
        average = sum(grades) / len(grades)
        print(f"Processed {line_count} lines")
        print(f"Valid grades: {len(grades)}")
        print(f"Average: {average:.1f}")
    else:
        print("No valid grades found")

# Create a sample grades file
with open('grades.txt', 'w') as file:
    file.write("85\n92\n78\n96\n88\n91\n75\n89\n")

print("Processing all at once:")
process_grades_all_at_once('grades.txt')

print("\nProcessing line by line:")
process_grades_line_by_line('grades.txt')
```

**Output:**
```
Processing all at once:
All grades: [85, 92, 78, 96, 88, 91, 75, 89]
Average: 87.5

Processing line by line:
Processed 8 lines
Valid grades: 8
Average: 87.5
```

## When to Use Each Method

### Use `read()` (All at Once) When:
- File is small (< 1MB)
- You need to search through all content
- You want to process data as a whole

### Use Line by Line When:
- File is large
- You can process each line independently
- Memory usage is a concern
- You want to show progress

## Key Points

- **`read()`** - loads entire file into memory
- **`readline()`** - reads one line at a time
- **`readlines()`** - loads all lines into a list
- **Loop through file** - most memory efficient
- **Choose based on file size and needs**

## Summary

✅ **All at once** - good for small files, simple processing  
✅ **Line by line** - good for large files, memory efficient  
✅ **Loop through file** - recommended for most cases  
✅ **Consider file size** when choosing method  

Choose the right method for your file size and processing needs!
