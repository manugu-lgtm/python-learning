# Lesson 3: Basic Operations

## Arithmetic Operations

Python can perform math! Here are the main operators:

### Basic Math Operators

```python
# Addition
print(10 + 5)         # 15
print(3.5 + 2.5)      # 6.0

# Subtraction
print(10 - 5)         # 5
print(-10 + 3)        # -7

# Multiplication
print(10 * 5)         # 50
print(3.5 * 2)        # 7.0

# Division (always returns float)
print(10 / 5)         # 2.0
print(10 / 3)         # 3.333...

# Floor Division (removes decimal)
print(10 // 3)        # 3
print(10 // 4)        # 2

# Modulo (remainder)
print(10 % 3)         # 1
print(10 % 4)         # 2

# Exponentiation (power)
print(2 ** 3)         # 8
print(5 ** 2)         # 25
```

## Order of Operations (PEMDAS)

Python follows the same order as math:

```python
result = 2 + 3 * 4      # 14 (NOT 20)
# Multiplication first: 3 * 4 = 12
# Then addition: 2 + 12 = 14

result = (2 + 3) * 4    # 20 (parentheses first)
```

**Order:**
1. Parentheses `()`
2. Exponents `**`
3. Multiplication/Division `*`, `/`, `//`, `%`
4. Addition/Subtraction `+`, `-`

## Using Operations with Variables

```python
# Calculate rectangle area
width = 5
height = 10
area = width * height
print(f"Area: {area}")  # Area: 50

# Calculate average
score1 = 85
score2 = 90
score3 = 78
average = (score1 + score2 + score3) / 3
print(f"Average: {average}")  # Average: 84.333...

# Calculate remaining money
starting_balance = 100
spent = 35
remaining = starting_balance - spent
print(f"Remaining: ${remaining}")  # Remaining: $65
```

## Updating Variables

### Using Shorthand Operators

```python
# Add to variable
count = 5
count = count + 1
print(count)          # 6

# Shorthand version (do the same thing)
count += 1            # Same as: count = count + 1
print(count)          # 7

# Other shorthand operators
count -= 2            # Same as: count = count - 2
count *= 3            # Same as: count = count * 3
count /= 2            # Same as: count = count / 2
count //= 2           # Same as: count = count // 2

# String concatenation shorthand
name = "Alice"
name += " Smith"      # Same as: name = name + " Smith"
print(name)           # Alice Smith
```

## String Operations

### String Repetition
```python
print("Ha" * 3)       # HaHaHa
print("-" * 20)       # --------------------

stars = "*"
print(stars * 10)     # **********
```

### String Length
```python
text = "Python"
length = len(text)
print(length)         # 6

name = "Bob"
print(len(name))      # 3
```

### Checking if Text Contains Something
```python
text = "Hello World"

print("Hello" in text)   # True
print("Goodbye" in text) # False
print("o" in text)       # True

# Negation
print("Goodbye" not in text)  # True
print("Hello" not in text)    # False
```

## Comparison Operators

These create True/False values:

```python
# Equal to
print(5 == 5)         # True
print(5 == 3)         # False

# Not equal to
print(5 != 3)         # True
print(5 != 5)         # False

# Greater than
print(5 > 3)          # True
print(3 > 5)          # False

# Less than
print(3 < 5)          # True
print(5 < 3)          # False

# Greater than or equal
print(5 >= 5)         # True
print(5 >= 3)         # True
print(3 >= 5)         # False

# Less than or equal
print(3 <= 5)         # True
print(5 <= 5)         # True
print(5 <= 3)         # False
```

## Logical Operators

Combine multiple conditions:

```python
# AND - both must be True
print(True and True)   # True
print(True and False)  # False
print(False and False) # False

age = 25
income = 50000
print(age > 18 and income > 40000)  # True

# OR - at least one must be True
print(True or False)   # True
print(False or False)  # False
print(True or True)    # True

day = "Saturday"
print(day == "Saturday" or day == "Sunday")  # True

# NOT - opposite
print(not True)        # False
print(not False)       # True

is_raining = True
print(not is_raining)  # False
```

## Practical Example: Pizza Calculator

```python
# Pizza Calculator
pizza_price = 15.99
quantity = 3
tax_rate = 0.08

# Calculate subtotal
subtotal = pizza_price * quantity
print(f"Subtotal: ${subtotal:.2f}")

# Calculate tax
tax = subtotal * tax_rate
print(f"Tax: ${tax:.2f}")

# Calculate total
total = subtotal + tax
print(f"Total: ${total:.2f}")

# How much per pizza?
price_per_pizza = total / quantity
print(f"Cost per pizza: ${price_per_pizza:.2f}")

# Compare prices
competitor_price = 14.50
print(f"Cheaper than competitor? {pizza_price < competitor_price}")
```

Output:
```
Subtotal: $47.97
Tax: $3.84
Total: $51.81
Cost per pizza: $17.27
Cheaper than competitor? False
```

## Common Mistakes

```python
# ❌ WRONG: Using = instead of ==
if age = 18:         # Syntax error!
    print("Adult")

# ✅ CORRECT: Use == to compare
if age == 18:
    print("Adult")

# ❌ WRONG: Confusing + and += 
name + " Smith"      # Creates new string but doesn't save it

# ✅ CORRECT: Use += to update
name += " Smith"     # Updates the variable

# ❌ WRONG: Math with strings
print("5" + "3")     # "53" (concatenation, not math!)

# ✅ CORRECT: Convert to numbers first
print(int("5") + int("3"))  # 8
```

## Exercises

### Exercise 3.1: Simple Calculator
Create a program that calculates:
- Sum of 10 + 20
- Difference of 50 - 15
- Product of 6 * 7
- Division of 100 / 4

Print all results.

### Exercise 3.2: Bill Splitter
Two friends went out to dinner. The bill was $45.78. They want to split it equally and add a 20% tip.
- Calculate the split amount per person
- Calculate total tip
- Calculate how much each person pays

### Exercise 3.3: Temperature Converter
Store a temperature in Celsius: `celsius = 25`
Convert to Fahrenheit using: `(celsius * 9/5) + 32`
Print the result.

### Exercise 3.4: True or False?
Write expressions that evaluate to True or False:
```python
print(10 > 5 and 20 < 30)         # ?
print(True or False)              # ?
print("Hello" in "Hello World")   # ?
print(100 / 10 == 10)             # ?
print(not (5 > 10))               # ?
```

---

**Key Takeaways:**
- Use `+`, `-`, `*`, `/`, `//`, `%`, `**` for math
- Use comparison operators (`==`, `!=`, `<`, `>`, `<=`, `>=`) to compare
- Use logical operators (`and`, `or`, `not`) to combine conditions
- Update variables with `+=`, `-=`, `*=`, `/=`
- Strings can be repeated with `*` and checked with `in`

Next → **Lesson 4: Input & Output**
