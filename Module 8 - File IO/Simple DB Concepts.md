# SQLite Basics

## What is a Database?

A database is a way to store data permanently (persistence). Unlike variables that disappear when your program ends, databases keep your data safe on disk.

**Persistence** means your data survives:
- Closing the program
- Restarting the computer
- Multiple program runs

## What is SQLite?

SQLite is a simple database built into Python. It's like a spreadsheet that:
- Stores data in tables
- Keeps data organized
- Works without installing anything extra

## Simple CRUD Examples

### Create - Add Data
```python
import sqlite3

# Connect to database (creates it if it doesn't exist)
conn = sqlite3.connect('students.db')
cursor = conn.cursor()

# Create table
cursor.execute('''
    CREATE TABLE IF NOT EXISTS students (
        name TEXT,
        age INTEGER,
        grade TEXT
    )
''')

# Add a student
cursor.execute('INSERT INTO students VALUES (?, ?, ?)', ('Alice', 20, 'A'))
conn.commit()
conn.close()
```

### Read - Get Data
```python
import sqlite3

conn = sqlite3.connect('students.db')
cursor = conn.cursor()

# Get all students
cursor.execute('SELECT * FROM students')
students = cursor.fetchall()

for student in students:
    print(f"Name: {student[0]}, Age: {student[1]}, Grade: {student[2]}")

conn.close()
```

### Update - Change Data
```python
import sqlite3

conn = sqlite3.connect('students.db')
cursor = conn.cursor()

# Change Alice's grade to A+
cursor.execute('UPDATE students SET grade = ? WHERE name = ?', ('A+', 'Alice'))
conn.commit()
conn.close()
```

### Delete - Remove Data
```python
import sqlite3

conn = sqlite3.connect('students.db')
cursor = conn.cursor()

# Remove Alice
cursor.execute('DELETE FROM students WHERE name = ?', ('Alice',))
conn.commit()
conn.close()
```

## Key Points

- **SQLite** - simple database built into Python
- **Persistence** - data stays after program ends
- **CRUD** - Create, Read, Update, Delete
- **Always commit** - save your changes
- **Always close** - free up resources

## Summary

✅ **Database** - stores data permanently  
✅ **SQLite** - simple, built-in database  
✅ **CRUD** - basic database operations  
✅ **Commit** - save your changes  
✅ **Close** - clean up connections
