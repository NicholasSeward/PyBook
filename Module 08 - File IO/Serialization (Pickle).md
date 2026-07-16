# Pickle and JSON Basics

## What is Serialization?

Serialization converts Python objects into a format that can be saved to files. It's like packing your data into a box that can be stored and unpacked later.

## Pickle - Python's Serialization Tool

### Basic Save and Load
```python
import pickle

# Save data
data = {"name": "Alice", "age": 25, "grades": [85, 92, 78]}
with open('data.pkl', 'wb') as file:
    pickle.dump(data, file)

# Load data back
with open('data.pkl', 'rb') as file:
    loaded_data = pickle.load(file)

print("Loaded:", loaded_data)
```

### Save Multiple Items
```python
import pickle

# Save several things
with open('stuff.pkl', 'wb') as file:
    pickle.dump("Hello", file)
    pickle.dump([1, 2, 3], file)
    pickle.dump({"a": 1, "b": 2}, file)

# Load them back (same order)
with open('stuff.pkl', 'rb') as file:
    text = pickle.load(file)
    numbers = pickle.load(file)
    info = pickle.load(file)

print(f"Text: {text}")
print(f"Numbers: {numbers}")
print(f"Info: {info}")
```

## JSON - Human-Readable Format

### Basic Save and Load
```python
import json

# Save data
data = {"name": "Alice", "age": 25, "grades": [85, 92, 78]}
with open('data.json', 'w') as file:
    json.dump(data, file, indent=2)

# Load data back
with open('data.json', 'r') as file:
    loaded_data = json.load(file)

print("Loaded:", loaded_data)
```

## CSV - Simple Table Format

### Basic Save and Load
```python
import csv

# Save data
data = [
    ["name", "age", "grade"],
    ["Alice", 20, "A"],
    ["Bob", 22, "B"],
    ["Charlie", 21, "A"]
]

with open('students.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerows(data)

# Load data back
with open('students.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

## Comparison Table

| Feature | Pickle | JSON | CSV |
|---------|--------|------|-----|
| **File Extension** | `.pkl` | `.json` | `.csv` |
| **Human Readable** | ❌ No | ✅ Yes | ✅ Yes |
| **Python Types** | ✅ All | ❌ Basic only | ❌ Basic only |
| **File Mode** | `'wb'/'rb'` | `'w'/'r'` | `'w'/'r'` |
| **Speed** | ✅ Fast | ⚠️ Medium | ✅ Fast |
| **File Size** | ✅ Small | ⚠️ Medium | ✅ Small |
| **Other Languages** | ❌ Python only | ✅ Universal | ✅ Universal |
| **Complex Objects** | ✅ Yes | ❌ No | ❌ No |

## When to Use Each

### Use Pickle When:
- Saving Python-specific objects
- Need to preserve exact data types
- Working only with Python

### Use JSON When:
- Need human-readable files
- Working with other languages
- Sharing data with others

### Use CSV When:
- Simple table data
- Need to open in Excel
- Basic text data

## Key Points

- **Pickle** - `pickle.dump()` to save, `pickle.load()` to load
- **JSON** - `json.dump()` to save, `json.load()` to load  
- **CSV** - `csv.writer()` to save, `csv.reader()` to load
- **Binary mode** - Pickle needs `'wb'/'rb'`
- **Text mode** - JSON and CSV use `'w'/'r'`

## Summary

✅ **Pickle** - fast, handles all Python types  
✅ **JSON** - human-readable, universal format  
✅ **CSV** - simple tables, Excel-friendly  
✅ **Choose wisely** - pick the right tool for your data
