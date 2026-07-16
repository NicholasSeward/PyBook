# Sets

## What are Sets?

Sets are collections of unique items. They're like mathematical sets - no duplicates allowed, and they're very fast for checking if something exists.

```python
# Create sets
fruits = {"apple", "banana", "orange"}
colors = {"red", "blue", "green"}

# Add items
fruits.add("grape")
print(fruits)  # {'apple', 'banana', 'orange', 'grape'}

# Remove duplicates automatically
numbers = {1, 2, 2, 3, 3, 4}
print(numbers)  # {1, 2, 3, 4}
```

## Set Operations

### Union (|)
Combine two sets - all items from both sets.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union = set1 | set2
print(union)  # {1, 2, 3, 4, 5}

# Or use union() method
union = set1.union(set2)
```

### Intersection (&)
Find items that exist in both sets.

```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}
intersection = set1 & set2
print(intersection)  # {3, 4}

# Or use intersection() method
intersection = set1.intersection(set2)
```

### Difference (-)
Find items in the first set that aren't in the second.

```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}
difference = set1 - set2
print(difference)  # {1, 2}

# Or use difference() method
difference = set1.difference(set2)
```

## O(1) Contains Check

The real power of sets is checking if an item exists - it's always fast regardless of size!

```python
# Create a large set
large_set = set(range(1000000))

# Check if numbers exist - always fast!
print(500000 in large_set)  # True - O(1) time
print(999999 in large_set)  # True - O(1) time
print(-1 in large_set)      # False - O(1) time

# Compare with list (much slower)
large_list = list(range(1000000))
print(500000 in large_list)  # True - but O(n) time!
```

## Key Points

- **Sets are unique**: No duplicates allowed
- **Fast lookups**: `in` check is O(1) - always fast
- **Set operations**: Union, intersection, difference
- **Use for**: Removing duplicates, fast membership testing
