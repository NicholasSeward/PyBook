# Immutable vs Mutable

## Overview
Some data types in Python can be changed after creation, others cannot. This is the difference between mutable and immutable.

## Mutable Types (Can Change)

### Lists
```python
# Lists can be changed
fruits = ["apple", "banana"]
fruits[0] = "orange"  # Change first item
fruits.append("grape")  # Add new item
print(fruits)  # ['orange', 'banana', 'grape']
```

### Dictionaries
```python
# Dictionaries can be changed
student = {"name": "Alice", "grade": 85}
student["grade"] = 90  # Change value
student["age"] = 20    # Add new key
print(student)  # {'name': 'Alice', 'grade': 90, 'age': 20}
```

## Immutable Types (Cannot Change)

### Strings
```python
# Strings cannot be changed
name = "Alice"
# name[0] = "B"  # This would cause an error!

# Instead, create a new string
new_name = "B" + name[1:]
print(new_name)  # "Blice"
```

### Tuples
```python
# Tuples cannot be changed
coordinates = (10, 20)
# coordinates[0] = 15  # This would cause an error!

# Instead, create a new tuple
new_coordinates = (15, 20)
print(new_coordinates)  # (15, 20)
```

### Numbers
```python
# Numbers cannot be changed
x = 5
# x = 6  # This creates a new number, doesn't change 5
```

## Why This Matters

### Mutable Lists
```python
# Two variables can point to the same list
list1 = [1, 2, 3]
list2 = list1  # Both point to the same list

list2.append(4)  # Change the list
print(f"list1: {list1}")  # [1, 2, 3, 4]
print(f"list2: {list2}")  # [1, 2, 3, 4]
```

### Immutable Strings
```python
# Two variables can point to the same string
str1 = "hello"
str2 = str1  # Both point to the same string

str2 = str2 + " world"  # Create new string
print(f"str1: {str1}")  # "hello"
print(f"str2: {str2}")  # "hello world"
```

## Creating Copies

### Shallow Copy (for lists)
```python
# Create a copy of a list
original = [1, 2, 3]
copy = original.copy()  # or list(original)

copy.append(4)
print(f"Original: {original}")  # [1, 2, 3]
print(f"Copy: {copy}")          # [1, 2, 3, 4]
```

### Deep Copy (for nested structures)
```python
import copy

# Nested list
original = [[1, 2], [3, 4]]
shallow_copy = original.copy()
deep_copy = copy.deepcopy(original)

# Change nested item
shallow_copy[0][0] = 99
deep_copy[0][0] = 88

print(f"Original: {original}")    # [[99, 2], [3, 4]]
print(f"Shallow: {shallow_copy}") # [[99, 2], [3, 4]]
print(f"Deep: {deep_copy}")       # [[88, 2], [3, 4]]
```

## Real Example: Student Records

```python
# Student record system
student1 = {
    "name": "Alice",
    "grades": [85, 92, 78]
}

# Create a copy for another student
student2 = student1.copy()
student2["name"] = "Bob"

# But grades list is still shared!
student2["grades"].append(95)

print(f"Alice's grades: {student1['grades']}")  # [85, 92, 78, 95]
print(f"Bob's grades: {student2['grades']}")    # [85, 92, 78, 95]

# Better approach - deep copy
import copy
student3 = copy.deepcopy(student1)
student3["name"] = "Charlie"
student3["grades"].append(88)

print(f"Alice's grades: {student1['grades']}")   # [85, 92, 78, 95]
print(f"Charlie's grades: {student3['grades']}") # [85, 92, 78, 88]
```

## Key Points

- **Mutable**: Lists, dictionaries, sets
- **Immutable**: Strings, tuples, numbers, booleans
- **Assignment** (`=`) creates a new reference
- **Copy methods** create new objects
- **Deep copy** needed for nested mutable objects

## Summary

✅ **Mutable** - can change after creation (lists, dicts)  
✅ **Immutable** - cannot change after creation (strings, tuples)  
✅ **Use `.copy()`** for simple copies  
✅ **Use `copy.deepcopy()`** for nested structures  

Understanding mutability helps you avoid unexpected bugs!
