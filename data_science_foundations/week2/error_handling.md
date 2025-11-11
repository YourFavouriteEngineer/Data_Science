## Functions & Error Handling

---

### Learning Objectives

By the end of this lesson, you’ll:

* Master **error handling** using `try`, `except`, `else`, and `finally`
* Debug code like a pro with meaningful exceptions

---

Programs fail.
But Python gives you tools to **handle** failures gracefully using `try` and `except`.

---

### Example 1: Basic Try/Except

```python
try:
    x = int(input("Enter a number: "))
    print(10 / x)
except:
    print("Something went wrong.")
```

Problem: This catches *everything*.
Better to catch **specific errors**.

---

### Example 2: Handling Specific Exceptions

```python
try:
    x = int(input("Enter a number: "))
    print(10 / x)
except ValueError:
    print("That's not a number!")
except ZeroDivisionError:
    print("You can't divide by zero!")
```

Now, you give **precise feedback**.

---

### Example 3: `else` and `finally`

```python
try:
    num = int(input("Enter a number: "))
except ValueError:
    print("Invalid input.")
else:
    print(f"You entered {num}")
finally:
    print("End of program.")
```

* `else` runs **only if no exception occurred**.
* `finally` runs **no matter what** (cleanup, closing files, etc.)

---

### Example 4: Raising Your Own Exceptions

You can raise custom exceptions when input isn’t acceptable.

```python
def withdraw(balance, amount):
    if amount > balance:
        raise ValueError("Insufficient funds!")
    return balance - amount

try:
    print(withdraw(1000, 1500))
except ValueError as e:
    print("Error:", e)
```

In real systems, you’ll see this in **bank apps, APIs, and robotics safety checks**.

---

## QUIZ TIME

**Q1:** What will this print?

```python
def test(x=2, y=3):
    return x * y

print(test(4))
```

 Output → `12`
Reason: `x=4`, `y` remains default `3`.

---

**Q2:** What does `*args` collect arguments as?

* A) Dictionary
* B) Tuple 
* C) List
* D) Set

---

**Q3:** What does this output?

```python
try:
    print(10 / 0)
except ZeroDivisionError:
    print("Error!")
```

Output → `Error!`

---

## ASSIGNMENT

### Task 1: Smart Calculator (with Error Handling)

Create a calculator that:

* Takes two numbers and an operator
* Supports `+`, `-`, `*`, `/`, and `sqrt`
* Uses `try/except` to catch invalid inputs or division by zero
* Wraps each operation in a function

---

### Task 2: Random Password Generator

Use what you know from:

* `random` module
* `functions`
* `error handling`

Write a program that:

1. Asks for password length
2. Generates a random mix of letters, digits, and symbols
3. Handles non-integer input gracefully

Hint:

```python
import random, string
string.ascii_letters, string.digits, string.punctuation
```

---

### Task 3: Custom “Safe Withdraw” App

Create a function that:

* Takes balance and withdrawal amount
* Raises a `ValueError` if balance < withdrawal
* Uses `try/except` to print a user-friendly message

