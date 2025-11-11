# Importing Modules (math, random, datetime)

---

## Objective

By the end of this lesson, learners will:

* Understand what **modules** are
* Know how to **import** and **use** built-in modules
* Learn **math**, **random**, and **datetime** through practical mini-projects
* Know how to create **their own custom module** later (we’ll cover that next)

---

## 1. What Are Modules?

A **module** is simply a **Python file** that contains **functions, variables, or classes** you can reuse.

Think of it as a **toolbox** — you don’t rebuild a hammer each time you need one.

---

### Why Modules Exist

* To **organize code** into logical sections
* To **reuse** existing functionality
* To **extend Python’s power** with external packages

---

## 2. How to Import Modules

You can import in several ways:

```python
import math
```

Then use:

```python
math.sqrt(16)
```

Or import only specific parts:

```python
from math import sqrt
print(sqrt(16))
```

Or rename for convenience:

```python
import math as m
print(m.sqrt(25))
```

---

## 3. The `math` Module: Advanced Mathematics

The `math` module gives you access to **scientific and engineering-level functions**.

Let’s explore the most useful ones.

---

### 🔹 Square Roots and Powers

```python
import math

print(math.sqrt(49))      # 7.0
print(math.pow(2, 5))     # 32.0
```

---

### 🔹 Rounding and Constants

```python
print(math.ceil(4.2))   # 5
print(math.floor(4.8))  # 4

print(math.pi)          # 3.141592653589793
print(math.e)           # 2.718281828459045
```

---

### 🔹 Trigonometry (for robotics or automation)

```python
angle = math.radians(30)
print(math.sin(angle))  # 0.5
print(math.cos(angle))  # 0.866...
```

---

### Quick Quiz

**Q:** What’s the difference between `ceil()` and `floor()`?
**A)** `ceil()` rounds up, `floor()` rounds down 

---

### Mini Challenge 1:

Write a program that:

1. Takes radius as input
2. Calculates:

   * Area of circle = πr²
   * Circumference = 2πr
3. Prints both results neatly.

---

## 4. The `random` Module: Generating Randomness

Random numbers are everywhere:

* Gaming 
* Simulations 
* Data sampling 
* Security 

---

### 🔹 Random Integers and Floats

```python
import random

print(random.randint(1, 10))     # Random integer 1–10
print(random.random())           # Random float 0–1
print(random.uniform(5, 15))     # Random float 5–15
```

---

### 🔹 Random Choice

```python
colors = ["red", "blue", "green", "yellow"]
print(random.choice(colors))
```

---

### 🔹 Shuffling Lists

```python
cards = ["A", "K", "Q", "J", "10"]
random.shuffle(cards)
print(cards)
```

---

### Mini Challenge 2: Dice Game

Simulate rolling two dice and print both values + total.

 *Hint: use `random.randint(1,6)` twice.*

---

### Quick Quiz

**Q:** Which function picks one random element from a list?
**A)** `choice()` 
**B)** `shuffle()`
**C)** `randint()`

---

## 5. The `datetime` Module — Working with Dates and Time

Real-world projects need timestamps:

* Logging sensor data
* Scheduling tasks
* Recording user actions

Let’s master this.

---

### 🔹 Getting Current Date & Time

```python
import datetime

now = datetime.datetime.now()
print("Current:", now)
```

---

### 🔹 Extracting Components

```python
print(now.year, now.month, now.day)
print(now.hour, now.minute)
```

---

### 🔹 Formatting Dates

```python
print(now.strftime("%Y-%m-%d %H:%M:%S"))
print(now.strftime("%A, %B %d, %Y"))
```

| Format Code | Meaning        | Example  |
| ----------- | -------------- | -------- |
| `%Y`        | Year           | 2025     |
| `%m`        | Month (number) | 11       |
| `%B`        | Month (word)   | November |
| `%d`        | Day            | 01       |
| `%A`        | Day name       | Saturday |
| `%H`        | Hour           | 13       |
| `%M`        | Minute         | 45       |
| `%S`        | Second         | 09       |

---

### 🔹 Creating Custom Dates

```python
birthday = datetime.date(1998, 7, 23)
print(birthday)
```

---

### 🔹 Date Arithmetic

```python
from datetime import date, timedelta

today = date.today()
future = today + timedelta(days=30)

print("Today:", today)
print("30 days later:", future)
```

---

### Mini Challenge 3: Countdown to a Date

Ask the user for their next birthday (YYYY-MM-DD), calculate and print:

> “ Your birthday is in X days!”

*Hint:* subtract `today` from `target_date`.

---

### Quick Quiz

**Q:** What does `datetime.now()` return?
**A)** Current time 
**B)** System timezone
**C)** Day name only

---

##  6. Combine All Three — Smart Date Game

Let’s make it practical. Combine **math**, **random**, and **datetime**.

---

###  Mini Project: “Random Math Quiz Game”

1. Generate two random integers between 1–10
2. Ask user: “What is num1 × num2?”
3. Check their answer
4. Print a timestamped log message:
   `Correct! (at 2025-11-01 09:22:12)`
5. Repeat 5 times and calculate their score

Modules used: `random`, `datetime`, `math`

---

### Example Run:

```
3 × 4 = ? 12
✅ Correct! (at 2025-11-01 09:22:12)

5 × 6 = ? 32
❌ Wrong! Answer: 30

Final Score: 4 / 5
```

---

## Final Quiz

1️⃣ Which module do you use for square roots?
2️⃣ Which one gives random floats? 
3️⃣ How do you get today’s date? 
---

## Advanced Challenge

Write a **Daily Reminder App** that:

* Prints today’s date
* Randomly selects one motivational quote from a list
* Uses `datetime` for date and `random.choice()` for quote selection
* Prints:

  > “Good Morning! Today is Tuesday, November 1, 2025. 
  > Here’s your quote: ‘Keep going, you’re improving daily.’”

