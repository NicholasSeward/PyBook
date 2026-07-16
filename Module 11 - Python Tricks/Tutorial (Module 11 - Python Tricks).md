# Tutorial (Module 11 - Python Tricks)

## Setup

Some sections use these imports:

```python
from collections import Counter, defaultdict
import copy
```

---

## Sets (dedup + membership)

**Try this code:**

```python
emails = ["a@x.com", "b@x.com", "a@x.com", "c@x.com"]
unique = sorted(set(emails))
print(unique)  # expected: ['a@x.com', 'b@x.com', 'c@x.com']
```

**Note:** For Question 1 and Question 2, assume you start from the code above each time (do not “carry over” changes unless a question explicitly says to).

**Question 1:** If you change `unique = sorted(set(emails))` to `unique = list(set(emails))`, which statement is true?
- A) It will always print the same order
- B) It will contain the same unique items, but the order may vary
- C) It will keep duplicates
- D) It will crash

**Question 2:** Which change makes membership testing fast (even if there are a billion emails) when checking if an email is already seen?
- A) Keep `emails` as a list and use `in`
- B) Convert to a set and use `in`
- C) Sort the list every time
- D) Use `print()` to compare values

---

## List Comprehensions (filter + map)

**Try this code:**

```python
nums = [1, 2, 3, 4, 5, 6]
squares_of_evens = [n * n for n in nums if n % 2 == 0]
print(squares_of_evens)  # expected: [4, 16, 36]
```

**Note:** For Question 3 and Question 4, assume you start from the code above each time.

**Question 3:** What change makes it print `[1, 9, 25]` instead?
- A) Change the filter to `if n % 2 == 1`
- B) Change `n * n` to `n`
- C) Change `nums` to `range(1, 7)`
- D) Remove the filter entirely

**Question 4:** If you change `n * n` to `n ** 3`, what will the list become?
- A) `[8, 64, 216]`
- B) `[1, 8, 27, 64, 125, 216]`
- C) `[4, 16, 36]`
- D) It crashes

---

## Dict Comprehensions

**Try this code:**

```python
words = ["apple", "banana", "cherry"]
length_by_word = {w: len(w) for w in words}
print(length_by_word)  # expected: {'apple': 5, 'banana': 6, 'cherry': 6}
```

**Note:** For Question 5 and Question 6, assume you start from the code above each time.

**Question 5:** If you change `len(w)` to `w[0]`, what does `length_by_word["banana"]` become?
- A) `6`
- B) `"banana"`
- C) `"b"`
- D) KeyError

**Question 6:** Which comprehension keeps only words with length 6 or more?
- A) `{w: len(w) for w in words if len(w) >= 6}`
- B) `{len(w): w for w in words}`
- C) `{w: len(w) if len(w) >= 6 for w in words}`
- D) `{w: len(w) for w in words} >= 6`

---

## `enumerate` (index + value)

**Try this code:**

```python
items = ["zero", "one", "two"]
labels = [f"{i}: {val}" for i, val in enumerate(items)]
print(labels)  # expected: ['0: zero', '1: one', '2: two']
```

**Note:** For Question 7 and Question 8, assume you start from the code above each time.

**Question 7:** What change makes it start counting at 1 instead of 0?
- A) `enumerate(items, start=1)`
- B) `enumerate(items, step=1)`
- C) `range(items)`
- D) `items.enumerate()`

**Question 8:** If you change the f-string to `f"{val}: {i}"`, what is `labels[0]`?
- A) `"zero: 0"`
- B) `"0: zero"`
- C) `"one: 1"`
- D) It crashes

---

## `zip` (combine lists)

**Try this code:**

```python
first = ["Ada", "Linus", "Grace"]
last = ["Lovelace", "Torvalds", "Hopper"]
full = [f"{f} {l}" for f, l in zip(first, last)]
print(full)  # expected: ['Ada Lovelace', 'Linus Torvalds', 'Grace Hopper']
```

**Note:** For Question 9 and Question 10, assume you start from the code above each time.

**Question 9:** If you swap the loop variables like this:

```python
full = [f"{l} {f}" for l, f in zip(first, last)]
```

what will `full[0]` be?
- A) `"Ada Lovelace"`
- B) `"Lovelace Ada"`
- C) `"Ada Torvalds"`
- D) It crashes

**Question 10:** What happens if `last` is shorter than `first`?
- A) `zip` pads with `None`
- B) `zip` stops at the shortest list
- C) `zip` throws an error
- D) `zip` repeats the last name

