## Scope, Reusability & Importing Modules

---

### Learning Objectives

By the end of this lesson, you’ll:

* Understand **variable scope** (local, global, and nonlocal)
* Know how **functions** improve code reusability
* Learn how to **import and use Python modules**
* Apply modules like `math`, `random`, and `datetime` in real examples

---

## Variable Scope

Every variable in Python has a **scope**, which determines **where it can be accessed**.

| Scope Type   | Description                                                                       | Example                      |
| ------------ | --------------------------------------------------------------------------------- | ---------------------------- |
| **Local**    | Variable inside a function. Only accessible there.                                | Defined inside a function    |
| **Global**   | Defined outside any function. Accessible anywhere.                                | Declared at top-level        |
| **Nonlocal** | Used inside nested functions, refers to variable in outer (but not global) scope. | Used with `nonlocal` keyword |

---

### Example 1: Local vs Global

```python
x = 10  # global variable

def show_numbers():
    x = 5   # local variable
    print("Inside function:", x)

show_numbers()
print("Outside function:", x)
```

**Think:** Why do we get two different outputs?

Local variable inside the function overrides the global one **only within the function’s scope**.

---

### Example 2: Using `global` keyword

Sometimes, you want to **modify** a global variable inside a function.

```python
counter = 0

def increase():
    global counter
    counter += 1
    print("Counter inside function:", counter)

increase()
print("Counter outside function:", counter)
```

Use `global` carefully — too many global variables make your code unpredictable.

---

### Example 3: `nonlocal` keyword

Used when you have **nested functions** (a function inside another function).

```python
def outer():
    message = "hello"

    def inner():
        nonlocal message
        message = "hi"
        print("Inner:", message)

    inner()
    print("Outer:", message)

outer()
```

Output:

```
Inner: hi
Outer: hi
```

The inner function **modified** the variable in the enclosing function.

---

## Reusability with Functions

Functions let you **reuse logic** instead of repeating code.

### Example 4: Simple Reusable Function

```python
def greet(name):
    print(f"Hello, {name}!")

greet("AG")
greet("Ada")
```

Try modifying it to return a string instead of printing it!

---

### Example 5: Function Return Values

```python
def add_numbers(a, b):
    return a + b

result = add_numbers(5, 7)
print("Sum:", result)
```

You can store returned values for further use — this is how real projects stay modular and testable.

---

## 3️⃣ Importing Modules

Python comes with a massive **standard library** — you don’t have to reinvent the wheel.

Let’s look at three key modules you’ll use **constantly**:
`math`, `random`, `datetime`

---

### 3.1 The `math` Module

```python
import math

print(math.sqrt(25))   # square root
print(math.pi)         # constant π
print(math.factorial(5))
print(math.sin(math.radians(90)))  # sine of 90 degrees
```

Try It:

* Compute `log(100, 10)`
* Round up and down using `ceil()` and `floor()`

---

### 3.2 The `random` Module

```python
import random

print(random.randint(1, 6))  # random integer between 1 and 6
print(random.choice(["Python", "C++", "Rust"]))  # random pick from list
print(random.random())  # random float between 0 and 1
```

Try It:

* Simulate a dice roll 10 times
* Build a mini lottery picker!

---

### 3.3 The `datetime` Module

```python
import datetime

now = datetime.datetime.now()
print("Current time:", now)
print("Year:", now.year)
print("Month:", now.month)
print("Day:", now.day)

# Create custom date
birthday = datetime.date(2025, 11, 1)
print("Birthday:", birthday)
```

Try It:

* Find the difference between today and your next birthday
* Display the current time every second for 5 seconds (use a loop and `time.sleep(1)`)

---

## QUIZ TIME

**Q1:** What is the output?

```python
x = 50
def test():
    x = 20
    print(x)
test()
print(x)
```

* A) 50, 50
* B) 20, 20
* C) 20, 50 

---

**Q2:** Which statement about `global` is true?

* A) It defines variables that can only be used in one function
* B) It allows a function to modify a variable declared outside it 
* C) It deletes local variables

---

**Q3:** What does this code print?

```python
import math
print(math.floor(3.7), math.ceil(3.7))
```

---

## 💻 ASSIGNMENT

### Task 1: Build a Mini Calculator (Revisited)

* Use functions for each operation (`add`, `subtract`, `multiply`, `divide`)
* Use `math` module to add `sqrt()` and `power()` features
* Add random test questions using the `random` module

---

### Task 2: “Days Until Birthday” App

Write a program that:

* Takes your birthday (month & day)
* Uses `datetime` to calculate days until next birthday
* Prints `"X days left!"`
