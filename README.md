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
# Exception Handling in Python
# What is Exception Handling?
Exception Handling is a mechanism to handle runtime errors so that the program does not crash suddenly.

Examples of runtime errors:

Division by zero

File not found

Invalid input

Index out of range

Python provides built-in keywords to handle such errors gracefully.

# Why Exception Handling is Important?
Prevents program crashes

Handles unexpected user input

Improves program reliability

Makes debugging easier

🔹 Keywords Used in Exception Handling
try

except

else

finally

🔹 try and except
🔹 Syntax
try:
    # code that may cause an error
except:
    # code that runs if an error occurs
🔹 Example
try:
    a = int(input("Enter a number: "))
    b = int(input("Enter another number: "))
    print(a / b)
except:
    print("An error occurred")
🔹 Handling Specific Exceptions
try:
    x = int("abc")
except ValueError:
    print("ValueError occurred")
🔹 Multiple except Blocks
try:
    a = int(input())
    b = int(input())
    print(a / b)
except ZeroDivisionError:
    print("Cannot divide by zero")
except ValueError:
    print("Invalid input")
# else Block
The else block executes only when no exception occurs.

try:
    a = 10
    b = 2
    print(a / b)
except ZeroDivisionError:
    print("Error")
else:
    print("Division successful")
# finally Block
The finally block always executes, whether an exception occurs or not.

try:
    f = open("data.txt", "r")
    print(f.read())
except FileNotFoundError:
    print("File not found")
finally:
    print("Execution completed")
* Object-Oriented Programming (OOPS)
# What is OOPS?
OOPS (Object-Oriented Programming System) is a programming approach that uses objects and classes to design applications.
It helps to represent real-world entities in programming.
or
Object Oriented Programming (OOPS)
Object-Oriented Programming (OOPS) is a programming paradigm that organizes software design around objects rather than functions.
It improves code reusability, security, scalability, and maintainability.

# Table of Contents
Class

Object

Constructor

Inheritance

Types of Inheritance

Single Inheritance

Multiple Inheritance

Multilevel Inheritance

Hierarchical Inheritance

Hybrid Inheritance

Abstraction

Encapsulation

 Class
A class is a blueprint or template used to create objects.
It defines properties (variables) and behaviors (methods).

Example (Python)
class Student:
    def study(self):
        print("Student is studying")
 Object
An object is an instance of a class.
It represents a real-world entity and can access class members.

Example
s1 = Student()
s1.study()
# Constructor
A constructor is a special method that is automatically executed when an object is created.
In Python, it is defined using __init__().

Example
class Student:
    def __init__(self, name):
        self.name = name

    def display(self):
        print("Name:", self.name)

s1 = Student("Priyanka")
s1.display()
#Inheritance
Inheritance allows a class to acquire properties and methods of another class.
It helps in code reuse and establishes a parent–child relationship.

* Single Inheritance
One child class inherits from one parent class.

class Parent:
    def show(self):
        print("Parent class")

class Child(Parent):
    pass

c = Child()
c.show()
🔹 Multiple Inheritance
A child class inherits from more than one parent class.

class Father:
    def skill1(self):
        print("Driving")

class Mother:
    def skill2(self):
        print("Cooking")

class Child(Father, Mother):
    pass

c = Child()
c.skill1()
c.skill2()
🔹 Multilevel Inheritance
A class is derived from another derived class.

class Grandparent:
    def gp(self):
        print("Grandparent")

class Parent(Grandparent):
    def p(self):
        print("Parent")

class Child(Parent):
    def c(self):
        print("Child")

obj = Child()
obj.gp()
obj.p()
obj.c()
🔹 Hierarchical Inheritance
Multiple child classes inherit from a single parent class.

class Parent:
    def show(self):
        print("Parent class")

class Child1(Parent):
    pass

class Child2(Parent):
    pass

