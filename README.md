# python
# 🐍 Python Basics – Complete Guide (Up to Functions)

This repository contains **well-structured notes and examples of Python programming**, covering topics from **basic syntax to functions**. It is useful for **beginners, students, and interview preparation**.

---

## 📌 Table of Contents

1. Introduction to Python
2. Python Syntax & Comments
3. Variables & Data Types
4. Type Conversion
5. Operators in Python
6. Input & Output
7. Control Flow Statements

   * if, if-else, elif
   * for loop
   * while loop
   * break, continue, pass
8. Strings
9. Lists
10. Tuples
11. Sets
12. Dictionaries
13. Functions

* Built-in Functions
* User-defined Functions
* Function Arguments
* Return Statement
* Lambda Functions

---

## Introduction to Python

Python is a **high-level, interpreted, object-oriented, and general-purpose programming language**. It is known for its **simple syntax and readability**.

### Features:

* Easy to learn and use
* Interpreted language
* Platform independent
* Large standard library
* Supports multiple paradigms

---

## Python Installation & Setup

* Download Python from the official website
* Install Python and add it to PATH
* Verify installation:

```bash
python --version
```

---

## Python Syntax & Comments

Python uses **indentation** instead of braces `{}`.

### Example:

```python
if True:
    print("Hello Python")
```

### Comments:

```python
# This is a single-line comment
"""This is a
multi-line comment"""
```

---

## Variables & Data Types

Variables store data values.

```python
x = 10
y = "Python"
z = 5.5
```

### Common Data Types:

* int
* float
* complex
* str
* list
* tuple
* set
* dict
* bool

---

## Type Conversion

Convert one data type into another.

```python
x = "10"
y = int(x)
```

Types:

* int()
* float()
* str()
* list()
* tuple()
* set()

---

## Operators in Python

### Arithmetic Operators

`+  -  *  /  %  **  //`

### Relational Operators

`==  !=  >  <  >=  <=`

### Logical Operators

`and  or  not`

### Assignment Operators

`=  +=  -=  *=`

### Membership Operators

`in  not in`

## Input & Output

```python
name = input("Enter your name: ")
print("Hello", name)
```

## Control Flow Statements (Decision Making & Loops)

Control flow statements control the **execution flow** of a program based on conditions or repetitions.

---

### 🔹 if Statement

Used to execute a block of code when a condition is true.

```python
x = 10
if x > 5:
    print("x is greater than 5")
```

---

### 🔹 if-else Statement

Executes one block if condition is true, otherwise another block.

```python
x = 3
if x % 2 == 0:
    print("Even number")
else:
    print("Odd number")
```

---

### 🔹 if-elif-else Statement

Used when multiple conditions are involved.

```python
marks = 85
if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
elif marks >= 60:
    print("Grade C")
else:
    print("Fail")
```

## 🔁 Loops in Python

Loops are used to **repeat a block of code multiple times**.


### 🔹 for Loop

Used to iterate over a sequence (list, tuple, string, range).

```python
for i in range(1, 6):
    print(i)
```

#### for loop with list

```python
fruits = ["apple", "banana", "cherry"]
for item in fruits:
    print(item)
```

### 🔹 while Loop

Executes a block as long as the condition is true.

```python
i = 1
while i <= 5:
    print(i)
    i += 1
```

### 🔹 Nested Loops

A loop inside another loop.

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(i, j)
```

### 🔹 Loop Control Statements

#### break

Terminates the loop completely.

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

#### continue

Skips the current iteration.

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

#### pass

Used as a placeholder.

```python
for i in range(3):
    pass
```

---

### 🔹 else with Loops

Executed when the loop finishes normally.

```python
for i in range(3):
    print(i)
else:
    print("Loop completed")
```

---

## Strings

Strings are sequences of characters.

```python
s = "Python"
print(s[0])
print(s.upper())
```

### String Operations:

* Indexing
* Slicing
* Concatenation
* Methods (`lower()`, `replace()`, `split()`)

---

## Lists

Lists are **mutable and ordered**.

```python
list1 = [1, 2, 3, 4]
list1.append(5)
```

Common Methods:

* append()
* insert()
* remove()
* pop()
* sort()

## Tuples

Tuples are **immutable and ordered**.

```python
t = (10, 20, 30)
```

---

##  Sets

Sets are **unordered and unique**.

```python
s = {1, 2, 3}
s.add(4)
```

---

## Dictionaries

Dictionaries store data as **key-value pairs**.

```python
d = {"name": "Alex", "age": 25}
print(d["name"])
```

Methods:

* keys()
* values()
* items()
* get()
* update()

## Functions
 Functions
A function is a reusable block of code that performs a specific task.

Advantages:
- Avoids repetition
- Improves readability
- Easy to maintain

Example:
def add(a, b):
    return a + b

### User-defined Function

```python
def add(a, b):
    return a + b