---

## `any` / `all` (boolean checks)

**Try this code:**

```python
passwords = ["weak", "Better123", "NoDigits!", "Str0ng!"]
has_digit = any(ch.isdigit() for pw in passwords for ch in pw)
has_bang = any("!" in pw for pw in passwords)
print(has_digit, has_bang)  # expected: True True
```

**Note:** For Question 11 and Question 12, assume you start from the code above each time.

**Question 11:** If you change `any(...)` to `all(...)` for `has_digit`, what prints?
- A) `True True`
- B) `False True`
- C) `True False`
- D) `False False`

**Question 12:** Which expression checks whether **every** password has at least one digit?
- A) `all(ch.isdigit() for pw in passwords for ch in pw)`
- B) `all(any(ch.isdigit() for ch in pw) for pw in passwords)`
- C) `any(all(ch.isdigit() for ch in pw) for pw in passwords)`
- D) `any(ch.isdigit() for pw in passwords for ch in pw)`

---

## Slicing Tricks

**Try this code:**

```python
data = [10, 20, 30, 40, 50, 60]
rev = data[::-1]
odds = data[1::2]
print(rev, odds)  # expected: [60, 50, 40, 30, 20, 10] [20, 40, 60]
```

**Note:** For Question 13 and Question 14, assume you start from the code above each time.

**Question 13:** What does `data[::2]` produce for this list?
- A) `[20, 40, 60]`
- B) `[10, 30, 50]`
- C) `[10, 20, 30]`
- D) It crashes

**Question 14:** If you change `data[::-1]` to `data[-1:0:-1]`, what is missing from the reversed list?
- A) `10`
- B) `20`
- C) `60`
- D) Nothing is missing

---

## `collections.Counter`

**Try this code:**

```python
from collections import Counter

words = ["red", "blue", "red", "green", "blue", "red"]
top2 = Counter(words).most_common(2)
print(top2)  # expected: [('red', 3), ('blue', 2)]
```

**Note:** For Question 15 and Question 16, assume you start from the code above each time.

**Question 15:** If you change `most_common(2)` to `most_common(1)`, what prints?
- A) `[('red', 3)]`
- B) `[('red', 3), ('blue', 2)]`
- C) `('red', 3)`
- D) `{'red': 3}`

**Question 16:** What expression extracts just the most common word (the string) from `most_common(1)`?
- A) `Counter(words).most_common(1)[0]`
- B) `Counter(words).most_common(1)[0][0]`
- C) `Counter(words).most_common(1)[1]`
- D) `Counter(words).most_common(1).key`

---

## `collections.defaultdict`

**Try this code:**

```python
from collections import defaultdict

pairs = [("a", 1), ("b", 2), ("a", 3)]
groups = defaultdict(list)
for k, v in pairs:
    groups[k].append(v)
print(dict(groups))  # expected: {'a': [1, 3], 'b': [2]}
```

**Note:** For Question 17 and Question 18, assume you start from the code above each time.

**Question 17:** If you change `groups = defaultdict(list)` to `groups = {}` without changing anything else, what happens?
- A) It prints the same result
- B) It prints `{'a': 3, 'b': 2}`
- C) It silently creates lists anyway
- D) It crashes because a key is missing

**Question 18:** Why is `defaultdict(list)` useful here?
- A) It prevents duplicates automatically
- B) It automatically creates an empty list for a missing key
- C) It sorts keys automatically
- D) It makes dicts immutable

---

## Generator Expressions (`sum`)

**Try this code:**

```python
nums = range(1, 101)
total = sum(n * n for n in nums)
print(total)  # expected: 338350
```

**Note:** For Question 19 and Question 20, assume you start from the code above each time.

**Question 19:** If you change `range(1, 101)` to `range(1, 11)`, what prints?
- A) `5050`
- B) `338350`
- C) `385`
- D) `100`

**Question 20:** Which is the best description of a generator expression in `sum(...)`?
- A) It builds the full list in memory first
- B) It produces values one at a time (lazy)
- C) It always runs faster than a list comprehension
- D) It only works with numbers

---

## f-Strings and Format Specs

**Try this code:**

```python
name = "Ada"
score = 9.4567
msg = f"{name} - {score:.2f}/10"
print(msg)  # expected: Ada - 9.46/10
```

**Note:** For Question 21 and Question 22, assume you start from the code above each time.

**Question 21:** If you change `.2f` to `.1f`, what prints?
- A) `Ada - 9.5/10`
- B) `Ada - 9.4/10`
- C) `Ada - 9.46/10`
- D) It crashes

