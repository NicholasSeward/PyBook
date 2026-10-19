# Tutorial (Module 8 - File IO)

---

## Code Block 1: Basic File Writing

**Try this code:**

```py
with open("output.txt", "w") as file:
    file.write("Hello World\n")
    file.write("Python File IO")
print("File written successfully")
```

**Question 1:** What does this code print?
- A) `Hello World\nPython File IO`
- B) `File written successfully`
- C) `Hello World` then `Python File IO`
- D) Nothing

**Question 2:** How would you modify the code to append to the file instead of overwriting it?
- A) Change `"w"` to `"a"`
- B) Change `"w"` to `"r"`
- C) Change `file.write()` to `file.append()`
- D) Change `with` to `append`

---

## Code Block 2: Reading Files All at Once

**Try this code:**

```py
# @file: main.py
with open("data.txt", "r") as file:
    content = file.read()
    print(len(content))

# @file: data.txt
Line 1
Line 2
Line 3
```

**Question 3:** What does this code print (the file contains `"Line 1\nLine 2\nLine 3"`)?
- A) `3`
- B) `21`
- C) `24`
- D) `27`

**Question 4:** How would you modify the code to print each line separately?
- A) Change `file.read()` to `file.readlines()`
- B) Change `file.read()` to `file.readline()`
- C) Use a `for` loop: `for line in file: print(line)`
- D) Both A and C would work

---

## Code Block 3: Reading Files Line by Line

**Try this code:**

```py
# @file: main.py
total = 0
with open("numbers.txt", "r") as file:
    for line in file:
        total += int(line.strip())
print(total)

# @file: numbers.txt
10
20
30
```

**Question 5:** What does this code print?
- A) `60`
- B) `102030`
- C) `10` then `20` then `30`
- D) `6`

**Question 6:** How would you modify the code to count the number of lines instead of summing the numbers?
- A) Change `total += int(line.strip())` to `total += 1`
- B) Use `len(file.readlines())`
- C) Change `total = 0` to `total = len(file)`
- D) Both A and B would work

---

## Code Block 4: File Open Modes

**Try this code:**

```py
with open("test.txt", "w") as file:
    file.write("First line\n")

with open("test.txt", "a") as file:
    file.write("Second line\n")

with open("test.txt", "r") as file:
    print(file.read())
```

**Question 7:** What does this code print?
- A) `First line`
- B) `Second line`
- C) `First line` then `Second line`
- D) `First line\nSecond line\n`

**Question 8:** How would you modify the code so the file only contains `"Second line\n"`?
- A) Change the second `"a"` to `"w"`
- B) Remove the first `with` block
- C) Change the first `"w"` to `"a"`
- D) Both A and B would work

---

## Code Block 5: File Paths

**Try this code:**

```py
import os

path = os.path.join("folder", "subfolder", "file.txt")
print(path)
exists = os.path.exists(path)
print(exists)
```

**Question 9:** What does this code print (on Windows)?
- A) `folder/subfolder/file.txt` then `False`
- B) `folder\subfolder\file.txt` then `False`
- C) `folder/subfolder/file.txt` then `True`
- D) `folder\subfolder\file.txt` then `True`

**Question 10:** How would you modify the code to check if the path is a directory?
- A) Change `os.path.exists(path)` to `os.path.isdir(path)`
- B) Change `os.path.exists(path)` to `os.path.isfile(path)`
- C) Change `os.path.exists(path)` to `os.path.isdirectory(path)`
- D) Change `os.path.exists(path)` to `path.isdir()`

---

## Code Block 6: Error Handling with try-except

**Try this code:**

```py
try:
    with open("nonexistent.txt", "r") as file:
        content = file.read()
    print("File read successfully")
except FileNotFoundError:
    print("File not found")
print("Program continues")
```

**Question 11:** What does this code print?
- A) `File read successfully` then `Program continues`
- B) `File not found` then `Program continues`
- C) `File not found`
- D) Error message

**Question 12:** How would you modify the code to create the file if it doesn't exist?
- A) Add `with open("nonexistent.txt", "w") as file: pass` in the except block
- B) Change `"r"` to `"w"` in the try block
- C) Remove the try-except block
- D) Change `FileNotFoundError` to `FileExistsError`

---

## Code Block 7: Writing Multiple Lines

**Try this code:**

```py
lines = ["Apple\n", "Banana\n", "Cherry\n"]
with open("fruits.txt", "w") as file:
    file.writelines(lines)
print(len(lines))
```

**Question 13:** What does this code print to the console? And what is written to `fruits.txt`?
- A) Prints `3`, file contains: `Apple\nBanana\nCherry\n`
- B) Prints `3`, file contains: `Apple Banana Cherry`
- C) Prints `Apple Banana Cherry`, file contains: `3`
- D) Prints `21`, file contains: `Apple\nBanana\nCherry\n`

**Question 14:** How would you modify the code to add line numbers before each fruit?
- A) Use `enumerate()`: `file.writelines([f"{i+1}. {line}" for i, line in enumerate(lines)])`
- B) Change `writelines()` to `write()`
- C) Use a loop: `for i, line in enumerate(lines): file.write(f"{i+1}. {line}")`
- D) Both A and C would work

---

## Code Block 8: Reading with readlines()

**Try this code:**

```py
# @file: main.py
with open("colors.txt", "r") as file:
    lines = file.readlines()
print(lines[1].strip())
print(len(lines))

# @file: colors.txt
Red
Green
Blue
```

**Question 15:** What does this code print?
- A) `Red` then `3`
- B) `Green` then `3`
- C) `Green` then `2`
- D) `Red` then `2`

**Question 16:** How would you modify the code to print all lines in reverse order?
- A) Change `lines[1].strip()` to `lines[::-1]`
- B) Use `for line in reversed(lines): print(line.strip())`
- C) Change `readlines()` to `readlines()[::-1]`
- D) Use `lines.reverse()` then print each line

---

## Code Block 9: Serialization with Pickle

**Try this code:**

```py
import pickle

data = {"name": "Alice", "age": 25, "city": "NYC"}
with open("person.pkl", "wb") as file:
    pickle.dump(data, file)
print("Data saved")

with open("person.pkl", "rb") as file:
    data2 = pickle.load(file)
print("Data loaded:", data2)
print("Are they equal?", data == data2)
```

**Question 17:** What does this code print?
- A) `Data saved` then `Data loaded: {'name': 'Alice', 'age': 25, 'city': 'NYC'}` then `Are they equal? True`
- B) `Data saved` then `Data loaded: person.pkl` then `Are they equal? False`
- C) `{'name': 'Alice', 'age': 25, 'city': 'NYC'}` then `True`
- D) `Data saved` only

**Question 18:** How would you modify the code to save and load a list instead of a dictionary?
- A) Change `data` to `['Alice', 25, 'NYC']` - `pickle.dump()` and `pickle.load()` work the same way
- B) Change `pickle.dump()` to `pickle.dump_list()`
- C) Change the file mode from `"wb"` to `"w"`
- D) Lists cannot be pickled