print(add(10, 20))
```

### Types of Arguments

* Positional
* Keyword
* Default
* Variable-length (`*args`, `**kwargs`)
## Modularization

Modularization means dividing a large program into smaller files called modules.

Benefits:
- Better code organization
- Easy debugging
- Code reuse
Example:
# module.py
def greet():
    print("Hello")

# main.py
import module
module.greet()

### Lambda Function

```python
square = lambda x: x * x
print(squauare(5)

## map()

map() applies a function to each element of an iterable.

Example:
nums = [1, 2, 3]
result = list(map(lambda x: x * 2, nums))

## filter()

filter() selects elements that satisfy a condition.

Example:
nums = [1, 2, 3, 4]
result = list(filter(lambda x: x % 2 == 0, nums))

## reduce()

reduce() reduces an iterable to a single value.
It is available in functools module.

Example:
from functools import reduce
nums = [1, 2, 3, 4]
result = reduce(lambda a, b: a + b, nums)

## map with filter

First filters elements, then applies map.

Example:
nums = [1, 2, 3, 4]
result = list(map(lambda x: x * x, filter(lambda x: x % 2 == 0, nums)))

## filter with map

First applies map, then filters the result.

Example:
nums = [1, 2, 3, 4]
result = list(filter(lambda x: x > 5, map(lambda x: x * 2, nums)))

## reduce with map

First applies map, then reduces the result.

Example:
from functools import reduce
nums = [1, 2, 3]
result = reduce(lambda a, b: a + b, map(lambda x: x * 2, nums))

## File Handling

File handling is used to store and retrieve data from files.

Syntax:
file = open("data.txt", "r")
content = file.read()
file.close()

## File Modes

r  → read  
w  → write  
a  → append  
x  → create  
rb → read binary  
wb → write binary  

## File Handling Rules

- Always close the file
- Use correct file mode
- Prefer using with statement

Example:
with open("data.txt", "w") as file:
    file.write("Hello")


## dump(), dumps(), load(), loads()

Used for serialization (saving and loading Python objects).

dump()   → writes object to file  
load()   → reads object from file  
dumps()  → converts object to byte string  
loads()  → converts byte string to object  

Example:
import pickle
pickle.dump(data, file)
data = pickle.load(file)
#dump()

* Writes serialized data **directly to a file**
* Used when storing data permanently

Example:

```python
import pickle
with open("data.pkl", "wb") as f:
    pickle.dump(my_list, f)
dumps()

* Converts data into a **bytes object**
* Does not write to a file

Example:

```python
serialized_data = pickle.dumps(my_dict)

# load()

* Reads serialized data **from a file**
* Converts it back to original form

Example:

with open("data.pkl", "rb") as f:
    data = pickle.load(f)

#loads()

* Converts serialized **bytes data** back to original data

Example:
``python
data = pickle.loads(serialized_data)

## Compression
ompressionis the process of reducing the size of data so it takes less storage space and can be transferred faster. In Python, compression is often used along with serialization, where data structures are converted into a format that can be saved to a file or sent over a network.

🔹 Lists in Compression

Compression reduces file size and saves storage.

Common modules:
- gzip
- zipfile
- zlib

Example:
import gzip


## List Comprehension

A concise way to create lists.

Example:
squares = [x * x for x in range(5)]

With condition:
evens = [x for x in range(10) if x % 2 == 0]

## Dictionary Comprehension
A concise way to create dictionaries.

Example:
squares = {x: x * x for x in range(5)}

With condition:
even_squares = {x: x * x for x in range(10) if x % 2 == 0}

##Summary

- Functions improve reusability
- Modularization improves structure
- map, filter, reduce simplify data processing
- File handling manages data storage
- dump and load store Python objects
- Compression reduces file size
- Comprehensions make code short and readable

##  Contact
kottamula priyanka
email:priyankakottamula@gmail.com
phno:6303145006








