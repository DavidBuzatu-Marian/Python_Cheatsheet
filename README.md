# Python Cheat Sheet
A brief, succint guide for picking up the Python language. Each section contains definitions and an abudance of examples.
## Feel free to suggest changes

# Table of contents
- [Table of contents](#table-of-contents)
- [Introduction](#introduction)
  * [1. Variables and types](#1-variables-and-types)
  * [2. Conversions](#2-conversions)
  * [Examples (Conversions)](#examples)
  * [3. Conditional statement](#3-conditional-statement)
  * [Examples (Conditionals)](#examples-1)
  * [4. Loops](#4-loops)
- [Lists](#lists)
- [Examples (Lists)](#examples-2)
- [Functions](#functions)
  * [Recursive functions](#recursive-functions)
- [Examples (Functions)](#examples--functions-)
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
# Lists
- Lists can be seen as a container for multiple elements of the same type.
- They are represented using *'[]'*.
- To access an index, use the list variable and put the index inside square brackets.
```python
some_list = [1, 2, 3]
# Print the second element
print(some_list[1])
```
- To create a sublist of a list, one can use the following notation:
```python
some_list = [1, 2, 3, 4, 5]
sub_list = some_list[idx_start:idx_end]
```
where **idx_start** represents the starting index for the substring and **idx_end** the ending index (non-inclusive).
# Examples
1. Initializing a list of size N, full of 0's
```python
example_list = [0 for i in range (N)]
```
2. Initializing a list of lists (matrix) of N rows and M columns
```python
example_matrix = [[0 for j in range (M)] for i in range (N)] 
```

# Functions
- Functions are blocks of reusable code that may be used anywhere throughout a program.
- They are composed of a header and body.
- The head of a function is defined as:
 - The **def** keyword
 - a *name* for the function
 - *parameters* of the function inside round brackets
 - Colon *:*
 E.g.:
 ```python
 def first_function(some_parameter):
   # some action
 ```
- Parameters are values that the function might use in its block code
E.g.: A function that gets a value and returns the value + 1
```python
def addOne(number):
  return number + 1
```
- A function can return a value or not. A function without a return value is called *void* function.
- A function can return any type of variable.
- Parameters can me of two types: immutable or mutable.
- Immutable types include: strings, integers, booleans.
- Mutable types include: lists, objects, containers.
## Recursive functions
- Are functions that call themselves.
- A well defined recursive function is composed of two things:
 - The base case: defines the stopping condition for the recursion
 - The general case: defines the part of code that is executed on each call that is not the base case

# Examples (Functions)
1. A function which returns True if the parameter passed is greater than 5, otherwise returns False
```python
def greaterThanFive(number):
    if number > 5:
        return True
    return False
```
2. Function to calculate the nth Fibonacci number (recursively)
```python
def fibo(n):
    if n == 0 or n == 1:
        return 1
    return fibo(n - 1) + fibo(n - 2)
```
3. Fibonnaci improved, using a list to memorise numbers calculated already
```python
def fibo(n, fib):
    if n == 0 or n == 1:
        return 1
    if fib[n] != 0:
        return fib[n]
    fibonacci_value = fibo(n - 1, fib) + fibo(n - 2, fib)
    fib[n] = fibonacci_value
    return fibonacci_value
list_fibo = [0 for i in range (0, 1001)]
# function call. It won't print anything! How would you print the result?
fibo(100, list_fibo)
```
4. Simplest and fastest Fibonacci function (non-recursive/iterative):
```python
def fibo_smartest(n):
    if n == 0 or n == 1:
        return 1
    fibo_prev = 1
    fibo_prev_prev = 1
    for i in range(2, n + 1):
        fibo_curr = fibo_prev + fibo_prev_prev
        fibo_prev_prev = fibo_prev
        fibo_prev = fibo_curr
    return fibo_prev
```


###### (1) Starting with Python 3.6, one can define a type for a variable as follows:
```python
x: int = 3
some_string: str = "some string"
```

# Resources used
*Python Cheat Sheet [python:cours:mementopython3-english.pdf](https://perso.limsi.fr/pointal/_media/python:cours:mementopython3-english.pdf)*
*Python function parameters passing [stackoverflow](https://stackoverflow.com/a/60979567/11023871)*
