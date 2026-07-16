# Coding Conventions (PEP 8)

## Overview
PEP 8 is Python's official style guide that defines coding conventions for readable, maintainable code.

**Official PEP 8 Documentation**: [https://www.python.org/dev/peps/pep-0008/](https://www.python.org/dev/peps/pep-0008/)

## Why Follow PEP 8?

- **Readability**: Code is easier to read and understand
- **Consistency**: All Python code follows the same style
- **Professionalism**: Industry standard that employers expect
- **Maintainability**: Easier to modify and debug code

## Naming Convention Summary

| Convention | Style | Example | When to Use |
|------------|-------|---------|-------------|
| **snake_case** | lowercase_with_underscores | `user_name`, `calculate_average` | Variables, functions, methods, modules, packages |
| **SCREAMING_SNAKE_CASE** | UPPERCASE_WITH_UNDERSCORES | `MAX_CONNECTIONS`, `PI` | Constants, configuration values |
| **PascalCase** | CapitalizedWords | `UserAccount`, `DatabaseConnection` | Classes, exceptions |
| **camelCase** | camelCase | `userName`, `calculateAverage` | **Avoid in Python** (use snake_case instead) |

## Key PEP 8 Rules

### Naming Conventions

#### Variables and Functions
```python
# Good - lowercase with underscores (snake_case)
user_name = "John"
calculate_average = lambda x: sum(x) / len(x)

# Bad - camelCase or PascalCase/TitleCase
userName = "John"
calculateAverage = lambda x: sum(x) / len(x)
```

#### Constants
```python
# Good - uppercase with underscores (SCREAMING_SNAKE_CASE)
MAX_CONNECTIONS = 100
PI = 3.14159

# Bad - lowercase
max_connections = 100
pi = 3.14159
```

#### Classes
```python
# Good - PascalCase
class UserAccount:
    pass

class DatabaseConnection:
    pass

# Bad - lowercase
class useraccount:
    pass
```

### Spacing and Indentation

#### Indentation
```python
# Good - 4 spaces (not tabs)
def calculate_area(radius):
    area = 3.14159 * radius ** 2
    return area

# Bad - inconsistent indentation
def calculate_area(radius):
  area = 3.14159 * radius ** 2
    return area
```

#### Line Length
```python
# Good - under 79 characters
def long_function_name(
    parameter1, parameter2, parameter3,
    parameter4, parameter5
):
    return parameter1 + parameter2

# Bad - too long
def long_function_name(parameter1, parameter2, parameter3, parameter4, parameter5):
    return parameter1 + parameter2
```

#### Spacing Around Operators
```python
# Good - spaces around operators
x = 5 + 3
y = 10 * 2

# Bad - no spaces
x=5+3
y=10*2
```

### Import Statements

#### Import Order
```python
# Good - standard library first, then third-party
import os
import sys
from datetime import datetime

import numpy as np
import pandas as pd

# Bad - mixed order
import numpy as np
import os
import pandas as pd
import sys
```

#### Import Style
```python
# Good - one import per line
import os
import sys

# Bad - multiple imports on one line
import os, sys
```

### Function and Class Definitions

#### Spacing
```python
# Good - two blank lines before class, one before function
class MyClass:
    def method1(self):
        pass
    
    def method2(self):
        pass


def my_function():
    pass


def another_function():
    pass
```

## Common Violations to Avoid

### Missing Spaces
```python
# Bad
if x==5:
    print("x is 5")

# Good
if x == 5:
    print("x is 5")
```


### Unused Imports
```python
# Bad - unused import
import os
import sys  # Not used anywhere

# Good - only import what you need
import os
```

## Tools to Help

### Linters
- **Flake8**: Popular PEP 8 checker
- **Pylint**: More comprehensive code analysis
- **Black**: Auto-formatter (opinionated but PEP 8 compliant)

### IDE Integration
- Most modern IDEs (VS Code, PyCharm) show PEP 8 violations
- Can be configured to auto-format on save

## Best Practices

1. **Start Early**: Develop good habits from the beginning
2. **Use Tools**: Let linters catch violations automatically
3. **Be Consistent**: Pick a style and stick with it
4. **Read Code**: Study well-formatted Python code
5. **Practice**: Write code regularly following these conventions

## Remember
PEP 8 is about making code readable for humans, not just functional for computers. Good style makes your code professional and easier to work with.
