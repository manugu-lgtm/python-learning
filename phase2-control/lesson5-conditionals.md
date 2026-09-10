# Lesson 5: Conditional Statements (if/else)

## What are Conditionals?

Conditionals let your program make **decisions** based on conditions.

Think of it like:
- If it's raining, bring an umbrella
- Else, enjoy the sunshine

## The `if` Statement

Executes code **only if** a condition is True:

```python
age = 18

if age >= 18:
    print("You are an adult")
```

Output: `You are an adult`

### Another Example

```python
temperature = 15

if temperature < 20:
    print("It's cold, wear a jacket")
```

Output: `It's cold, wear a jacket`

### What if Condition is False?

```python
age = 15

if age >= 18:
    print("You are an adult")  # This won't run

print("Program continues")  # This always runs
```

Output: `Program continues`

## The `if-else` Statement

Executes one block **if** True, another block **if** False:

```python
age = 15

if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")
```

Output: `You are a minor`

### Another Example

```python
score = 75

if score >= 90:
    print("Grade: A")
else:
    print("Not an A")
```

## The `if-elif-else` Statement

Multiple conditions:

```python
score = 75

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
else:
    print("Grade: F")
```

Output: `Grade: C`

### How it works:
1. Check first `if` - is score >= 90? No
2. Check first `elif` - is score >= 80? No
3. Check second `elif` - is score >= 70? **Yes** → Print "Grade: C"
4. Stop checking (don't check `else`)

### Important: Order Matters!

```python
# ❌ WRONG - wrong order
score = 95

if score >= 70:
    print("Grade: C")  # This runs! Problem!
elif score >= 90:
    print("Grade: A")  # Never reached

# ✅ CORRECT - highest first
if score >= 90:
    print("Grade: A")  # This runs
elif score >= 70:
    print("Grade: C")
```

## Indentation is Critical!

Python uses **indentation** (spaces) to show which code belongs to the `if`:

```python
age = 20

if age >= 18:
    print("Line 1: Inside if")
    print("Line 2: Inside if")
print("Line 3: Outside if")  # Always prints
```

```python
# ❌ WRONG - wrong indentation
age = 20
if age >= 18:
print("Syntax Error!")  # Python expects indentation

# ✅ CORRECT
if age >= 18:
    print("Correct!")
```

## Practical Examples

### Example 1: Login Check

```python
password = input("Enter password: ")

if password == "secret123":
    print("Login successful!")
else:
    print("Wrong password")
```

### Example 2: Number Checker

```python
number = int(input("Enter a number: "))

if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
else:
    print("Zero")
```

### Example 3: Even or Odd

```python
number = int(input("Enter a number: "))

if number % 2 == 0:
    print("Even")
else:
    print("Odd")
```

### Example 4: Age Category

```python
age = int(input("Enter your age: "))

if age < 13:
    print("Child")
elif age < 18:
    print("Teen")
elif age < 65:
    print("Adult")
else:
    print("Senior")
```

### Example 5: Letter Grade

```python
score = int(input("Enter your score: "))

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print(f"Your grade: {grade}")
```

## Nested if Statements

`if` inside `if`:

```python
age = 20
has_license = True

if age >= 18:
    if has_license:
        print("You can drive")
    else:
        print("You need a license")
else:
    print("Too young to drive")
```

Output: `You can drive`

## Multiple Conditions (Recap)

```python
age = 20
has_license = True

# Using 'and'
if age >= 18 and has_license:
    print("You can drive")

# Using 'or'
if age < 13 or age > 65:
    print("Special category")

# Using 'not'
if not has_license:
    print("Need a license")
else:
    print("Already licensed")
```

## Exercises

### Exercise 5.1: Simple Age Check
Write a program that:
1. Asks for the user's age
2. Prints "Adult" if age >= 18
3. Prints "Minor" otherwise

### Exercise 5.2: Even or Odd
Write a program that:
1. Asks for a number
2. Prints "Even" if divisible by 2
3. Prints "Odd" otherwise

### Exercise 5.3: Grade Calculator
Write a program that asks for a score and prints:
- "A" if score >= 90
- "B" if score >= 80
- "C" if score >= 70
- "D" if score >= 60
- "F" if score < 60

### Exercise 5.4: Login System
Write a program that:
1. Asks for username
2. Asks for password
3. Checks if username == "admin" AND password == "pass123"
4. Prints "Login successful" or "Login failed"

### Exercise 5.5: Weather Advisor
Write a program that:
1. Asks for temperature
2. Prints advice:
   - "Hot! Drink water" if temp > 30
   - "Warm! Enjoy" if 20 < temp <= 30
   - "Cool! Wear a jacket" if 10 < temp <= 20
   - "Cold! Bundle up" if temp <= 10

---

**Key Takeaways:**
- Use `if` to check one condition
- Use `if-else` for two paths
- Use `if-elif-else` for multiple paths
- **Indentation matters!** It shows what code belongs to the `if`
- Combine conditions with `and`, `or`, `not`
- `elif` is checked only if previous `if` was False

Next → **Lesson 6: Loops (for/while)**