c1 = Child1()
c2 = Child2()
c1.show()
c2.show()
🔹 Hybrid Inheritance
Hybrid inheritance is a combination of two or more inheritance types.

class A:
    def showA(self):
        print("Class A")

class B(A):
    def showB(self):
        print("Class B")

class C(A):
    def showC(self):
        print("Class C")

class D(B, C):
    pass

d = D()
d.showA()
d.showB()
d.showC()
# Abstraction
Abstraction means hiding implementation details and showing only essential features.
It is achieved using abstract classes.

Example
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass

class Bike(Vehicle):
    def start(self):
        print("Bike started")

b = Bike()
b.start()
# Encapsulation
Encapsulation is wrapping data and methods into a single unit (class).
It protects data using private variables.

Example
class Account:
    def __init__(self):
        self.__balance = 1000  # private variable

    def get_balance(self):
        return self.__balance

acc = Account()
print(acc.get_balance())
# Advantages of OOPS
Code Reusability

Data Security

Easy Maintenance

Real-World Representation

Better Modularity

#Conclusion
OOPS helps developers build structured, scalable, and secure applications.
Understanding class, object, inheritance, abstraction, and encapsulation is essential for software development and interviews.

🧵 Multithreading
Multithreading allows a program to run multiple threads concurrently within a single process.

Key Points
Threads share the same memory space

Best for I/O-bound tasks (file handling, network calls)

Uses threading module

Example
from threading import Thread

def task():
    print("Thread is running")

t = Thread(target=task)
t.start()
⚙️ Multiprocessing
Multiprocessing allows a program to run multiple processes, each with its own memory.

Key Points
Uses multiple CPU cores

Best for CPU-bound tasks

Uses multiprocessing module

Example
from multiprocessing import Process

def task():
    print("Process is running")

p = Process(target=task)
p.start()
🔢 NumPy (Numerical Python)
NumPy is a powerful library for numerical computing and array operations.

Creating Arrays
import numpy as np

a = np.array([1, 2, 3])
Important NumPy Functions
Function	Description
array()	Create array
arange()	Create range of values
ndim	Number of dimensions
shape	Rows & columns
size	Total elements
reshape()	Change shape
zeros()	Array of zeros
ones()	Array of ones
eye()	Identity matrix
diag()	Diagonal elements
ravel()	Convert to 1D
transpose()	Swap rows & columns
concatenate()	Join arrays
full()	Constant-filled array
Reshape Examples
a = np.array([1,2,3,4])

print(a.reshape(1, -1))  # Row vector
print(a.reshape(-1, 1))  # Column vector
Random Functions
np.random.rand(2,2)
np.random.randn(2,2)
np.random.randint(1, 10, size=5)
Mathematical Functions
np.max(a)
np.min(a)
np.sum(a)
np.argmax(a)
np.argmin(a)
np.repeat(a, 2)
Axis Explanation
axis=0 → column-wise

axis=1 → row-wise

np.sum(a, axis=0)
np.sum(a, axis=1)
Matrix Operations
np.add(a, b)
np.matmul(a, b)
🐼 Pandas
Pandas is used for data analysis and manipulation.

Core Structures
Series → 1D data

DataFrame → 2D table

Creating DataFrame
import pandas as pd

df = pd.DataFrame({
    "Name": ["A", "B"],
    "Marks": [80, 90]
})
Pandas Built-in Functions
Function	Purpose
shape	Rows & columns
head()	First 5 rows
tail()	Last 5 rows
info()	Dataset summary
unique()	Unique values
value_counts()	Frequency
isnull().sum()	Missing values
select_dtypes()	Select datatype
groupby()	Group data
fillna()	Fill missing values
drop()	Remove rows/columns
rename()	Rename columns
index	Index access
loc & iloc
df.loc[0, 'Name']
df.iloc[0, 1]
Axis Usage
axis=0 → rows

axis=1 → columns

