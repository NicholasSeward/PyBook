# Common Algorithms

## Max and Min

Finding the maximum or minimum value in a list is a common task. You can do this by keeping track of the best value you've seen so far.

```python
def find_max(numbers):
    if not numbers:
        return None
    
    max_value = numbers[0]  # Start with first number
    for num in numbers:
        if num > max_value:
            max_value = num
    return max_value

def find_min(numbers):
    if not numbers:
        return None
    
    min_value = numbers[0]  # Start with first number
    for num in numbers:
        if num < min_value:
            min_value = num
    return min_value

# Examples
scores = [85, 92, 78, 96, 88]
highest = find_max(scores)  # 96
lowest = find_min(scores)   # 78
```

## Linear Search

Linear search checks each item in a list one by one until it finds what you're looking for. It's simple but not always the fastest.

```python
def linear_search(items, target):
    for i, item in enumerate(items):
        if item == target:
            return i  # Found it! Return the position
    return -1  # Not found

# Examples
names = ["Alice", "Bob", "Charlie", "David"]
position = linear_search(names, "Charlie")  # 2
not_found = linear_search(names, "Eve")     # -1
```

## Key Points

- **Max/Min**: Check each item and remember the best one
- **Linear Search**: Look through items one by one
- **Simple but slow**: These algorithms are easy to understand but can be slow with large lists
- **Time Complexity**: All are O(n) - time grows with list size
