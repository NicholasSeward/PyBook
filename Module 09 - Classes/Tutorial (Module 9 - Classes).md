# Tutorial (Module 9 - Classes)

## Code Block 1: Basic Class Definition

**Try this code:**

```python
class Dog:
    """Represents a dog."""
    pass

# Create a dog
my_dog = Dog()
my_dog.name = "Buddy"
my_dog.age = 3

print(my_dog.name)
print(my_dog.age)
```

**Question 1:** What does this code print?
- A) `Dog` then `None`
- B) `Buddy` then `3`
- C) `name` then `age`
- D) Error

**Question 2:** Remove the `pass` statement and run the code again. What happens?
- A) The code runs normally
- B) You get a syntax error
- C) The output changes
- D) Nothing changes

---

## Code Block 2: Adding Methods to a Class

**Try this code:**

```python
class Cat:
    """Represents a cat."""
    
    def speak(self):
        return "Meow"
    
    def eat(self, food):
        return f"The cat is eating {food}"

# Create and use a cat
my_cat = Cat()
print(my_cat.speak())
print(my_cat.eat("fish"))
```

**Question 3:** What does this code print?
- A) `Meow` then `The cat is eating fish`
- B) `speak` then `eat`
- C) `Cat` then `None`
- D) Error

**Question 4:** Change the `speak` method to take no parameters (remove `self`), then try to call it. What happens?
- A) It runs fine and prints the expected output
- B) You get a TypeError when calling the method
- C) The output is different
- D) No error, but nothing prints

---

## Code Block 3: Constructor Method (__init__)

**Try this code:**

```python
class Student:
    """Represents a student."""
    
    def __init__(self, name, gpa):
        self.name = name
        self.gpa = gpa
    
    def get_info(self):
        return f"{self.name} has a GPA of {self.gpa}"

# Create students
alice = Student("Alice", 3.8)
bob = Student("Bob", 3.5)

print(alice.get_info())
print(bob.get_info())
```

**Question 5:** What does this code print?
- A) `Student has a GPA of None` then `Student has a GPA of None`
- B) `Alice has a GPA of 3.8` then `Bob has a GPA of 3.5`
- C) `name` then `gpa` for each
- D) Error

**Question 6:** What happens if you add `print("Creating student")` inside the `__init__` method and then create a new `Student` object?
- A) "Creating student" prints each time a new Student is created
- B) The message prints only once, when the class is defined
- C) The message does not print at all
- D) You get an error

---

## Code Block 4: Multiple Objects from One Class

**Try this code:**

```python
class Book:
    """Represents a book."""
    
    def __init__(self, title, author):
        self.title = title
        self.author = author
        self.is_borrowed = False
    
    def borrow(self):
        if not self.is_borrowed:
            self.is_borrowed = True
            return True
        return False
    
    def get_status(self):
        status = "borrowed" if self.is_borrowed else "available"
        return f"{self.title} by {self.author} - {status}"

# Create multiple books
book1 = Book("Python Programming", "John Smith")
book2 = Book("Data Science", "Jane Doe")

print(book1.get_status())
print(book2.get_status())
```

**Question 7:** What does this code print?
- A) Both books show as "borrowed"
- B) `Python Programming by John Smith - available` then `Data Science by Jane Doe - available`
- C) Both print the same message
- D) Error

**Question 8:** Call `book1.borrow()` twice in a row and print the result each time. What are the two return values?
- A) `True` then `True`
- B) `True` then `False`
- C) `False` then `False`
- D) `False` then `True`

---

## Code Block 5: Object Interaction

**Try this code:**

```python
class Point:
    """Represents a point in 2D space."""
    
    def __init__(self, x, y):
        self.x = x
        self.y = y
    
    def distance_to(self, other):
        dx = self.x - other.x
        dy = self.y - other.y
        return (dx**2 + dy**2)**0.5
    
    def move(self, dx, dy):
        self.x += dx
        self.y += dy

# Create and use points
p1 = Point(0, 0)
p2 = Point(3, 4)

distance = p1.distance_to(p2)
print(distance)

p1.move(1, 1)
print(f"P1 is now at ({p1.x}, {p1.y})")
```

**Question 9:** What does this code print (approximately)?
- A) `5.0` then `P1 is now at (1, 1)`
- B) `7.0` then `P1 is now at (0, 0)`
- C) `25.0` then `P1 is now at (3, 4)`
- D) Error

**Question 10:** Create a third point `p3 = Point(0, 0)`, then call `print(p1.distance_to(p3))` after moving p1 twice with `p1.move(1, 1)`. What is the distance?
- A) `0.0`
- B) `2.0` (approximately)
- C) `4.0` (approximately)
- D) Error

---

## Code Block 6: Encapsulation

**Try this code:**

```python
class BankAccount:
    """A simple bank account."""
    
    def __init__(self, initial_balance=0):
        self._balance = initial_balance  # Protected attribute
    
    def get_balance(self):
        return self._balance
    
    def deposit(self, amount):
        if amount > 0:
            self._balance += amount
            return True
        return False
    
    def withdraw(self, amount):
        if amount > 0 and amount <= self._balance:
            self._balance -= amount
            return True
        return False

# Use the account
account = BankAccount(1000)
account.deposit(500)
print(f"Balance: ${account.get_balance()}")
```

**Question 11:** What does this code print?
- A) `Balance: $0`
- B) `Balance: $1500`
- C) `Balance: $1000`
- D) `Balance: $500`

