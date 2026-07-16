# Accumulators and Counters

## Overview
Accumulators and counters help you keep track of information while looping through data.

## Counters

Counters keep track of how many times something happens.

```python
# Count how many even numbers we have
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
even_count = 0  # This is our counter

for num in numbers:
    if num % 2 == 0:
        even_count += 1  # Add 1 to our counter

print(f"We found {even_count} even numbers")
```

**Output:**
```
We found 4 even numbers
```

## Accumulators

Accumulators add up values as you go through a loop.

```python
# Add up all the numbers
numbers = [10, 20, 30, 40, 50]
total = 0  # This is our accumulator

for num in numbers:
    total += num  # Add each number to our total

print(f"The sum is: {total}")
```

**Output:**
```
The sum is: 150
```

## Finding the Maximum

```python
# Find the highest score
scores = [85, 92, 78, 96, 88, 91]
highest = scores[0]  # Start with first score

for score in scores:
    if score > highest:
        highest = score  # Update if we find a higher one

print(f"Highest score: {highest}")
```

**Output:**
```
Highest score: 96
```

## Building a List

```python
# Collect all positive numbers
numbers = [-5, 3, -2, 8, -1, 4, -7]
positive_numbers = []  # Start with empty list

for num in numbers:
    if num > 0:
        positive_numbers.append(num)  # Add positive numbers

print(f"Positive numbers: {positive_numbers}")
```

**Output:**
```
Positive numbers: [3, 8, 4]
```

## Real Example: Grade Analysis

```python
# Analyze student grades
grades = [85, 92, 78, 96, 88, 91, 75, 89]

# Counters
passing_count = 0
excellent_count = 0

# Accumulators
total_score = 0
highest_grade = grades[0]

for grade in grades:
    # Count passing grades (60+)
    if grade >= 60:
        passing_count += 1
    
    # Count excellent grades (90+)
    if grade >= 90:
        excellent_count += 1
    
    # Add to total
    total_score += grade
    
    # Check if this is the highest
    if grade > highest_grade:
        highest_grade = grade

# Calculate average
average = total_score / len(grades)

print(f"Total students: {len(grades)}")
print(f"Passing: {passing_count}")
print(f"Excellent: {excellent_count}")
print(f"Average: {average:.1f}")
print(f"Highest: {highest_grade}")
```

**Output:**
```
Total students: 8
Passing: 8
Excellent: 3
Average: 87.5
Highest: 96
```

## Key Points

- **Counters** start at 0 and add 1 each time something happens
- **Accumulators** start at a neutral value (0 for sums, first item for max/min)
- **Lists** start empty `[]` and you add items with `.append()`
- Always initialize your counter/accumulator before the loop!

## Summary

✅ **Counters** - count how many times something happens  
✅ **Accumulators** - add up values as you go  
✅ **Lists** - collect items that meet certain conditions  

These patterns are used in almost every program that processes data!
