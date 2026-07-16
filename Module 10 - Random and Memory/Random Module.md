# Random Module

## Overview
The `random` module gives you tools to generate random numbers and make random choices.

## Basic Random Functions

### `random()` - Random Float
```python
import random

# Generate random float between 0.0 and 1.0
print(f"Random float: {random.random()}")  # 0.0 to 1.0
print(f"Random float: {random.random()}")  # Different each time
```

### `randint()` - Random Integer
```python
import random

# Generate random integer between 1 and 10 (inclusive)
print(f"Random number 1-10: {random.randint(1, 10)}")
print(f"Random number 1-10: {random.randint(1, 10)}")

# Generate random integer between -5 and 5
print(f"Random number -5 to 5: {random.randint(-5, 5)}")
```

### `choice()` - Random Choice from List
```python
import random

# Pick random item from a list
fruits = ["apple", "banana", "orange", "grape"]
print(f"Random fruit: {random.choice(fruits)}")
print(f"Random fruit: {random.choice(fruits)}")

# Pick random number from range
numbers = list(range(1, 11))  # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(f"Random number: {random.choice(numbers)}")
```

## More Random Functions

### `shuffle()` - Shuffle a List
```python
import random

# Shuffle a list in place
cards = ["A♠", "K♠", "Q♠", "J♠", "10♠"]
print(f"Original: {cards}")

random.shuffle(cards)
print(f"Shuffled: {cards}")

# Shuffle again
random.shuffle(cards)
print(f"Shuffled again: {cards}")
```

### `sample()` - Random Sample
```python
import random

# Pick 3 random items without repeating
students = ["Alice", "Bob", "Charlie", "Diana", "Eve", "Frank"]
picked = random.sample(students, 3)
print(f"Random students: {picked}")

# Pick 2 random numbers from 1-20
numbers = random.sample(range(1, 21), 2)
print(f"Random numbers: {numbers}")
```

### `uniform()` - Random Float in Range
```python
import random

# Random float between 0.0 and 10.0
print(f"Random float 0-10: {random.uniform(0.0, 10.0):.2f}")

# Random float between -1.0 and 1.0
print(f"Random float -1 to 1: {random.uniform(-1.0, 1.0):.3f}")
```

## Setting the Seed

### Reproducible Random Numbers
```python
import random

# Set seed for reproducible results
random.seed(42)

print("With seed 42:")
print(f"Random 1-10: {random.randint(1, 10)}")
print(f"Random 1-10: {random.randint(1, 10)}")
print(f"Random 1-10: {random.randint(1, 10)}")

# Reset seed
random.seed(42)
print("\nWith seed 42 again:")
print(f"Random 1-10: {random.randint(1, 10)}")
print(f"Random 1-10: {random.randint(1, 10)}")
print(f"Random 1-10: {random.randint(1, 10)}")
```

## Real Example: Dice Game

```python
import random

def roll_dice():
    """Roll two dice and return their values"""
    die1 = random.randint(1, 6)
    die2 = random.randint(1, 6)
    return die1, die2

def play_dice_game():
    """Play a simple dice game"""
    print("Rolling dice...")
    
    # Roll dice
    die1, die2 = roll_dice()
    total = die1 + die2
    
    print(f"Die 1: {die1}")
    print(f"Die 2: {die2}")
    print(f"Total: {total}")
    
    # Check for special rolls
    if total == 7:
        print("Lucky seven!")
    elif total == 2:
        print("Snake eyes!")
    elif total == 12:
        print("Boxcars!")
    elif total >= 10:
        print("High roll!")
    elif total <= 4:
        print("Low roll!")
    
    return total

# Play the game
print("=== Dice Game ===")
score1 = play_dice_game()
print()
score2 = play_dice_game()
print()

# Determine winner
if score1 > score2:
    print(f"Player 1 wins with {score1} vs {score2}")
elif score2 > score1:
    print(f"Player 2 wins with {score2} vs {score1}")
else:
    print(f"It's a tie! Both rolled {score1}")
```

## Random Password Generator

```python
import random
import string

def generate_password(length=8):
    """Generate a random password"""
    # Characters to choose from
    letters = string.ascii_letters  # a-z, A-Z
    digits = string.digits          # 0-9
    symbols = "!@#$%^&*()_+-="     # Special characters
    
    # Make sure we have at least one of each type
    password = [
        random.choice(letters),  # One letter
        random.choice(digits),   # One digit
        random.choice(symbols)   # One symbol
    ]
    
    # Fill the rest randomly
    all_chars = letters + digits + symbols
    for _ in range(length - 3):
        password.append(random.choice(all_chars))
    
    # Shuffle the password
    random.shuffle(password)
    return ''.join(password)

# Generate some passwords
print("Random passwords:")
for i in range(5):
    password = generate_password(10)
    print(f"Password {i+1}: {password}")
```

## Key Points

- **`random.random()`** - float between 0.0 and 1.0
- **`random.randint(a, b)`** - integer between a and b (inclusive)
- **`random.choice(list)`** - random item from list
- **`random.shuffle(list)`** - shuffle list in place
- **`random.seed(n)`** - set seed for reproducible results

## Summary

✅ **`random()`** - random float 0.0 to 1.0  
✅ **`randint()`** - random integer in range  
✅ **`choice()`** - random item from list  
✅ **`shuffle()`** - randomize list order  
✅ **`seed()`** - make random numbers reproducible  

The random module makes your programs unpredictable and fun!
