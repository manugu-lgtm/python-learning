# Lesson 6: Loops (for/while)

## What are Loops?

Loops let your program **repeat code** multiple times.

Instead of:
```python
print("Hello 1")
print("Hello 2")
print("Hello 3")
print("Hello 4")
print("Hello 5")
```

You can write:
```python
for i in range(5):
    print(f"Hello {i+1}")
```

## The `for` Loop

Repeats code for each item in a sequence:

```python
for i in range(5):
    print(i)
```

Output:
```
0
1
2
3
4
```

### How `range()` Works

```python
# range(5) → 0, 1, 2, 3, 4
for i in range(5):
    print(i)

# range(start, end) → start to end-1
for i in range(1, 4):
    print(i)  # 1, 2, 3

# range(start, end, step)
for i in range(0, 10, 2):
    print(i)  # 0, 2, 4, 6, 8

# Counting backward
for i in range(5, 0, -1):
    print(i)  # 5, 4, 3, 2, 1
```

## Looping Through Strings

```python
name = "Python"

for letter in name:
    print(letter)
```

Output:
```
P
y
t
h
o
n
```

## Looping Through Lists

```python
fruits = ["apple", "banana", "orange"]

for fruit in fruits:
    print(fruit)
```

Output:
```
apple
banana
orange
```

## Practical Examples

### Example 1: Print a Pattern

```python
for i in range(5):
    print("*" * (i + 1))
```

Output:
```
*
**
***
****
*****
```

### Example 2: Count Down

```python
for i in range(10, 0, -1):
    print(i)
print("Blastoff!")
```

Output:
```
10
9
8
...
1
Blastoff!
```

### Example 3: Multiplication Table

```python
number = 3

for i in range(1, 11):
    result = number * i
    print(f"{number} × {i} = {result}")
```

Output:
```
3 × 1 = 3
3 × 2 = 6
3 × 3 = 9
...
3 × 10 = 30
```

### Example 4: Sum a List

```python
numbers = [10, 20, 30, 40, 50]
total = 0

for num in numbers:
    total += num

print(f"Total: {total}")  # Total: 150
```

## The `while` Loop

Repeats code **while** a condition is True:

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

Output:
```
1
2
3
4
5
```

### How It Works
1. Check condition: Is count <= 5? Yes
2. Execute code: print(count)
3. Update: count += 1
4. Go back to step 1
5. Continue until condition is False

## `for` vs `while`

### Use `for` when:
- You know how many times to loop
- You're looping through a list/string

```python
for i in range(10):          # Loop 10 times
for item in my_list:         # Loop through list
for letter in "Hello":       # Loop through string
```

### Use `while` when:
- You don't know how many times to loop
- Loop continues based on a condition

```python
while user_input != "quit":  # Loop until user types 'quit'
while age < 18:              # Loop while age is less than 18
while money > 0:             # Loop while money remains
```

## Breaking Out of Loops

### `break` - Exit the Loop

```python
for i in range(10):
    if i == 5:
        break  # Exit loop
    print(i)
```

Output:
```
0
1
2
3
4
```

### `continue` - Skip to Next Iteration

```python
for i in range(5):
    if i == 2:
        continue  # Skip this iteration
    print(i)
```

Output:
```
0
1
3
4
```

## Practical Examples with `while`

### Example 1: User Input Validation

```python
while True:
    password = input("Enter password: ")
    if password == "secret123":
        print("Correct!")
        break
    else:
        print("Try again")
```

### Example 2: Guessing Game

```python
target = 7
guess = None
attempts = 0

while guess != target:
    guess = int(input("Guess a number (1-10): "))
    attempts += 1
    
    if guess < target:
        print("Too low")
    elif guess > target:
        print("Too high")
    else:
        print(f"Correct! You took {attempts} attempts")
```

### Example 3: Menu Program

```python
while True:
    print("\n=== MENU ===")
    print("1. Play")
    print("2. Settings")
    print("3. Quit")
    
    choice = input("Select option: ")
    
    if choice == "1":
        print("Playing...")
    elif choice == "2":
        print("Opening settings...")
    elif choice == "3":
        print("Goodbye!")
        break
    else:
        print("Invalid choice")
```

## Nested Loops

Loop inside a loop:

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(f"({i}, {j})")
```

Output:
```
(1, 1)
(1, 2)
(1, 3)
(2, 1)
(2, 2)
(2, 3)
(3, 1)
(3, 2)
(3, 3)
```

### Example: Multiplication Grid

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(f"{i*j}", end=" ")
    print()  # New line
```

Output:
```
1 2 3 
2 4 6 
3 6 9 
```

## Common Mistakes

```python
# ❌ WRONG: Infinite loop (condition always True)
while True:
    print("This prints forever!")

# ✅ CORRECT: Update variable so condition becomes False
count = 0
while count < 5:
    print(count)
    count += 1

# ❌ WRONG: Forgot to increment
while i < 10:
    print(i)  # Infinite loop!

# ✅ CORRECT: Increment variable
while i < 10:
    print(i)
    i += 1
```

## Exercises

### Exercise 6.1: Print Numbers
Write a program that prints numbers 1 to 10 using a `for` loop.

### Exercise 6.2: Sum of Numbers
Write a program that calculates the sum of numbers 1 to 100.

### Exercise 6.3: Multiplication Table
Write a program that prints the 7 times table (7×1 to 7×10).

### Exercise 6.4: User Guessing Game
Write a program that:
1. Picks a secret number (1-10)
2. Asks user to guess
3. Tells if guess is too high/low
4. Continues until correct
5. Shows number of attempts

### Exercise 6.5: Pattern Maker
Write a program that creates this pattern:
```
#
##
###
####
#####
```

### Exercise 6.6: Count Evens
Write a program that counts how many even numbers are between 1 and 100.

---

**Key Takeaways:**
- `for` loops repeat a set number of times
- `while` loops repeat while a condition is True
- Use `range()` to generate sequences
- `break` exits a loop early
- `continue` skips to the next iteration
- Nested loops create patterns
- Always update variables in `while` loops to avoid infinite loops

Next → **Lesson 7: Break, Continue & Advanced Control**