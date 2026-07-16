
# Tutorial (Module 7 - String Manipulation)

## Code Block 1: Strings as Sequences

**Try this code:**
```python
word = "Python"
for char in word:
    print(char, end="-")
```

**Question 1:** What does this code print?
- A) `Python`
- B) `P-y-t-h-o-n-`
- C) `P-y-t-h-o-n`
- D) `Python-`

**Question 2:** How would you modify the code to print `P*y*t*h*o*n*`?
- A) Change `end="-"` to `end="*"`
- B) Change `print(char, end="-")` to `print(char + "*")`
- C) Change `for char in word:` to `for char in word + "*":`
- D) Change `end="-"` to `sep="*"`

---

## Code Block 2: String Indexing and Slicing (Part 1)

**Try this code:**
```python
text = "Programming"
print(text[0])
print(text[-1])
print(text[4:8])
```

**Question 3:** What does this code print?
- A) `P` then `g` then `ramm`
- B) `P` then `g` then `gram`
- C) `0` then `-1` then `ramm`
- D) `P` then `g` then `rami`

**Question 4:** How would you modify the code to print `P` then `g` then `ogramming`?
- A) Change `text[4:8]` to `text[2:]`
- B) Change `text[4:8]` to `text[2:11]`
- C) Change `text[4:8]` to `text[2:10]`
- D) Change `text[4:8]` to `text[2:12]`

---

## Code Block 3: String Indexing and Slicing (Part 2)

**Try this code:**
```python
word = "abcdefgh"
result = word[1:7:2]
print(result)
```

**Question 5:** What does this code print?
- A) `bdf`
- B) `aceg`
- C) `bdfh`
- D) `ace`

**Question 6:** How would you modify the code to print `hgfedcba`?
- A) Change `word[1:7:2]` to `word[::-1]`
- B) Change `word[1:7:2]` to `word[-1:0:-1]`
- C) Change `word[1:7:2]` to `word[7:0:-1]`
- D) Change `word[1:7:2]` to `word.reverse()`

---

## Code Block 4: String Methods (Part 1)

**Try this code:**
```python
text = "hello world"
print(text.upper())
print(text.replace("o", "0"))
print(text.count("l"))
```

**Question 7:** What does this code print?
- A) `HELLO WORLD` then `hell0 w0rld` then `3`
- B) `hello world` then `hell0 w0rld` then `3`
- C) `HELLO WORLD` then `hell0 w0rld` then `2`
- D) `HELLO WORLD` then `hello world` then `3`

**Question 8:** How would you modify the code to make the second line print `he110 w0r1d`?
- A) Change `replace("o", "0")` to `replace("lo", "10")`
- B) Add another `replace("l", "1")` call: `text.replace("o", "0").replace("l", "1")`
- C) Change `replace("o", "0")` to `replace("lo", "10").replace("l", "1")`
- D) Change `replace("o", "0")` to `replace("o", "0").replace("ll", "11")`

---

## Code Block 5: String Methods (Part 2)

**Try this code:**
```python
sentence = "  Python Programming  "
print(sentence.strip())
print(sentence.split())
print("-".join(["a", "b", "c"]))
```

**Question 9:** What does this code print?
- A) `Python Programming` then `['Python', 'Programming']` then `a-b-c`
- B) `  Python Programming  ` then `['Python', 'Programming']` then `a-b-c`
- C) `Python Programming` then `['  Python Programming  ']` then `abc`
- D) `Python Programming` then `['Python', 'Programming']` then `['a', 'b', 'c']`

**Question 10:** How would you modify the code to make the last line print `a*b*c`?
- A) Change `"-".join(["a", "b", "c"])` to `"*".join(["a", "b", "c"])`
- B) Change `"-".join(["a", "b", "c"])` to `"-".join("*", ["a", "b", "c"])`
- C) Change `"-".join(["a", "b", "c"])` to `join("-", ["a", "b", "c"])`
- D) Change `"-".join(["a", "b", "c"])` to `["a", "b", "c"].join("*")`

---

## Code Block 6: String Methods (Part 3)

**Try this code:**
```python
text = "Python3"
print(text.isalpha())
print(text.isalnum())
print(text.startswith("Py"))
print(text.endswith("3"))
```

**Question 11:** What does this code print?
- A) `False` then `True` then `True` then `True`
- B) `True` then `True` then `True` then `True`
- C) `False` then `False` then `True` then `True`
- D) `True` then `False` then `True` then `True`

**Question 12:** How would you modify the code to make the first line print `True`?
- A) Change `text = "Python3"` to `text = "Python"`
- B) Change `text.isalpha()` to `text.isalnum()`
- C) Change `text.isalpha()` to `text.isdigit()`
- D) Change `text = "Python3"` to `text = "3Python"`

---

## Code Block 7: Pattern Matching with Regex

**Try this code:**
```python
import re
text = "My phone is 555-1234"
pattern = r"\d{3}-\d{4}"
match = re.search(pattern, text)
if match:
    print(match.group())
```

**Question 13:** What does this code print?
- A) `555-1234`
- B) `My phone is 555-1234`
- C) `555`
- D) `1234`

