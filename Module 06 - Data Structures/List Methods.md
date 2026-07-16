# List Methods

## Overview
Lists have many built-in methods that make them easier to work with. Think of methods as actions you can perform on lists.

## Adding Items

### append() - Add to End
```python
fruits = ["apple", "banana"]
fruits.append("orange")
print(fruits)  # ['apple', 'banana', 'orange']
```

### insert() - Add at Position
```python
fruits = ["apple", "banana"]
fruits.insert(1, "grape")  # Insert at position 1
print(fruits)  # ['apple', 'grape', 'banana']
```

### extend() - Add Multiple Items
```python
fruits = ["apple", "banana"]
more_fruits = ["orange", "grape"]
fruits.extend(more_fruits)
print(fruits)  # ['apple', 'banana', 'orange', 'grape']
```

## Removing Items

### remove() - Remove by Value
```python
fruits = ["apple", "banana", "orange", "banana"]
fruits.remove("banana")  # Removes first "banana"
print(fruits)  # ['apple', 'orange', 'banana']
```

### pop() - Remove by Position
```python
fruits = ["apple", "banana", "orange"]
last_fruit = fruits.pop()  # Remove and return last item
print(f"Removed: {last_fruit}")  # Removed: orange
print(f"Remaining: {fruits}")    # Remaining: ['apple', 'banana']

first_fruit = fruits.pop(0)  # Remove and return first item
print(f"Removed: {first_fruit}")  # Removed: apple
```

### del - Remove by Position
```python
fruits = ["apple", "banana", "orange"]
del fruits[1]  # Remove item at position 1
print(fruits)  # ['apple', 'orange']
```

## Finding Items

### index() - Find Position
```python
fruits = ["apple", "banana", "orange"]
position = fruits.index("banana")
print(f"Banana is at position {position}")  # Banana is at position 1
```

### count() - Count Occurrences
```python
fruits = ["apple", "banana", "apple", "orange", "apple"]
apple_count = fruits.count("apple")
print(f"Apples appear {apple_count} times")  # Apples appear 3 times
```

### in - Check if Item Exists
```python
fruits = ["apple", "banana", "orange"]
if "banana" in fruits:
    print("We have bananas!")
```

## Sorting and Reversing

### sort() - Sort in Place
```python
numbers = [3, 1, 4, 1, 5, 9, 2, 6]
numbers.sort()
print(numbers)  # [1, 1, 2, 3, 4, 5, 6, 9]

# Sort strings
fruits = ["banana", "apple", "cherry"]
fruits.sort()
print(fruits)  # ['apple', 'banana', 'cherry']
```

### reverse() - Reverse Order
```python
numbers = [1, 2, 3, 4, 5]
numbers.reverse()
print(numbers)  # [5, 4, 3, 2, 1]
```

## Real Example: Student Grades

```python
# Manage a list of student grades
grades = [85, 92, 78, 96, 88]

# Add a new grade
grades.append(91)
print(f"After adding: {grades}")

# Find the highest grade
highest = max(grades)
highest_position = grades.index(highest)
print(f"Highest grade {highest} is at position {highest_position}")

# Sort grades from highest to lowest
grades.sort(reverse=True)
print(f"Sorted grades: {grades}")

# Remove the lowest grade
lowest = min(grades)
grades.remove(lowest)
print(f"After removing lowest: {grades}")

# Calculate average
average = sum(grades) / len(grades)
print(f"Average: {average:.1f}")
```

**Output:**
```
After adding: [85, 92, 78, 96, 88, 91]
Highest grade 96 is at position 3
Sorted grades: [96, 92, 91, 88, 85, 78]
After removing lowest: [96, 92, 91, 88, 85]
Average: 90.4
```

## Key Points

- **Methods change the list** (like `append`, `sort`)
- **Some methods return values** (like `pop`, `index`)
- **Use `in` to check if something exists**
- **`sort()` changes the list, `sorted()` returns a new list**

## Summary

✅ **Adding** - `append()`, `insert()`, `extend()`  
✅ **Removing** - `remove()`, `pop()`, `del`  
✅ **Finding** - `index()`, `count()`, `in`  
✅ **Organizing** - `sort()`, `reverse()`  

List methods make working with data much easier!
