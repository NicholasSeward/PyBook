# Tutorial (Module 6 - Data Structures)

## Code Block 1: List Creation and Basic Operations

**Try this code:**

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
fruits.insert(1, "grape")
print(fruits)
```

**Question 1:** What does this code print?
- A) `["apple", "grape", "banana", "cherry", "orange"]`
- B) `["apple", "banana", "grape", "cherry", "orange"]`
- C) `["apple", "grape", "banana", "cherry"]`
- D) `["grape", "apple", "banana", "cherry", "orange"]`

**Question 2:** How would you modify the code to insert "kiwi" at the beginning of the list?
- A) `fruits.insert(0, "kiwi")`
- B) `fruits.insert(-1, "kiwi")`
- C) `fruits.append("kiwi")`
- D) `fruits.insert(1, "kiwi")`

---

## Code Block 2: List Indexing and Negative Indices

**Try this code:**

```python
numbers = [10, 20, 30, 40, 50]
print(numbers[1], numbers[-2], numbers[2:4])
```

**Question 3:** What does this code print?
- A) `20 40 [30, 40]`
- B) `20 40 [30, 40, 50]`
- C) `10 40 [30, 40]`
- D) `20 30 [30, 40]`

**Question 4:** How would you modify the code to print the last three elements `[30, 40, 50]`?
- A) `numbers[2:]`
- B) `numbers[-3:]`
- C) `numbers[2:5]`
- D) All of the above

---

## Code Block 3: List Slicing with Steps

**Try this code:**

```python
data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
result = data[1:8:2]
print(result)
```

**Question 5:** What does this code print?
- A) `[2, 4, 6, 8]`
- B) `[1, 3, 5, 7]`
- C) `[2, 4, 6, 8, 10]`
- D) `[1, 3, 5, 7, 9]`

**Question 6:** How would you modify the code to print `[9, 7, 5, 3]` (reverse order, every other element)?
- A) `data[8:0:-2]`
- B) `data[9:1:-2]`
- C) `data[-2:-9:-2]`
- D) `data[8:1:-2]`

---

## Code Block 4: List Methods - Stack Operations

**Try this code:**

```python
stack = []
stack.append(1)
stack.append(2)
stack.append(3)
popped = stack.pop()
print(f"Popped: {popped}, Stack: {stack}")
```

**Question 7:** What does this code print?
- A) `Popped: 1, Stack: [2, 3]`
- B) `Popped: 3, Stack: [1, 2]`
- C) `Popped: 2, Stack: [1, 3]`
- D) `Popped: 3, Stack: [2, 1]`

**Question 8:** How would you modify the code to implement a queue (FIFO) instead of a stack?
- A) Use `stack.pop(0)` instead of `stack.pop()`
- B) Use `stack.remove(0)` instead of `stack.pop()`
- C) Use `stack.pop()` with `stack.insert(0, item)` for adding
- D) Use `stack.pop(0)` and keep `stack.append()`

---

## Code Block 5: List Methods - Remove and Count

**Try this code:**

```python
items = ["apple", "banana", "apple", "cherry", "apple"]
items.remove("apple")
count = items.count("apple")
print(f"Items: {items}, Apple count: {count}")
```

**Question 9:** What does this code print?
- A) `Items: ["banana", "apple", "cherry", "apple"], Apple count: 2`
- B) `Items: ["banana", "cherry", "apple"], Apple count: 1`
- C) `Items: ["banana", "apple", "cherry"], Apple count: 1`
- D) `Items: ["banana", "cherry"], Apple count: 0`

**Question 10:** How would you modify the code to remove ALL occurrences of "apple"?
- A) Use a loop: `while "apple" in items: items.remove("apple")`
- B) Use `items.clear()` if all items are "apple"
- C) Use list comprehension: `items = [item for item in items if item != "apple"]`
- D) All of the above

---

## Code Block 6: Tuple Creation and Immutability

**Try this code:**

```python
coordinates = (3, 4)
x, y = coordinates
coordinates_list = list(coordinates)
coordinates_list[0] = 5
print(f"Original: {coordinates}, Modified list: {coordinates_list}")
```

**Question 11:** What does this code print?
- A) `Original: (5, 4), Modified list: [5, 4]`
- B) `Original: (3, 4), Modified list: [5, 4]`
- C) `Original: (3, 4), Modified list: [3, 4]`
- D) Error: cannot modify tuple

**Question 12:** How would you modify the code to create a new tuple with the modified values?
- A) `new_coordinates = (coordinates_list[0], coordinates_list[1])`
- B) `new_coordinates = tuple(coordinates_list)`
- C) `new_coordinates = (5, 4)`
- D) All of the above

---

## Code Block 7: Dictionary Creation and Access

**Try this code:**

```python
student = {"name": "Alice", "age": 20, "grade": "A"}
student["major"] = "Computer Science"
print(student["name"], student.get("gpa", "Not specified"))
```

**Question 13:** What does this code print?
- A) `Alice Not specified`
- B) `Alice None`
- C) `Alice Error`
- D) `Alice Computer Science`

**Question 14:** How would you modify the code to safely check if "gpa" exists and print "GPA: 3.8" if it does, otherwise "No GPA"?
- A) `print("GPA:", student.get("gpa", "No GPA"))`
- B) `print("GPA:", student["gpa"] if "gpa" in student else "No GPA")`
- C) `print(f"GPA: {student['gpa']}" if "gpa" in student else "No GPA")`
- D) All of the above

---

## Code Block 8: Dictionary Methods and Iteration

**Try this code:**

```python
inventory = {"apples": 10, "bananas": 5, "oranges": 8}
for item, quantity in inventory.items():
    if quantity > 6:
        print(f"{item}: {quantity}")
