# Python Cheat Sheet
A brief, succint guide for picking up the Python language. Each section contains definitions and an abudance of examples.
###### Feel free to suggest changes

# Table of contents
- [Introduction](#introduction)
  * [1. Variables and types](#1-variables-and-types)
  * [2. Conversions](#2-conversions)
  * [Examples](#examples)
  * [3. Conditional statement](#3-conditional-statement)
  * [Examples](#examples-1)
  * [4. Loops](#4-loops)
- [Lists & Containers - Will be continued](#lists--containers---will-be-continued)
- [Examples](#examples-2)
- [Resources used](#resources-used)


# Introduction

## 1. Variables and types
- Variables are defined without specifying their types (*However, one can specify a type if wanted. See (1)*).
- Through the types available, we can mention:
  - **int**: they represent natural numbers
  ```python
  some_integer_number = 3
  x: int = 3
  ```
  - **float**: they represent fractionals (comma sepparated numbers);
  
  \*Python infers the division of numbers to float.
  ```python
  some_float_number = 3.14
  y: float = 3.14
  result_of_division = 3 / 2 # == 1.5
  ```
  - **char**: they represent characters.
  ```python
  some_char = 'a'
  c: char = 'b'
  ```
  - **str**: they represent strings.
  ```python
  some_string = "some example string"
  string_example: string = "this is a string"
  ```
  - **bool**: they represent booleans. They are only *True* or *False*.
  ```python
  some_bool = True
  another_bool: bool = False
  ```
## 2. Conversions
- Variables can have their types converted.
- One can use the type name to convert from a type to another
## Examples
```python
some_int = 3
# Converting from int to float (works vice-versa)
some_float = float(some_int)
# Converting from int to string (works vice-versa, BUT string must be a valid number)
some_str = str(some_int)
# Converting from char to int (gives the ASCII code for the character)
some_int = chr('a') # == 97 
# Converting from int to char (given the ASCII code, it gets back the character)
some_char = ord(97) # == 'a'
```

## 3. Conditional statement
- Statement block gets executed only if the checked expression is **true**.
- Can be chained by **elif** and **else**, however only one block (or none) will get executed.
- if, elif and else **must always** be followed by *:*.

## Examples
1. Printing x only if x is odd
```python
if x % 2 == 0:
  print(x)
```

2. Adding 1 to x if x is divisible with 10, adding 2 if it is even or subtract 1 is neither is true
```python
if x % 10 == 0:
  x += 1
elif x % 2 == 0:
  x += 2
else:
  x -= 1
```

## 4. Loops
4.1. For loops
- They are used to iterate over a range of values and execute the block instruction that many teams
```python
for i in range(start, end, step):
  # do something
```
4.2 While loops
- While loops execute as long as the expression verified is true.
- The block statement is executed every time the while loop's condition is true
```python
# Looping as long as x is greater than 10
while x > 10:
  # do something
```
# Lists & Containers - Will be continued
- Lists can be seen as a container for multiple elements of the same type
- They are represented using *'[]'*
- To access an index, use the list variable and put the index inside square brackets.
```python
some_list = [1, 2, 3]
# Print the second element
print(some_list[1])
```
# Examples
1. Initializing a list of size N, full of 0's
```python
example_list = [0 for i in range (N)]
```


###### (1) Starting with Python 3.6, one can define a type for a variable as follows:
```python
x: int = 3
some_string: str = "some string"
```


# Resources used
*Python Cheat Sheet [python:cours:mementopython3-english.pdf](https://perso.limsi.fr/pointal/_media/python:cours:mementopython3-english.pdf)*
