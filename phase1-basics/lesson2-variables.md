# Lesson 2: Variables & Data Types

## What is a Variable?

A **variable** is a container that stores information. Think of it like a labeled box:

```
┌─────────────────┐
│   name = "Bob"  │ ← Variable "name" holds the value "Bob"
└─────────────────┘
```

## Creating Variables

### Syntax
```python
variable_name = value
```

### Examples
```python
name = "Alice"
age = 25
height = 5.7
is_student = True
```

**Rules for variable names:**
- Start with letter or underscore: `_age`, `name`
- Use letters, numbers, underscores: `user_age_1`
- Can't start with number: ❌ `1_age`
- Can't use spaces: ❌ `user age`
- Avoid Python keywords: ❌ `class`, `for`, `if`

## Data Types

Python has several built-in data types. The main ones are:

### 1. String (Text) - `str`

Text enclosed in quotes:

```python
name = "Alice"
greeting = 'Hello World'
sentence = """This is a 
multi-line string"""

print(name)           # Alice
print(type(name))     # <class 'str'>
```

### 2. Integer (Whole Numbers) - `int`

Numbers without decimals:

```python
age = 25
score = -10
year = 2024

print(age)            # 25
print(type(age))      # <class 'int'>
```

### 3. Float (Decimal Numbers) - `float`

Numbers with decimals:

```python
height = 5.7
temperature = -3.14
price = 19.99

print(height)         # 5.7
print(type(height))   # <class 'float'>
```

### 4. Boolean (True/False) - `bool`

Only two possible values:

```python
is_student = True
is_raining = False

print(is_student)     # True
print(type(is_student))  # <class 'bool'>
```

## Working with Variables

### Printing Variables
```python
name = "Bob"
age = 30

print(name)           # Bob
print(age)            # 30
print(name, age)      # Bob 30
```

### String Concatenation (Joining Strings)
```python
first_name = "John"
last_name = "Doe"

full_name = first_name + " " + last_name
print(full_name)      # John Doe
```

### String Formatting (Modern Way - f-strings)
```python
name = "Alice"
age = 25

# Method 1: f-string (preferred)
print(f"My name is {name} and I am {age} years old")

# Method 2: format()
print("My name is {} and I am {} years old".format(name, age))

# Method 3: concatenation (older)
print("My name is " + name + " and I am " + str(age) + " years old")
```

### Type Conversion
```python
# String to Integer
age_str = "25"
age = int(age_str)
print(age + 5)        # 30

# Integer to String
number = 42
text = str(number)
print(text + " is the answer")  # 42 is the answer

# String to Float
price_str = "9.99"
price = float(price_str)
print(price)          # 9.99
```

## Complete Example

```python
# Personal Information Program
name = "Sarah"
age = 28
height = 5.6
is_working = True

print("=" * 40)
print("PERSONAL INFORMATION")
print("=" * 40)

print(f"Name: {name}")
print(f"Age: {age} years old")
print(f"Height: {height} feet")
print(f"Currently working: {is_working}")

print("=" * 40)
```

Output:
```
========================================
PERSONAL INFORMATION
========================================
Name: Sarah
Age: 28 years old
Height: 5.6 feet
Currently working: True
========================================
```

## Data Type Summary

| Type | Name | Example | Use Case |
|------|------|---------|----------|
| `str` | String | `"Hello"` | Text, names, messages |
| `int` | Integer | `42`, `-5` | Whole numbers, counts |
| `float` | Float | `3.14`, `-2.5` | Decimals, measurements |
| `bool` | Boolean | `True`, `False` | Yes/No, True/False |

## Exercises

### Exercise 2.1: Create Variables
Create a program with variables for:
- Your full name (string)
- Your age (integer)
- Your height in meters (float)
- Whether you like pizza (boolean)

Print all of them.

### Exercise 2.2: String Formatting
Create a program that stores:
- Product name: "Laptop"
- Price: 999.99
- In stock: True

Print a formatted message like:
```
Laptop is available for $999.99
```

### Exercise 2.3: Type Conversion
Ask the user's birth year (as a string), convert to integer, and calculate their age:
```python
birth_year = "2000"
# Convert and calculate
current_year = 2024
age = current_year - int(birth_year)
print(f"You are {age} years old")  # You are 24 years old
```

### Exercise 2.4: Mad Libs
Create a mad libs game where you store:
- A name
- An animal
- A food
- An adjective

Then print a funny story using all of them!

---

**Key Takeaways:**
- Variables store data with a name
- Python has 4 main data types: str, int, float, bool
- Use `type()` to check a variable's type
- Use f-strings to insert variables into text
- Convert types when needed with `int()`, `str()`, `float()`

Next → **Lesson 3: Basic Operations**
