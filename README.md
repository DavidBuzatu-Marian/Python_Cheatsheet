# Python Cheat Sheet
A brief, succint guide for picking up the Python language. Each section contains definitions and an abudance of examples.
###### Feel free to suggest changes

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
# Lists & Containers (Will be continued)



###### (1) Starting with Python 3.6, one can define a type for a variable as follows:
```python
x: int = 3
some_string: str = "some string"
```


# Resources used
*Python Cheat Sheet [python:cours:mementopython3-english.pdf](https://perso.limsi.fr/pointal/_media/python:cours:mementopython3-english.pdf)*
