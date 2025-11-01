# Mini Projects 

---

## Objective

You’ll build **three small but powerful beginner projects**:

1. Simple Calculator
2. Unit Converter
3. Looping Through a List of Numbers

Each reinforces **core Python flow control** and **data handling** you’ve learned so far.

---

## Project 1: Simple Calculator

---

### Step 1: Problem Breakdown

We need to:

* Ask the user for two numbers
* Ask for an operation (`+`, `-`, `*`, `/`)
* Perform the calculation
* Show the result

This means:
You’ll use **input()**, **float()**, **if-elif-else**, and **print()**.

---

###  Step 2: Code It

```python
Hint: Try not to use ChatGPT, any LLM or agent. The goal is to think and build on what you have learnt
```

---

### Example Run

```
Enter first number: 20
Enter operation (+, -, *, /): /
Enter second number: 4
Result: 5.0
```

---

### 💡 Challenge:

* Add **power (^)** and **modulus (%)** support
* Add a **loop** so it runs until the user types “exit”

---

### Quick Quiz

**Q:** What happens if you don’t convert input to `float()`?
**A)** It throws an error
**B)** It concatenates as text 
**C)** It crashes the program


---

## Project 2: Unit Converter

---

### Step 1: Problem Breakdown

Let’s convert:

* Kilometers ↔ Miles
* Celsius ↔ Fahrenheit

You’ll use:

* **Conditionals** to choose conversion type
* **Formulas** to calculate conversion
* **Loops** to make it continuous

---

### Step 2: Conversion Formulas

| Conversion | Formula                 |
| ---------- | ----------------------- |
| km → miles | `miles = km * 0.621371` |
| miles → km | `km = miles / 0.621371` |
| °C → °F    | `F = (C * 9/5) + 32`    |
| °F → °C    | `C = (F - 32) * 5/9`    |

---

### 🧱 Step 3: Code It

```python
Hint: Just in case you ignored me, try not to use ChatGPT, any LLM or agent. The goal is to think and build on what you have learnt
```

---

### Challenge:

Add:

* **Weight (kg ↔ lbs)**
* **Currency conversion (₦ ↔ $)** — simulate rate with a constant variable
* **Color-coded output** using `colorama` module

---

### Quick Quiz

**Q:** Which structure ensures the program keeps running until you exit?
**A)** if-else
**B)** for loop
**C)** while loop 


---

## 🔁 Project 3: Looping Through a List of Numbers

---

###  Objective

Generate a list of numbers
Print the numbers
print only the even numbers
Calculate total and average
Find the max and min
---

### 🧱 Step 1: Code It

```python

Hint: I'll remind you the last time, try not to use ChatGPT, any LLM or agent. The goal is to think and build on what you have learnt
```

---

### 🔍 Output Example

```
numbers = 12, 7, 9, 20, 33, 42, 56, 2
Even numbers:
12
20
42
56

Total = 181, Average = 22.63
Max = 56, Min = 2
```

---

### Challenge:

1. Square every number in the list and store it in a new list.
2. Create a dictionary mapping each number → its square.
3. Find and print all numbers divisible by 3.

---

###  Quiz Time

**Q1:** Which function returns total sum?
**A)** `sum()`
**B)** `add()`
**C)** `sum_list()`

**Q2:** What does `len(numbers)` do?
**A)** Gives largest number
**B)** Gives number of items 
**C)** Gives list average

---

## 🏁 Final Challenge — Combine All Three

Create one notebook called **“Python Basics Final Challenge.ipynb”**, where:

* The user picks a mode: `calculator`, `converter`, or `analyzer`
* Depending on the mode, one of the three programs runs
* Each mode loops until the user chooses to exit

💡 *This simulates a real CLI-based mini-tool — perfect for your GitHub repo.*

---
