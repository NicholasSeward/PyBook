# ASCII and Unicode

## Overview
Computers store text as numbers. ASCII and Unicode are systems that map characters to numbers.

## ASCII (American Standard Code)

ASCII uses 7 bits to represent 128 characters.

```python
# ASCII values for common characters
print(f"A = {ord('A')}")      # A = 65
print(f"a = {ord('a')}")      # a = 97
print(f"0 = {ord('0')}")      # 0 = 48
print(f"! = {ord('!')}")      # ! = 33
print(f"space = {ord(' ')}")  # space = 32

# Convert numbers back to characters
print(f"65 = {chr(65)}")      # 65 = A
print(f"97 = {chr(97)}")      # 97 = a
```

## Unicode

Unicode can represent over 1 million characters from many languages.

```python
# Unicode supports many languages
print(f"English A: {ord('A')}")           # English A: 65
print(f"Greek α: {ord('α')}")             # Greek α: 945
print(f"Chinese 中: {ord('中')}")          # Chinese 中: 20013
print(f"Emoji 😀: {ord('😀')}")           # Emoji 😀: 128512

# Convert back
print(f"945 = {chr(945)}")                # 945 = α
print(f"20013 = {chr(20013)}")            # 20013 = 中
```

## Working with Character Codes

### Check Character Types
```python
# Check if character is a letter
def is_letter(char):
    code = ord(char)
    return (65 <= code <= 90) or (97 <= code <= 122)

print(f"Is 'A' a letter? {is_letter('A')}")      # True
print(f"Is '5' a letter? {is_letter('5')}")      # False
print(f"Is '!' a letter? {is_letter('!')}")      # False
```

### Convert Case
```python
# Convert lowercase to uppercase using ASCII
def to_upper(char):
    if 'a' <= char <= 'z':
        # ASCII: 'a' = 97, 'A' = 65, difference = 32
        return chr(ord(char) - 32)
    return char

print(f"a -> {to_upper('a')}")  # a -> A
print(f"z -> {to_upper('z')}")  # z -> Z
print(f"A -> {to_upper('A')}")  # A -> A
```

## Real Example: Simple Encryption

```python
# Caesar cipher - shift letters by 3 positions
def caesar_encrypt(text, shift=3):
    result = ""
    for char in text:
        if char.isalpha():
            # Get ASCII value
            code = ord(char)
            # Determine base (A=65, a=97)
            base = 65 if char.isupper() else 97
            # Shift and wrap around alphabet
            shifted = (code - base + shift) % 26 + base
            result += chr(shifted)
        else:
            result += char  # Keep non-letters unchanged
    return result

def caesar_decrypt(text, shift=3):
    return caesar_encrypt(text, -shift)

# Test encryption
message = "Hello World!"
encrypted = caesar_encrypt(message)
decrypted = caesar_decrypt(encrypted)

print(f"Original: {message}")
print(f"Encrypted: {encrypted}")
print(f"Decrypted: {decrypted}")
```

**Output:**
```
Original: Hello World!
Encrypted: Khoor Zruog!
Decrypted: Hello World!
```

## String Methods and Encoding

### Encoding Strings
```python
# Convert string to bytes
text = "Hello, 世界!"
bytes_data = text.encode('utf-8')
print(f"Bytes: {bytes_data}")

# Convert bytes back to string
decoded_text = bytes_data.decode('utf-8')
print(f"Decoded: {decoded_text}")
```

### Check String Properties
```python
# Check if string contains only ASCII
def is_ascii(text):
    return all(ord(char) < 128 for char in text)

print(f"Is 'Hello' ASCII? {is_ascii('Hello')}")           # True
print(f"Is 'Hello 世界' ASCII? {is_ascii('Hello 世界')}")  # False
```

## Key Points

- **ASCII** - 128 characters, mainly English
- **Unicode** - over 1 million characters, all languages
- **`ord()`** - get character code
- **`chr()`** - get character from code
- **UTF-8** - common way to encode Unicode

## Summary

✅ **ASCII** - basic English characters (128 total)  
✅ **Unicode** - all world languages (1M+ characters)  
✅ **`ord()`** - character to number  
✅ **`chr()`** - number to character  
✅ **UTF-8** - standard encoding for Unicode  

Understanding encoding helps you work with text from different languages!
