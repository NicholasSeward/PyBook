# Quiz (Module 9 - Classes)

## Multiple Choice Questions (10 questions)

1. What is the purpose of the `__init__` method in a Python class?
   a) To destroy objects
   b) To initialize the attributes of a new object
   c) To print the object
   d) To compare objects

2. What is the difference between a class and an instance?
   a) A class is a template, an instance is a specific object created from that template
   b) A class is an object, an instance is a method
   c) A class is a variable, an instance is a function
   d) There is no difference

3. What is the purpose of the `self` parameter in a method?
   a) It refers to the class itself
   b) It refers to the specific instance of the class
   c) It refers to the parent class
   d) It refers to the module

4. What is the output of the following code?
   ```python
   class Dog:
       def __init__(self, name):
           self.name = name
   
   dog1 = Dog("Buddy")
   print(dog1.name)
   ```
   a) `Dog`
   b) `Buddy`
   c) `self.name`
   d) Error

5. What is the purpose of inheritance in object-oriented programming?
   a) To create multiple copies of the same class
   b) To reuse code from a parent class in a child class
   c) To make classes private
   d) To delete classes

6. What is the output of `isinstance(dog1, Dog)`?
   a) `True`
   b) `False`
   c) `None`
   d) Error

7. What is the purpose of the `super()` function?
   a) To call methods from the parent class
   b) To create a new instance
   c) To delete an instance
   d) To print an object

8. What is the output of the following code?
   ```python
   class Animal:
       def speak(self):
           return "Some sound"
   
   class Cat(Animal):
       def speak(self):
           return "Meow"
   
   cat = Cat()
   print(cat.speak())
   ```
   a) `"Some sound"`
   b) `"Meow"`
   c) `"Cat"`
   d) Error

9. What is the purpose of encapsulation?
   a) To hide data and methods from outside access
   b) To make classes public
   c) To create multiple inheritance
   d) To delete objects

10. What is the output of `type(dog1)`?
    a) `<class 'Dog'>`
    b) `<class 'object'>`
    c) `<class 'instance'>`
    d) Error

## Matching Questions (2 questions)

**Question 11:** Match each OOP concept with its description.

| Concept | Description |
|---------|-------------|
| A) Class | 1) A specific object created from a class |
| B) Instance | 2) A blueprint for creating objects |
| C) Method | 3) A function defined within a class |
| D) Attribute | 4) A variable that belongs to an object |

**Question 12:** Match each special method with its purpose.

| Method | Purpose |
|--------|---------|
| A) `__init__` | 1) String representation of object |
| B) `__str__` | 2) Initialize object attributes |
| C) `__len__` | 3) Get length of object |
| D) `__del__` | 4) Clean up when object is destroyed |

## True/False Questions (3 questions)

13. All methods in a class must have the `self` parameter. (True/False)

14. A child class can access all methods and attributes from its parent class. (True/False)

15. The `__init__` method is automatically called when creating a new instance. (True/False)

## Fill in the Blank Questions (5 questions)

16. The `_____` method is called when creating a new instance of a class.

17. A `_____` is a specific object created from a class template.

18. The `_____` parameter refers to the instance of the class in method definitions.

19. `_____` allows a child class to reuse code from a parent class.

20. The `_____` function checks if an object is an instance of a specific class.