**Question 14:** How would you modify the pattern to match phone numbers in the format `(555) 1234`?
- A) Change `r"\d{3}-\d{4}"` to `r"\(\d{3}\) \d{4}"`
- B) Change `r"\d{3}-\d{4}"` to `r"(\d{3}) \d{4}"`
- C) Change `r"\d{3}-\d{4}"` to `r"\d{3} \d{4}"`
- D) Change `r"\d{3}-\d{4}"` to `r"[\d{3}] \d{4}"`

---

## Code Block 8: Regex Patterns

**Try this code:**
```python
import re
text = "The price is $25 and $30"
numbers = re.findall(r"\$\d+", text)
print(numbers)
```

**Question 15:** What does this code print?
- A) `['25', '30']`
- B) `['$25', '$30']`
- C) `['$', '25', '$', '30']`
- D) `['$25 and $30']`

**Question 16:** How would you modify the code to print `['25', '30']` (without the dollar signs)?
- A) Change `r"\$\d+"` to `r"\d+"`
- B) Change `r"\$\d+"` to `r"$\d+"`
- C) Change `r"\$\d+"` to `r"[\$]\d+"`
- D) Change `r"\$\d+"` to `r"\\\$\d+"`

---

## Code Block 9: ASCII and Unicode

**Try this code:**
```python
print(ord('A'))
print(ord('a'))
print(chr(65))
print(chr(97))
```

**Question 17:** What does this code print?
- A) `65` then `97` then `A` then `a`
- B) `A` then `a` then `65` then `97`
- C) `65` then `97` then `a` then `A`
- D) `97` then `65` then `a` then `A`

**Question 18:** How would you modify the code to print `90` then `122` then `Z` then `z`?
- A) Change `'A'` to `'Z'` and `'a'` to `'z'`
- B) Change `65` to `90` and `97` to `122`
- C) Change `'A'` to `'Z'`, `'a'` to `'z'`, `65` to `90`, and `97` to `122`
- D) Change `'A'` to `'z'` and `'a'` to `'Z'`

---

## Code Block 10: ASCII Operations

**Try this code:**
```python
text = "ABC"
result = ""
for char in text:
    result += chr(ord(char) + 1)
print(result)
```

**Question 19:** What does this code print?
- A) `ABC`
- B) `BCD`
- C) `DEF`
- D) `123`

**Question 20:** How would you modify the code to print `XYZ` when starting with `text = "ABC"`?
- A) Change `ord(char) + 1` to `ord(char) + 23`
- B) Change `ord(char) + 1` to `ord(char) + 25`
- C) Change `ord(char) + 1` to `ord(char) + 24`
- D) Change `ord(char) + 1` to `ord(char) - 3`

---

## Code Block 11: Escape Characters

**Try this code:**
```python
text = "Hello\nWorld\tPython"
print(text)
```

**Question 21:** What does this code print?
- A) `Hello\nWorld\tPython`
- B) `Hello` on one line, then `World    Python` on the next line
- C) `HelloWorldPython`
- D) `Hello World Python`

**Question 22:** How would you modify the code to print `Hello\nWorld\tPython` literally (with the backslashes visible)?
- A) Change `"Hello\nWorld\tPython"` to `"Hello\\nWorld\\tPython"`
- B) Change `"Hello\nWorld\tPython"` to `r"Hello\nWorld\tPython"`
- C) Change `"Hello\nWorld\tPython"` to `'Hello\nWorld\tPython'`
- D) Both A and B are correct

---

## Code Block 12: Escape Sequences in Action

**Try this code:**
```python
path = "C:\\Users\\Documents"
quote = 'She said, "Hello"'
print(path)
print(quote)
```

**Question 23:** What does this code print?
- A) `C:\Users\Documents` then `She said, "Hello"`
- B) `C:\\Users\\Documents` then `She said, "Hello"`
- C) `C:\Users\Documents` then `She said, Hello`
- D) `C:UsersDocuments` then `She said, "Hello"`

**Question 24:** How would you modify the code to print `C:/Users/Documents` instead?
- A) Change `"C:\\Users\\Documents"` to `"C:/Users/Documents"`
- B) Change `"C:\\Users\\Documents"` to `"C:\Users\Documents"`
- C) Change `"C:\\Users\\Documents"` to `r"C:/Users/Documents"`
- D) Change `"C:\\Users\\Documents"` to `'C:/Users/Documents'`

---

## Challenge Questions

**Question 25:** In Code Block 4, what happens if you chain multiple string methods like `text.upper().replace("O", "0").count("L")`?
- A) It prints `2`
- B) It prints `3`
- C) It prints `0`
- D) It causes an error

**Question 26:** In Code Block 8, how would you modify the regex pattern to match both `$25` and `£30` (different currency symbols)?
- A) Change `r"\$\d+"` to `r"[$£]\d+"`
- B) Change `r"\$\d+"` to `r"[\$£]\d+"`
- C) Change `r"\$\d+"` to `r"($|£)\d+"`
- D) Change `r"\$\d+"` to `r"\$|\£\d+"`

**Question 27:** In Code Block 10, what happens if you change `ord(char) + 1` to `ord(char) - 32` for the text `"abc"`?
- A) It prints `ABC`
- B) It prints `def`
- C) It prints `012`
- D) It causes an error

---



