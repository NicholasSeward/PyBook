# Activity 2: Inheritance Family Tree

**Module:** 09 - Classes  
**Time:** 25 minutes  
**Group size:** Pairs  
**Materials:** Laptops

## Goal

Extend a base class with a subclass that reuses and overrides behavior, then demo the family of objects.

## Starter base (provided)

```py
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return "..."
```

## Build (12 min)

Pairs create two subclasses (for example `Dog`, `Cat`) that override `speak` and optionally add one new method.

## Zoo demo (8 min)

Pairs swap machines with neighbors and run:

```py
zoo = [Dog("Rex"), Cat("Miso")]
for animal in zoo:
    print(animal.name, animal.speak())
```

Can another pair use your classes without reading every line?

## Share-out (5 min)

What belongs on the base class vs only on a child?

## Instructor notes

- Keep it light; this is intuition for inheritance, not a full OOP course.
- Optional stretch: override `__str__`.