**Question 22:** Which change produces `Ada - 9.457/10` from this starting point?

```python
msg = f"{name} - {score}/10"
```

- A) `f"{name} - {score:3f}/10"`
- B) `f"{name} - {score:03}/10"`
- C) `f"{name} - {score:.3f}/10"`
- D) `f"{name} - {score:.03}/10"`

---

## With (Context Managers)

**Try this code:**

```python
path = "sample.txt"
with open(path, "w", encoding="utf-8") as f:
    f.write("hello\nworld\n")

with open(path, "r", encoding="utf-8") as f:
    content = f.read()

print(content.splitlines())  # expected: ['hello', 'world']
```

**Note:** For Question 23 and Question 24, assume you start from the code above each time.

**Question 23:** If you change the write mode from `"w"` to `"a"` and run the program **twice**, what will the file contain after the second run?
- A) `hello` and `world` once
- B) Only the second run’s lines
- C) `hello` and `world` twice
- D) The file is empty

**Question 24:** Why is `with open(...) as f:` preferred over manually calling `open()` then `close()`?
- A) It makes the file read-only
- B) It automatically closes the file even if something goes wrong
- C) It loads the whole file into memory
- D) It makes Python run faster

---

## Extended Iterable Unpacking

**Try this code:**

```python
values = [10, 20, 30, 40, 50]
head, *middle, tail = values
print(head, middle, tail)  # expected: 10 [20, 30, 40] 50
```

**Note:** For Question 25 and Question 26, assume you start from the code above each time.

**Question 25:** If you change it to `head, *middle = values`, what happens?
- A) `head` is 10 and `middle` is `[20, 30, 40]`
- B) `head` is 10 and `middle` is `[20, 30, 40, 50]`
- C) `head` is 50 and `middle` is `[10, 20, 30, 40]`
- D) It crashes

**Question 26:** Which line puts the first two items of `values` into `a` and `b`, and the remaining items (as a list) into `rest`?
- A) `a, *rest, b = values`
- B) `*rest, a, b = values`
- C) `a, b, *rest = values`
- D) `a, *b, rest = values`

---

## Ternary Expressions

**Try this code:**

```python
age = 18
label = "adult" if age >= 18 else "minor"
print(label)  # expected: adult
```

**Note:** For Question 27 and Question 28, assume you start from the code above each time.

**Question 27:** If you change the condition to `age > 18`, what prints?
- A) `adult`
- B) `minor`
- C) `True`
- D) `False`

**Question 28:** Which is a correct ternary expression to check if someone is a teen (age between 13 and 19)?
- A) `"teen" if 13 <= age <= 19 else "not teen"`
- B) `if 13 <= age <= 19: "teen" else "not teen"`
- C) `"teen" if age >= 13 else "not teen"`
- D) `"teen" else "not teen" if 13 <= age <= 19`

---

## Walrus Operator (`:=`) [Python 3.8+]

**Try this code:**

```python
def fetch():
    return "data"

if (result := fetch()):
    print(result)
```

**Note:** For Question 29 and Question 30, assume you start from the code above each time.

**Question 29:** If `fetch()` returns `""` (empty string), what happens?
- A) It prints a blank line
- B) It prints nothing
- C) It crashes
- D) It prints `result`

**Question 30:** What is the main benefit of the walrus operator here?
- A) It makes strings immutable
- B) It lets you assign and use a value in the same expression
- C) It prevents aliasing
- D) It guarantees random output

---

## Sorting with `lambda` (exam-focus trick)

**Try this code:**

```python
students = [
    {"name": "Ada", "score": 92},
    {"name": "Linus", "score": 88},
    {"name": "Grace", "score": 95},
]
sorted_students = sorted(students, key=lambda s: (-s["score"], s["name"]))
print([s["name"] for s in sorted_students])  # expected: ['Grace', 'Ada', 'Linus']
```

**Note:** For Question 31 and Question 32, assume you start from the code above each time.

**Question 31:** If you change the key to `key=lambda s: (s["score"], s["name"])`, what prints?
- A) `['Grace', 'Ada', 'Linus']`
- B) `['Ada', 'Grace', 'Linus']`
- C) `['Linus', 'Ada', 'Grace']`
- D) It crashes

**Question 32:** Why does `-s["score"]` make scores sort from high to low?
- A) Negative numbers are always sorted last
- B) It reverses alphabetical order
- C) Larger scores become “smaller” negatives (so they come first)
- D) It only works for strings

