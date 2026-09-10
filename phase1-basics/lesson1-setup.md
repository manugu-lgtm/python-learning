# Lesson 1: Getting Started & Setup

## What is Python?

Python is a **programming language** - a way to give instructions to a computer. It's:
- **Easy to read** - looks almost like English
- **Powerful** - used by Google, Netflix, Instagram, NASA
- **Versatile** - web apps, data science, AI, automation, games

## Installing Python

### Step 1: Download Python
Go to [python.org](https://www.python.org) and download Python 3.12 (or latest 3.x version)

### Step 2: Install
- **Windows**: Run installer, **check "Add Python to PATH"**, click Install
- **Mac**: Run installer and follow prompts
- **Linux**: `sudo apt-get install python3`

### Step 3: Verify Installation
Open terminal/command prompt and type:
```bash
python --version
```

You should see: `Python 3.x.x`

## Your First Program

### Method 1: Interactive Mode (REPL)
Type `python` in terminal, then:

```python
>>> print("Hello, World!")
Hello, World!
```

Great! You just ran Python code. Type `exit()` to quit.

### Method 2: Script File
1. Create a file named `hello.py` with this content:

```python
print("Hello, World!")
```

2. Save it in a folder
3. Open terminal in that folder
4. Run: `python hello.py`

## Python Basics

### What is a Program?

A program is a **sequence of instructions** the computer executes line by line.

```python
print("My name is Alice")
print("I am learning Python")
print("This is fun!")
```

Output:
```
My name is Alice
I am learning Python
This is fun!
```

### Comments

Comments are notes to yourself (not executed):

```python
# This is a comment - it's ignored by Python
print("This runs")  # This comment is also ignored

"""
Multi-line comments
use triple quotes
"""
```

### Indentation

Python uses **indentation** (spaces) to organize code. This is important and we'll see why later.

```python
print("Start")
print("End")  # No indentation needed here
```

## Your First Real Program

Create a file called `introduce_yourself.py`:

```python
# My first real program
print("=" * 30)
print("Welcome to Python!")
print("=" * 30)

print("\nHello! My name is Python Learner")
print("I am excited to learn programming")
print("Let's get started!")

print("\n" + "=" * 30)
```

Run it and see the output!

## Key Concepts So Far

| Concept | Meaning |
|---------|---------|
| **print()** | Displays text on screen |
| **Comment** | Text ignored by Python (marked with #) |
| **String** | Text in quotes ("hello") |
| **Syntax** | Rules of Python language |

## Exercises

### Exercise 1.1: Your First Print
Create a file and print your name, age, and favorite hobby (3 print statements).

### Exercise 1.2: Multi-line Output
Create a program that prints a box pattern:
```
**********
*        *
*  Hello *
*        *
**********
```

### Exercise 1.3: Comments Practice
Write a program with at least 3 comments explaining what each line does.

## Next Steps

✅ Python is installed  
✅ You can run Python files  
✅ You can print text  

Ready? Move to **Lesson 2: Variables & Data Types** →

---

## Troubleshooting

**"python: command not found"**
- Make sure Python is installed
- Add Python to PATH (reinstall with this option on Windows)

**"SyntaxError"**
- Check for typos
- Make sure quotes match: `"text"` not `"text'`

**File won't run**
- Make sure you saved the file
- Run from correct folder: `cd /path/to/folder`
- Use correct filename: `python filename.py`