df.drop("Marks", axis=1)
CSV Operations
df.to_csv("data.csv", index=False)
pd.read_csv("data.csv")
📊 Matplotlib (Visualization)
Matplotlib is used to visualize data graphically.

Line Chart
import matplotlib.pyplot as plt

plt.plot([1,2,3], [4,5,6])
plt.show()
Scatter Plot
plt.scatter([1,2,3], [4,5,6])
plt.show()
Bar Chart
plt.bar(["A","B","C"], [10,20,30])
plt.show()
Histogram
plt.hist([1,2,2,3,3,3])
plt.show()
Pie Chart
plt.pie([30,40,30], labels=["A","B","C"], autopct="%1.1f%%")
plt.show()
Subplot
plt.subplot(1,2,1)
plt.plot([1,2,3])

plt.subplot(1,2,2)
plt.bar([1,2,3],[3,2,1])
plt.show()



📊 Matplotlib Visualizations (Code + Output)
1️⃣ Line Chart
✅ Code
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 15, 30]

plt.plot(x, y)
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Line Chart Example")
plt.show()
📈 Output

https://www.w3schools.com/python/img_matplotlib_line_red.png

https://media.geeksforgeeks.org/wp-content/uploads/20201013170331/simpleplot-300x169.png
Used for: Trend over time

2️⃣ Scatter Plot
✅ Code
x = [1, 2, 3, 4]
y = [10, 20, 15, 30]

plt.scatter(x, y)
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Scatter Plot Example")
plt.show()
🔵 Output

https://www.w3schools.com/python/img_matplotlib_scatter_colormap1.png

https://matplotlib.org/stable/_images/sphx_glr_scatter_001.png
Used for: Relationship between variables

3️⃣ Bar Chart
✅ Code
names = ["A", "B", "C"]
marks = [70, 85, 90]

plt.bar(names, marks)
plt.xlabel("Students")
plt.ylabel("Marks")
plt.title("Bar Chart Example")
plt.show()
📊 Output

https://matplotlib.org/3.1.0/_images/sphx_glr_barchart_001.png

https://pythonspot.com/wp-content/uploads/2015/07/figure_barchart.png
Used for: Category comparison

4️⃣ Histogram
✅ Code
data = [10, 20, 20, 30, 30, 30, 40, 50]

plt.hist(data, bins=5)
plt.xlabel("Values")
plt.ylabel("Frequency")
plt.title("Histogram Example")
plt.show()
📉 Output

https://www.w3schools.com/python/img_matplotlib_histogram1.png

https://media.geeksforgeeks.org/wp-content/uploads/20231205223137/Screenshot-2023-12-05-222229.png
Used for: Data distribution

5️⃣ Pie Chart
✅ Code
sizes = [40, 35, 25]
labels = ["Python", "Java", "C++"]

plt.pie(sizes, labels=labels, autopct="%1.1f%%")
plt.title("Pie Chart Example")
plt.show()
🥧 Output

https://pythonspot.com/wp-content/uploads/2015/07/matplotlib_pie.png

https://matplotlib.org/stable/_images/sphx_glr_pie_and_donut_labels_002.png
Used for: Percentage representation

6️⃣ Subplots
✅ Code
plt.subplot(1, 2, 1)
plt.plot([1,2,3], [3,2,1])
plt.title("Line Chart")

plt.subplot(1, 2, 2)
plt.bar([1,2,3], [1,2,3])
plt.title("Bar Chart")

plt.show()
🧩 Output

https://matplotlib.org/stable/_images/sphx_glr_subplots_demo_002.png

https://i.stack.imgur.com/1kSL5.png
Used for: Multiple charts in one figure

🧠 Quick Chart Selection
Chart	Best Use
Line	Trend
Scatter	Relationship
Bar	Comparison
Histogram	Distribution
Pie	Percentage
Subplot	Multiple views






 









##  Contact
kottamula priyanka
email:priyankakottamula@gmail.com
phno:6303145006








