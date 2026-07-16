
# Tutorial (Module 5 - Iteration)

## Code Block 1: Range Function Intuition

**Try this code:**
```python
for i in range(3, 8, 2):
    print(i, end=" ")
```

**Question 1:** What does this code print?
- A) `3 4 5 6 7`
- B) `3 5 7`
- C) `3 5 7 9`
- D) `4 6 8`

**Question 2:** How would you modify the code to print `2 4 6 8`?
- A) `range(2, 9, 2)`
- B) `range(2, 8, 2)`
- C) `range(2, 10, 2)`
- D) `range(1, 9, 2)`

---

## Code Block 2: Nested Loop Behavior

**Try this code:**
```python
for i in range(2):
    for j in range(3):
        print(f"({i},{j})", end=" ")
    print()
```

**Question 3:** What does this code print?
- A) `(0,0) (0,1) (0,2) (1,0) (1,1) (1,2)`
- B) `(0,0) (0,1) (0,2)` then `(1,0) (1,1) (1,2)` on separate lines
- C) `(0,0) (1,0) (0,1) (1,1) (0,2) (1,2)`
- D) `(0,0) (0,1) (0,2) (1,0) (1,1) (1,2)` all on one line

**Question 4:** How would you modify the code to print `(0,0) (0,1) (1,0) (1,1) (2,0) (2,1)`?
- A) Change outer loop to `range(3)` and inner loop to `range(2)`
- B) Change outer loop to `range(2)` and inner loop to `range(3)`
- C) Swap the variables: `print(f"({j},{i})", end=" ")`
- D) Change both loops to `range(2)`

---

## Code Block 3: While Loop Edge Cases

**Try this code:**
```python
x = 10
while x > 0:
    x -= 3
    print(x, end=" ")
```

**Question 5:** What does this code print?
- A) `7 4 1 -2`
- B) `7 4 1`
- C) `7 4 1 0`
- D) `7 4 1 -2 -5`

**Question 6:** How would you modify the code to print `9 6 3 0`?
- A) Change condition to `while x >= 0:` and `x -= 3`
- B) Change condition to `while x > 0:` and `x -= 3`
- C) Change condition to `while x >= 0:` and `x -= 3`
- D) Change condition to `while x > 0:` and `x -= 3`

---

## Code Block 4: Break vs Continue Intuition

**Try this code:**
```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i, end=" ")
```

**Question 7:** What does this code print?
- A) `1 2 3 4 5`
- B) `1 2 4 5`
- C) `1 2`
- D) `4 5`

**Question 8:** How would you modify the code to print `1 2 3`?
- A) Change `continue` to `break`
- B) Change condition to `if i == 4:`
- C) Change condition to `if i > 3:`
- D) Change condition to `if i >= 3:`

---

## Code Block 5: Accumulator Pattern with Conditions

**Try this code:**
```python
total = 0
for i in range(1, 6):
    if i % 2 == 0:
        total += i * 2
    else:
        total += i
print(total)
```

**Question 9:** What does this code print?
- A) `15`
- B) `25`
- C) `35`
- D) `45`

**Question 10:** How would you modify the code to print `30`?
- A) Change `total += i * 2` to `total += i * 3`
- B) Change `total += i` to `total += i * 2`
- C) Change `total += i * 2` to `total += i * 4`
- D) Change `total += i` to `total += i * 3`

---

## Code Block 6: String Iteration with Index

**Try this code:**
```python
word = "hello"
for i in range(len(word)):
    if i % 2 == 0:
        print(word[i].upper(), end="")
    else:
        print(word[i], end="")
```

**Question 11:** What does this code print?
- A) `HELLO`
- B) `HeLlO`
- C) `hElLo`
- D) `hello`

**Question 12:** How would you modify the code to print `hElLo`?
- A) Change condition to `if i % 2 == 1:`
- B) Change condition to `if i % 2 != 0:`
- C) Swap the print statements
- D) Change condition to `if i % 2 == 0:` and swap the print statements

---

## Code Block 7: Complex While Loop Logic

**Try this code:**
```python
n = 8
count = 0
while n > 1:
    if n % 2 == 0:
        n = n // 2
    else:
        n = n * 3 + 1
    count += 1
    print(n, end=" ")
print(f"\nSteps: {count}")
```

**Question 13:** What does this code print?
- A) `4 2 1` then `Steps: 3`
- B) `4 2 1` then `Steps: 4`
- C) `4 2 1` then `Steps: 2`
- D) `4 2 1` then `Steps: 5`

**Question 14:** How would you modify the code to start with `n = 6` and print `3 10 5 16 8 4 2 1`?
- A) Change `n = 8` to `n = 6`
- B) Change `n = 8` to `n = 6` and modify the logic
- C) Change `n = 8` to `n = 6` and change the condition
- D) Change `n = 8` to `n = 6` and change the operations

---

## Code Block 8: Loop with Multiple Conditions

**Try this code:**
```python
for i in range(1, 10):
    if i % 3 == 0 and i % 2 == 0:
        print("Both", end=" ")
    elif i % 3 == 0:
        print("Three", end=" ")
    elif i % 2 == 0:
        print("Two", end=" ")
    else:
        print(i, end=" ")
```

**Question 15:** What does this code print?
- A) `1 Two 3 Two 5 Both 7 Two 9`
- B) `1 Two 3 Two 5 Two 7 Two 9`
- C) `1 Two 3 Two 5 Both 7 Two 9`
- D) `1 Two 3 Two 5 Two 7 Two 9`

**Question 16:** How would you modify the code to print `1 Two 3 Two 5 Two 7 Two 9`?
- A) Remove the `elif i % 2 == 0:` condition
- B) Change `and` to `or` in the first condition
- C) Remove the `elif i % 3 == 0:` condition
- D) Change `and` to `or` in the first condition and remove `elif i % 2 == 0:`

---

## Challenge Questions

**Question 17:** In Code Block 3, what happens if you change `x -= 3` to `x -= 2`?
- A) The loop runs forever
- B) The loop prints `8 6 4 2 0`
- C) The loop prints `8 6 4 2`
- D) The loop prints `8 6 4 2 0 -2`

**Question 18:** In Code Block 7, what happens if you change `n = 8` to `n = 5`?
- A) The loop prints `16 8 4 2 1` then `Steps: 5`
- B) The loop prints `16 8 4 2 1` then `Steps: 6`
- C) The loop prints `16 8 4 2 1` then `Steps: 4`
- D) The loop prints `16 8 4 2 1` then `Steps: 7`

---