**Question 12:** Try to access `account._balance` directly by adding `print(account._balance)` after creating the account. Does it work?
- A) No, it's private and can't be accessed
- B) Yes, it prints the balance value
- C) Yes, but only from within the class
- D) Error because balance doesn't exist

---

## Code Block 7: Inheritance Basics

**Try this code:**

```python
class Animal:
    """Base class for animals."""
    
    def __init__(self, name):
        self.name = name
    
    def speak(self):
        return "Some sound"
    
    def get_info(self):
        return f"Name: {self.name}"

class Dog(Animal):
    """Dog class inherits from Animal."""
    
    def speak(self):
        return "Woof!"

class Cat(Animal):
    """Cat class inherits from Animal."""
    
    def speak(self):
        return "Meow!"

# Use the classes
dog = Dog("Buddy")
cat = Cat("Whiskers")

print(dog.speak())
print(cat.speak())
print(dog.get_info())
```

**Question 13:** What does this code print?
- A) `Woof!` then `Meow!` then `Name: Buddy`
- B) `Some sound` then `Some sound` then `Name: Buddy`
- C) `Dog` then `Cat` then `Animal`
- D) Error

**Question 14:** Suppose you override the `speak` method in both the `Dog` and `Cat` classes. What happens if you remove the `speak` method from the `Cat` class and then call `cat.speak()`?
- A) It uses the `speak` method from the `Animal` class and prints "Some sound"
- B) You get an error because `Cat` must have its own `speak` method
- C) It prints nothing
- D) It prints "Meow!" from the non-existent method


---

## Code Block 8: Using isinstance()

**Try this code:**

```python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    pass

class Cat(Animal):
    pass

dog = Dog("Buddy")
animal = Animal("Generic")

print(isinstance(dog, Dog))
print(isinstance(dog, Animal))
print(isinstance(animal, Dog))
print(isinstance(dog, Cat))
```

**Question 15:** What does this code print?
- A) `True` then `True` then `False` then `False`
- B) `False` then `False` then `True` then `True`
- C) `True` then `False` then `True` then `False`
- D) Error

**Question 16:** Which of the following would return `True`?
- A) `isinstance(dog, Animal)`
- B) `isinstance(animal, Dog)`
- C) `isinstance(dog, Cat)`
- D) `isinstance(animal, Cat)`


---

## Code Block 9: Method Overriding

**Try this code:**

```python
class Shape:
    """Base class for shapes."""
    
    def area(self):
        return 0
    
    def perimeter(self):
        return 0

class Rectangle(Shape):
    """Rectangle class inherits from Shape."""
    
    def __init__(self, width, height):
        self.width = width
        self.height = height
    
    def area(self):
        return self.width * self.height
    
    def perimeter(self):
        return 2 * (self.width + self.height)

class Circle(Shape):
    """Circle class inherits from Shape."""
    
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14159 * self.radius ** 2

# Use the classes
rect = Rectangle(5, 3)
circ = Circle(4)

print(f"Rectangle area: {rect.area()}")
print(f"Circle area: {circ.area()}")
```

**Question 17:** What does this code print?
- A) `Rectangle area: 0` then `Circle area: 0`
- B) `Rectangle area: 15` then `Circle area: 50.265`
- C) `Rectangle area: 16` then `Circle area: 12.566`
- D) Error

**Question 18:** Remove the `area()` method from the `Circle` class and run the code. What happens?
- A) Error because `circ.area()` is called
- B) It prints `Circle area: 0` (uses parent method)
- C) It prints `Circle area: 0` but different behavior
- D) Nothing changes in the output

---

## Code Block 10: Practical Example

**Try this code:**

```python
class BankAccount:
    """A bank account with basic operations."""
    
    def __init__(self, owner, balance=0):
        self.owner = owner
        self._balance = balance
    
    def deposit(self, amount):
        if amount > 0:
            self._balance += amount
            return True
        return False
    
    def withdraw(self, amount):
        if 0 < amount <= self._balance:
            self._balance -= amount
            return True
        return False
    
    def get_balance(self):
        return self._balance
    
    def get_info(self):
        return f"{self.owner}: ${self._balance}"

class SavingsAccount(BankAccount):
    """Savings account with interest."""
    
    def __init__(self, owner, balance=0, interest_rate=0.02):
        super().__init__(owner, balance)
        self.interest_rate = interest_rate
    
    def add_interest(self):
        interest = self._balance * self.interest_rate
        self._balance += interest
        return interest

# Use the classes
account = BankAccount("Alice", 1000)
savings = SavingsAccount("Bob", 500, 0.03)

print(account.get_info())
print(savings.get_info())

account.deposit(200)
savings.add_interest()

print(f"After deposits: Alice has ${account.get_balance()}")
print(f"After interest: Bob has ${savings.get_balance()}")
```

**Question 19:** What does this code print (approximately)?
- A) `Alice: $1000` then `Bob: $500` then `After deposits: Alice has $1200` then `After interest: Bob has $515`
- B) `Alice: $1200` then `Bob: $515` then both messages show errors
- C) `Bank Account` then `Savings Account` then two zeros
- D) Error

**Question 20:** Remove the `super().__init__(owner, balance)` line from `SavingsAccount` and run the code. What happens when you try to create a savings account?
- A) Error because owner and balance aren't set
- B) Works fine, variables are set automatically
- C) Account is created but owner is None
- D) Error because interest_rate isn't set

