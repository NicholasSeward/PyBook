> NOTE: Adapted from [*Think Python*, 3rd edition](https://allendowney.github.io/ThinkPython/) by Allen B. Downey, [Chapter 9: Lists](https://github.com/AllenDowney/ThinkPython/blob/v3/chapters/chap09.ipynb). Provided here for convenience.

# Lists

This chapter presents one of Python's most useful built-in types, lists.
You will also learn more about objects and what can happen when multiple variables refer to the same object.

In the exercises at the end of the chapter, we'll make a word list and use it to search for special words like palindromes and anagrams.

## A list is a sequence

Like a string, a **list** is a sequence of values. In a string, the
values are characters; in a list, they can be any type.
The values in a list are called **elements**.

There are several ways to create a new list; the simplest is to enclose the elements in square brackets (`[` and `]`).
For example, here is a list of two integers.

```py
numbers = [42, 123]
```

And here's a list of three strings.

```py
cheeses = ['Cheddar', 'Edam', 'Gouda']
```

The elements of a list don't have to be the same type.
The following list contains a string, a float, an integer, and even another list.

```py
t = ['spam', 2.0, 5, [10, 20]]
```

A list within another list is **nested**.

A list that contains no elements is called an empty list; you can create
one with empty brackets, `[]`.

```py
empty = []
```

The `len` function returns the length of a list.

```py
cheeses = ['Cheddar', 'Edam', 'Gouda']
print(len(cheeses))
```

The length of an empty list is `0`.

```py
empty = []
print(len(empty))
```

The following figure shows the state diagram for `cheeses`, `numbers` and `empty`.

Lists are represented by boxes with the word "list" outside and the numbered elements of the list inside.

## Lists are mutable

To read an element of a list, we can use the bracket operator.
The index of the first element is `0`.

```py
cheeses = ['Cheddar', 'Edam', 'Gouda']
print(cheeses[0])
```

Unlike strings, lists are mutable. When the bracket operator appears on
the left side of an assignment, it identifies the element of the list
that will be assigned.

```py
numbers = [42, 123]
numbers[1] = 17
print(numbers)
```

The second element of `numbers`, which used to be `123`, is now `17`.

List indices work the same way as string indices:

-   Any integer expression can be used as an index.

-   If you try to read or write an element that does not exist, you get
    an `IndexError`.

-   If an index has a negative value, it counts backward from the end of
    the list.

The `in` operator works on lists -- it checks whether a given element appears anywhere in the list.

```py
cheeses = ['Cheddar', 'Edam', 'Gouda']
print('Edam' in cheeses)
```

```py
cheeses = ['Cheddar', 'Edam', 'Gouda']
print('Wensleydale' in cheeses)
```

Although a list can contain another list, the nested list still counts as a single element -- so in the following list, there are only four elements.

```py
t = ['spam', 2.0, 5, [10, 20]]
print(len(t))
```

And `10` is not considered to be an element of `t` because it is an element of a nested list, not `t`.

```py
t = ['spam', 2.0, 5, [10, 20]]
print(len(t))
print(10 in t)
```

## List slices

The slice operator works on lists the same way it works on strings.
The following example selects the second and third elements from a list of four letters.

```py
letters = ['a', 'b', 'c', 'd']
print(letters[1:3])
```

If you omit the first index, the slice starts at the beginning.

```py
letters = ['a', 'b', 'c', 'd']
print(letters[1:3])
print(letters[:2])
```

If you omit the second, the slice goes to the end.

```py
letters = ['a', 'b', 'c', 'd']
print(letters[1:3])
print(letters[2:])
```

So if you omit both, the slice is a copy of the whole list.

```py
letters = ['a', 'b', 'c', 'd']
print(letters[1:3])
print(letters[:])
```

Another way to copy a list is to use the `list` function.

```py
letters = ['a', 'b', 'c', 'd']
print(letters[1:3])
print(list(letters))
```

Because `list` is the name of a built-in function, you should avoid using it as a variable name.

## List operations

The `+` operator concatenates lists.

```py
t1 = [1, 2]
t2 = [3, 4]
print(t1 + t2)
```

The `*` operator repeats a list a given number of times.

```py
print(['spam'] * 4)
```

No other mathematical operators work with lists, but the built-in function `sum` adds up the elements.

```py
t1 = [1, 2]
t2 = [3, 4]
print(t1 + t2)
print(sum(t1))
```

And `min` and `max` find the smallest and largest elements.

```py
t1 = [1, 2]
t2 = [3, 4]
print(t1 + t2)
print(min(t1))
```

```py
t1 = [1, 2]
t2 = [3, 4]
print(t1 + t2)
print(max(t2))
```

## List methods

Python provides methods that operate on lists. For example, `append`
adds a new element to the end of a list:

```py
letters = ['a', 'b', 'c', 'd']
print(letters[1:3])
print(letters.append('e'))
print(letters)
```

`extend` takes a list as an argument and appends all of the elements:

```py
letters = ['a', 'b', 'c', 'd']
print(letters[1:3])
print(letters.extend(['f', 'g']))
print(letters)
```

There are two methods that remove elements from a list.
If you know the index of the element you want, you can use `pop`.

```py
t = ['a', 'b', 'c']
print(t.pop(1))
```

The return value is the element that was removed.
And we can confirm that the list has been modified.

```py
t = ['a', 'b', 'c']
print(t.pop(1))
print(t)
```

If you know the element you want to remove (but not the index), you can use `remove`:

```py
t = ['a', 'b', 'c']
print(t.remove('b'))
```

The return value from `remove` is `None`.
But we can confirm that the list has been modified.

```py
t = ['a', 'b', 'c']
print(t.remove('b'))
print(t)
```

If the element you ask for is not in the list, that's a ValueError.

```
# This raises ValueError
t.remove('d')
```

## Lists and strings

A string is a sequence of characters and a list is a sequence of values,
but a list of characters is not the same as a string. 
To convert from a string to a list of characters, you can use the `list` function.

```py
s = 'spam'
t = list(s)
print(t)
```

The `list` function breaks a string into individual letters.
If you want to break a string into words, you can use the `split` method:

```py
s = 'pining for the fjords'
t = s.split()
print(t)
```

An optional argument called a **delimiter** specifies which characters to use as word boundaries. The following example uses a hyphen as a delimiter.

```py
s = 'ex-parrot'
t = s.split('-')
print(t)
```

If you have a list of strings, you can concatenate them into a single string using `join`.
`join` is a string method, so you have to invoke it on the delimiter and pass the list as an argument.

```py
delimiter = ' '
t = ['pining', 'for', 'the', 'fjords']
s = delimiter.join(t)
print(s)
```

In this case the delimiter is a space character, so `join` puts a space
between words.
To join strings without spaces, you can use the empty string, `''`, as a delimiter.

## Looping through a list

You can use a `for` statement to loop through the elements of a list.

```py
cheeses = ['Cheddar', 'Edam', 'Gouda']

for cheese in cheeses:
    print(cheese)
```

For example, after using `split` to make a list of words, we can use `for` to loop through them.

```py
s = 'pining for the fjords'

for word in s.split():
    print(word)
```

A `for` loop over an empty list never runs the indented statements.

```py
for x in []:
    print('This never happens.')
```

## Sorting lists

Python provides a built-in function called `sorted` that sorts the elements of a list.

```py
scramble = ['c', 'a', 'b']
print(sorted(scramble))
```

The original list is unchanged.

```py
scramble = ['c', 'a', 'b']
print(sorted(scramble))
print(scramble)
```

`sorted` works with any kind of sequence, not just lists. So we can sort the letters in a string like this.

```py
print(sorted('letters'))
```

The result is a list.
To convert the list to a string, we can use `join`.

```py
print(''.join(sorted('letters')))
```

With an empty string as the delimiter, the elements of the list are joined with nothing between them.

## Objects and values

If we run these assignment statements:

```py
a = 'banana'
b = 'banana'
```

We know that `a` and `b` both refer to a string, but we don't know whether they refer to the *same* string. 
There are two possible states, shown in the following figure.

In the diagram on the left, `a` and `b` refer to two different objects that have the
same value. In the diagram on the right, they refer to the same object.
To check whether two variables refer to the same object, you can use the `is` operator.

```py
a = 'banana'
b = 'banana'
print(a is b)
```

In this example, Python only created one string object, and both `a`
and `b` refer to it.
But when you create two lists, you get two objects.

```py
a = [1, 2, 3]
b = [1, 2, 3]
print(a is b)
```

So the state diagram looks like this.

```py
t = [1, 2, 3]
binding1 = Binding(Value('a'), Value(repr(t)))
binding2 = Binding(Value('b'), Value(repr(t)))
frame = Frame([binding1, binding2], dy=-0.25)
```

In this case we would say that the two lists are **equivalent**, because they have the same elements, but not **identical**, because they are not the same object. 
If two objects are identical, they are also equivalent, but if they are equivalent, they are not necessarily identical.

## Aliasing

If `a` refers to an object and you assign `b = a`, then both variables refer to the same object.

```py
a = [1, 2, 3]
b = a
print(b is a)
```

So the state diagram looks like this.

```py
t = [1, 2, 3]
binding1 = Binding(Value('a'), Value(repr(t)), dy=-0.11)
binding2 = Binding(Value('b'), draw_value=False, dy=0.11)
frame = Frame([binding1, binding2], dy=-0.25)
```

The association of a variable with an object is called a **reference**.
In this example, there are two references to the same object.

An object with more than one reference has more than one name, so we say the object is **aliased**.
If the aliased object is mutable, changes made with one name affect the other.
In this example, if we change the object `b` refers to, we are also changing the object `a` refers to.

```py
a = [1, 2, 3]
b = a
print(b is a)
a = [1, 2, 3]
b = a
print(b is a)
b[0] = 5
print(a)
```

So we would say that `a` "sees" this change.
Although this behavior can be useful, it is error-prone.
In general, it is safer to avoid aliasing when you are working with mutable objects.

For immutable objects like strings, aliasing is not as much of a problem.
In this example:

```py
a = 'banana'
b = 'banana'
```

It almost never makes a difference whether `a` and `b` refer to the same
string or not.

## List arguments

When you pass a list to a function, the function gets a reference to the
list. If the function modifies the list, the caller sees the change. For
example, `pop_first` uses the list method `pop` to remove the first element from a list.

```py
def pop_first(lst):
    return lst.pop(0)
```

We can use it like this.

```py
def pop_first(lst):
    return lst.pop(0)
letters = ['a', 'b', 'c']
print(pop_first(letters))
```

The return value is the first element, which has been removed from the list -- as we can see by displaying the modified list.

```py
def pop_first(lst):
    return lst.pop(0)
letters = ['a', 'b', 'c']
print(pop_first(letters))
print(letters)
```

In this example, the parameter `lst` and the variable `letters` are aliases for the same object, so the state diagram looks like this:

```py
lst = make_list('abc', dy=-0.3, offsetx=0.1)
binding1 = Binding(Value('letters'), draw_value=False)
frame1 = Frame([binding1], name='__main__', loc='left')

binding2 = Binding(Value('lst'), draw_value=False, dx=0.61, dy=0.35)
frame2 = Frame([binding2], name='pop_first', loc='left', offsetx=0.08)

stack = Stack([frame1, frame2], dx=-0.3, dy=-0.5)
```

Passing a reference to an object as an argument to a function creates a form of aliasing.
If the function modifies the object, those changes persist after the function is done.

## Making a word list

In the previous chapter, we read the file `words.txt` and searched for words with certain properties, like using the letter `e`.
But we read the entire file many times, which is not efficient.
It is better to read the file once and put the words in a list.
The following loop shows how.

```py
from pathlib import Path
Path('words.txt').write_text('aa\naha\nbib\nbob\ncivic\ndad\neve\ngag\nhanah\nkayak\nlevel\nmom\nnoon\notto\npeep\nradar\nrefer\nrepaper\nrotator\nrotor\nsagas\nsolos\nstats\ntenet\nwow\n')
word_list = []
for line in open('words.txt'):
    word = line.strip()
    word_list.append(word)
print(len(word_list))
```

Before the loop, `word_list` is initialized with an empty list.
Each time through the loop, the `append` method adds a word to the end.
When the loop is done, there are more than 113,000 words in the list.

Another way to do the same thing is to use `read` to read the entire file into a string.

```py
from pathlib import Path
Path('words.txt').write_text('aa\naha\nbib\nbob\ncivic\ndad\neve\ngag\nhanah\nkayak\nlevel\nmom\nnoon\notto\npeep\nradar\nrefer\nrepaper\nrotator\nrotor\nsagas\nsolos\nstats\ntenet\nwow\n')
string = open('words.txt').read()
print(len(string))
```

The result is a single string with more than a million characters.
We can use the `split` method to split it into a list of words.

```py
from pathlib import Path
Path('words.txt').write_text('aa\naha\nbib\nbob\ncivic\ndad\neve\ngag\nhanah\nkayak\nlevel\nmom\nnoon\notto\npeep\nradar\nrefer\nrepaper\nrotator\nrotor\nsagas\nsolos\nstats\ntenet\nwow\n')
string = open('words.txt').read()
print(len(string))
word_list = string.split()
print(len(word_list))
```

Now, to check whether a string appears in the list, we can use the `in` operator.
For example, `'demotic'` is in the list.

```py
from pathlib import Path
Path('words.txt').write_text('aa\naha\nbib\nbob\ncivic\ndad\neve\ngag\nhanah\nkayak\nlevel\nmom\nnoon\notto\npeep\nradar\nrefer\nrepaper\nrotator\nrotor\nsagas\nsolos\nstats\ntenet\nwow\n')
string = open('words.txt').read()
print(len(string))
word_list = string.split()
print(len(word_list))
print('demotic' in word_list)
```

But `'contrafibularities'` is not.

```py
from pathlib import Path
Path('words.txt').write_text('aa\naha\nbib\nbob\ncivic\ndad\neve\ngag\nhanah\nkayak\nlevel\nmom\nnoon\notto\npeep\nradar\nrefer\nrepaper\nrotator\nrotor\nsagas\nsolos\nstats\ntenet\nwow\n')
string = open('words.txt').read()
print(len(string))
word_list = string.split()
print(len(word_list))
print('contrafibularities' in word_list)
```

And I have to say, I'm anaspeptic about it.

## Debugging

Note that most list methods modify the argument and return `None`.
This is the opposite of the string methods, which return a new string and leave the original alone.

If you are used to writing string code like this:

```py
word = 'plumage!'
word = word.strip('!')
print(word)
```

It is tempting to write list code like this:

```py
t = [1, 2, 3]
t = t.remove(3)           # WRONG!
```

`remove` modifies the list and returns `None`, so next operation you perform with `t` is likely to fail.

```
# This raises AttributeError
t.remove(2)
```

This error message takes some explaining.
An **attribute** of an object is a variable or method associated with it.
In this case, the value of `t` is `None`, which is a `NoneType` object, which does not have a attribute named `remove`, so the result is an `AttributeError`.

If you see an error message like this, you should look backward through the program and see if you might have called a list method incorrectly.

## Glossary

**list:**
 An object that contains a sequence of values.

**element:**
 One of the values in a list or other sequence.

**nested list:**
A list that is an element of another list.

**delimiter:**
 A character or string used to indicate where a string should be split.

**equivalent:**
 Having the same value.

**identical:**
 Being the same object (which implies equivalence).

**reference:**
 The association between a variable and its value.

**aliased:**
If there is more than one variable that refers to an object, the object is aliased.

**attribute:**
 One of the named values associated with an object.

## Exercises

```py
# This cell tells Jupyter to provide detailed debugging information
# when a runtime error occurs. Run it before working on the exercises.
```

### Ask a virtual assistant

In this chapter, I used the words "contrafibularities" and "anaspeptic", but they are not actually English words.
They were used in the British television show *Black Adder*, Season 3, Episode 2, "Ink and Incapability".

However, when I asked ChatGPT 3.5 (August 3, 2023 version) where those words came from, it initially claimed they are from Monty Python, and later claimed they are from the Tom Stoppard play *Rosencrantz and Guildenstern Are Dead*.

If you ask now, you might get different results.
But this example is a reminder that virtual assistants are not always accurate, so you should check whether the results are correct.
As you gain experience, you will get a sense of which questions virtual assistants can answer reliably.
In this example, a conventional web search can identify the source of these words quickly.

If you get stuck on any of the exercises in this chapter, consider asking a virtual assistant for help.
If you get a result that uses features we haven't learned yet, you can assign the VA a "role".

For example, before you ask a question try typing "Role: Basic Python Programming Instructor".
After that, the responses you get should use only basic features.
If you still see features we you haven't learned, you can follow up with "Can you write that using only basic Python features?"

### Exercise

Two words are anagrams if you can rearrange the letters from one to spell the other.
For example, `tops` is an anagram of `stop`.

One way to check whether two words are anagrams is to sort the letters in both words.
If the lists of sorted letters are the same, the words are anagrams.

Write a function called `is_anagram` that takes two strings and returns `True` if they are anagrams.

To get you started, here's an outline of the function with doctests.

```py
def is_anagram(word1, word2):
    """Checks whether two words are anagrams.
    
    >>> is_anagram('tops', 'stop')
    True
    >>> is_anagram('skate', 'takes')
    True
    >>> is_anagram('tops', 'takes')
    False
    >>> is_anagram('skate', 'stop')
    False
    """
    return None
```

```py
# Solution goes here
```

You can use `doctest` to test your function.

```py
def is_anagram(word1, word2):
    """Checks whether two words are anagrams.
    
    >>> is_anagram('tops', 'stop')
    True
    >>> is_anagram('skate', 'takes')
    True
    >>> is_anagram('tops', 'takes')
    False
    >>> is_anagram('skate', 'stop')
    False
    """
    return None
from doctest import run_docstring_examples

def run_doctests(func):
    run_docstring_examples(func, globals(), name=func.__name__)
print(run_doctests(is_anagram))
```

Using your function and the word list, find all the anagrams of `takes`.

```py
# Solution goes here
```

### Exercise

Python provides a built-in function called `reversed` that takes as an argument a sequence of elements -- like a list or string -- and returns a `reversed` object that contains the elements in reverse order.

```py
print(reversed('parrot'))
```

If you want the reversed elements in a list, you can use the `list` function.

```py
print(list(reversed('parrot')))
```

Or if you want them in a string, you can use the `join` method.

```py
print(''.join(reversed('parrot')))
```

So we can write a function that reverses a word like this.

```py
def reverse_word(word):
    return ''.join(reversed(word))
```

A palindrome is a word that is spelled the same backward and forward, like "noon" and "rotator".
Write a function called `is_palindrome` that takes a string argument and returns `True` if it is a palindrome and `False` otherwise.

Here's an outline of the function with doctests you can use to check your function.

```py
def is_palindrome(word):
    """Check if a word is a palindrome.
    
    >>> is_palindrome('bob')
    True
    >>> is_palindrome('alice')
    False
    >>> is_palindrome('a')
    True
    >>> is_palindrome('')
    True
    """
    return False
```

```py
# Solution goes here
```

```py
def is_anagram(word1, word2):
    """Checks whether two words are anagrams.
    
    >>> is_anagram('tops', 'stop')
    True
    >>> is_anagram('skate', 'takes')
    True
    >>> is_anagram('tops', 'takes')
    False
    >>> is_anagram('skate', 'stop')
    False
    """
    return None
from doctest import run_docstring_examples

def run_doctests(func):
    run_docstring_examples(func, globals(), name=func.__name__)
print(run_doctests(is_anagram))

def is_palindrome(word):
    """Check if a word is a palindrome.
    
    >>> is_palindrome('bob')
    True
    >>> is_palindrome('alice')
    False
    >>> is_palindrome('a')
    True
    >>> is_palindrome('')
    True
    """
    return False
print(run_doctests(is_palindrome))
```

You can use the following loop to find all of the palindromes in the word list with at least 7 letters.

```py
from pathlib import Path
Path('words.txt').write_text('aa\naha\nbib\nbob\ncivic\ndad\neve\ngag\nhanah\nkayak\nlevel\nmom\nnoon\notto\npeep\nradar\nrefer\nrepaper\nrotator\nrotor\nsagas\nsolos\nstats\ntenet\nwow\n')
string = open('words.txt').read()
print(len(string))
word_list = string.split()
print(len(word_list))

def is_palindrome(word):
    """Check if a word is a palindrome.
    
    >>> is_palindrome('bob')
    True
    >>> is_palindrome('alice')
    False
    >>> is_palindrome('a')
    True
    >>> is_palindrome('')
    True
    """
    return False
for word in word_list:
    if len(word) >= 7 and is_palindrome(word):
        print(word)
```

### Exercise

Write a function called `reverse_sentence` that takes as an argument a string that contains any number of words separated by spaces.
It should return a new string that contains the same words in reverse order.
For example, if the argument is "Reverse this sentence", the result should be "Sentence this reverse".

Hint: You can use the `capitalize` methods to capitalize the first word and convert the other words to lowercase.

To get you started, here's an outline of the function with doctests.

```py
def reverse_sentence(input_string):
    '''Reverse the words in a string and capitalize the first.
    
    >>> reverse_sentence('Reverse this sentence')
    'Sentence this reverse'

    >>> reverse_sentence('Python')
    'Python'

    >>> reverse_sentence('')
    ''

    >>> reverse_sentence('One for all and all for one')
    'One for all and all for one'
    '''
    return None
```

```py
# Solution goes here
```

```py
def is_anagram(word1, word2):
    """Checks whether two words are anagrams.
    
    >>> is_anagram('tops', 'stop')
    True
    >>> is_anagram('skate', 'takes')
    True
    >>> is_anagram('tops', 'takes')
    False
    >>> is_anagram('skate', 'stop')
    False
    """
    return None
from doctest import run_docstring_examples

def run_doctests(func):
    run_docstring_examples(func, globals(), name=func.__name__)
print(run_doctests(is_anagram))

def reverse_sentence(input_string):
    """Reverse the words in a string and capitalize the first.
    
    >>> reverse_sentence('Reverse this sentence')
    'Sentence this reverse'

    >>> reverse_sentence('Python')
    'Python'

    >>> reverse_sentence('')
    ''

    >>> reverse_sentence('One for all and all for one')
    'One for all and all for one'
    """
    return None
print(run_doctests(reverse_sentence))
```

### Exercise

Write a function called `total_length` that takes a list of strings and returns the total length of the strings.
The total length of the words in `word_list` should be $902{,}728$.

```py
# Solution goes here
```

```py
# Solution goes here
```

[Think Python: 3rd Edition](https://allendowney.github.io/ThinkPython/index.html)

Copyright 2024 [Allen B. Downey](https://allendowney.com)

Code license: [MIT License](https://mit-license.org/)

Text license: [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0/)