```

**Question 15:** What does this code print?
- A) `apples: 10` then `oranges: 8`
- B) `apples: 10` then `bananas: 5` then `oranges: 8`
- C) `oranges: 8`
- D) `apples: 10` then `oranges: 8`

**Question 16:** How would you modify the code to print items with quantity less than or equal to 6?
- A) Change condition to `if quantity <= 6:`
- B) Change condition to `if quantity < 7:`
- C) Change condition to `if not quantity > 6:`
- D) All of the above

---

## Code Block 9: Dictionary Update and Merge

**Try this code:**

```python
dict1 = {"a": 1, "b": 2}
dict2 = {"b": 3, "c": 4}
dict1.update(dict2)
print(dict1)
```

**Question 17:** What does this code print?
- A) `{"a": 1, "b": 2, "c": 4}`
- B) `{"a": 1, "b": 3, "c": 4}`
- C) `{"a": 1, "b": 2, "b": 3, "c": 4}`
- D) `{"b": 3, "c": 4, "a": 1}`

**Question 18:** How would you modify the code to preserve the original values in dict1 when there are key conflicts?
- A) Use `dict2.update(dict1)` instead
- B) Check if key exists before updating: `for k, v in dict2.items(): if k not in dict1: dict1[k] = v`
- C) Use dictionary comprehension: `{**dict2, **dict1}`
- D) All of the above

---

## Code Block 10: Nested Data Structures

**Try this code:**

```python
students = {
    "Alice": {"age": 20, "grades": [85, 90, 88]},
    "Bob": {"age": 19, "grades": [78, 82, 80]}
}
alice_avg = sum(students["Alice"]["grades"]) / len(students["Alice"]["grades"])
print(f"Alice's average: {alice_avg}")
```

**Question 19:** What does this code print?
- A) `Alice's average: 87.67`
- B) `Alice's average: 87.0`
- C) `Alice's average: 88`
- D) `Alice's average: 87.66666666666667`

**Question 20:** How would you modify the code to calculate Bob's average grade?
- A) `bob_avg = sum(students["Bob"]["grades"]) / len(students["Bob"]["grades"])`
- B) `bob_avg = sum(students["Bob"]["grades"]) / 3`
- C) `bob_avg = (78 + 82 + 80) / 3`
- D) All of the above

---

## Challenge Questions

**Question 21:** In Code Block 4, what happens if you try to pop from an empty stack?
- A) Returns `None`
- B) Returns `[]`
- C) Raises an `IndexError`
- D) Returns `0`

**Question 22:** In Code Block 7, what's the difference between `student["gpa"]` and `student.get("gpa")`?
- A) No difference, both return the same value
- B) `student["gpa"]` raises `KeyError` if key doesn't exist, `student.get("gpa")` returns `None`
- C) `student.get("gpa")` is faster
- D) `student["gpa"]` is more readable

---
