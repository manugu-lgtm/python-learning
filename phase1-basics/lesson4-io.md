# Lesson 4: Input & Output

## Output (Printing)

We've already seen `print()`. Let's master it!

### Basic Printing
```python
print("Hello, World!")
print(42)
print(3.14)
print(True)
```

### Printing Multiple Items
```python
print("Name:", "Alice")           # Name: Alice
print("Age:", 25, "Height:", 5.7) # Age: 25 Height: 5.7

# Add separator (default is space)
print("A", "B", "C", sep="-")     # A-B-C
print("X", "Y", "Z", sep=" | ")   # X | Y | Z
```

### Printing on Multiple Lines
```python
# Using \n for newline
print("Line 1\nLine 2\nLine 3")

# Using end parameter
print("No newline", end="")
print(" followed by this")

# Output: No newline followed by this
```

### Formatting Numbers
```python
# Round to 2 decimal places
price = 19.9999
print(f"Price: ${price:.2f}")      # Price: $20.00

# Format with commas
number = 1000000
print(f"Number: {number:,}")       # Number: 1,000,000

# Percentage
score = 0.85
print(f"Score: {score:.0%}")       # Score: 85%
```

## Input (Getting User Input)

### The `input()` Function

`input()` pauses the program and waits for the user to type something:

```python
name = input("What is your name? ")
print(f"Hello, {name}!")
```

When you run this:
```
What is your name? Alice
Hello, Alice!
```

### Important: input() Returns a String

Whatever the user types is stored as a **string**, even if they type a number:

```python
age_text = input("How old are you? ")
print(type(age_text))  # <class 'str'>

# To use it as a number, convert it
age = int(age_text)
print(age + 1)  # This works!
```

### Simpler: Combine input() and int()

```python
age = int(input("How old are you? "))
print(f"Next year you'll be {age + 1}")
```

## Interactive Programs

### Example 1: Personal Introduction

```python
# Get user information
name = input("What is your name? ")
age = int(input("How old are you? "))
city = input("What city do you live in? ")

# Display information
print("\n" + "=" * 40)
print("YOUR INFORMATION")
print("=" * 40)
print(f"Name: {name}")
print(f"Age: {age} years old")
print(f"City: {city}")
print("=" * 40)
```

### Example 2: Simple Calculator

```python
# Get numbers from user
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

# Perform operations
addition = num1 + num2
subtraction = num1 - num2
multiplication = num1 * num2
division = num1 / num2 if num2 != 0 else "undefined"

# Display results
print("\n" + "=" * 30)
print(f"{num1} + {num2} = {addition}")
print(f"{num1} - {num2} = {subtraction}")
print(f"{num1} * {num2} = {multiplication}")
print(f"{num1} / {num2} = {division}")
print("=" * 30)
```

Run it:
```
Enter first number: 10
Enter second number: 3

==============================
10.0 + 3.0 = 13.0
10.0 - 3.0 = 7.0
10.0 * 3.0 = 30.0
10.0 / 3.0 = 3.333...
==============================
```

### Example 3: Temperature Converter

```python
# Get temperature in Celsius
celsius = float(input("Enter temperature in Celsius: "))

# Convert to Fahrenheit
fahrenheit = (celsius * 9/5) + 32

# Display result
print(f"{celsius}°C = {fahrenheit:.2f}°F")
```

### Example 4: Pizza Order

```python
print("=" * 40)
print("PIZZA PLACE ORDER")
print("=" * 40)

# Get order details
name = input("What is your name? ")
pizzas = int(input("How many pizzas? "))
price_per_pizza = 12.50
tip_percent = float(input("Tip percentage (e.g., 15 for 15%): "))

# Calculate
subtotal = pizzas * price_per_pizza
tip_amount = subtotal * (tip_percent / 100)
total = subtotal + tip_amount

# Display order
print("\n" + "=" * 40)
print("ORDER SUMMARY")
print("=" * 40)
print(f"Customer: {name}")
print(f"Pizzas: {pizzas} @ ${price_per_pizza:.2f} each")
print(f"Subtotal: ${subtotal:.2f}")
print(f"Tip ({tip_percent}%): ${tip_amount:.2f}")
print(f"Total: ${total:.2f}")
print("=" * 40)
```

## Handling Input Errors

Users sometimes enter wrong types. We'll learn error handling later, but here's a simple check:

```python
# Simple check
user_input = input("Enter your age: ")

if user_input.isdigit():
    age = int(user_input)
    print(f"You are {age} years old")
else:
    print("Please enter a valid number!")
```

## Input/Output Exercises

### Exercise 4.1: Greeting Program
Create a program that:
1. Asks for the user's name
2. Asks for their favorite color
3. Asks for their favorite number
4. Prints: "Hello [name]! Your favorite color is [color] and your favorite number is [number]."

### Exercise 4.2: Area Calculator
Create a program that:
1. Asks for the length of a rectangle
2. Asks for the width
3. Calculates and prints the area
4. Calculates and prints the perimeter

Formula:
- Area = length × width
- Perimeter = 2 × (length + width)

### Exercise 4.3: Money Calculator
Create a program that:
1. Asks how much money the user has
2. Asks the cost of an item
3. Calculates change
4. Prints if they can afford it and how much change they'd get (or how much more they need)

### Exercise 4.4: Quiz Program
Create a simple quiz:
1. Ask 3 questions and get answers
2. Count how many are correct
3. Print the score (e.g., "You got 2 out of 3!")

Questions:
- "What is 5 + 3?" (Answer: 8)
- "What is the capital of France?" (Answer: Paris)
- "How many legs does a cat have?" (Answer: 4)

### Exercise 4.5: Mad Libs
Create a mad libs generator:
1. Ask for 5 random words (noun, verb, adjective, etc.)
2. Plug them into a funny story
3. Print the story

Example story:
"The [adjective] [noun] [verb] to the store to buy [noun]."

---

## Common Mistakes

```python
# ❌ WRONG: Forgetting input() returns a string
age = input("Age: ")
print(age + 5)           # TypeError!

# ✅ CORRECT: Convert to int
age = int(input("Age: "))
print(age + 5)           # Works!

# ❌ WRONG: Using wrong variable name
name = input("Name: ")
print(f"Hello, {nama}")   # NameError!

# ✅ CORRECT: Match variable name
name = input("Name: ")
print(f"Hello, {name}")   # Works!

# ❌ WRONG: input() always waits for user
result = input()         # Program pauses indefinitely!

# ✅ CORRECT: Give clear prompt
name = input("Enter name: ")  # User knows what to type
```

## Quick Reference

| Function | Purpose | Example |
|----------|---------|---------|
| `print()` | Display output | `print("Hello")` |
| `input()` | Get user input | `name = input("Name: ")` |
| `int()` | Convert to integer | `age = int(input("Age: "))` |
| `float()` | Convert to decimal | `price = float(input("Price: "))` |
| `str()` | Convert to string | `text = str(42)` |
| `f"text"` | Format string | `f"Age: {age}"` |

---

**Key Takeaways:**
- `print()` displays information
- `input()` gets information from the user (returns a string)
- Always convert input to the correct type (`int()`, `float()`, etc.)
- Use formatting for nice output (f-strings, `.2f`, `:,`)
- Test your programs with different inputs

Next → **Lesson 5: Conditional Statements (if/else)**
