# Lesson 1: Functions, Scope & Reusability

---

## Objective

By the end of this lesson, learners should:

* Understand what functions are and why they exist
* Know how to define, call, and return values from functions
* Understand local vs global scope
* Learn how to write reusable, modular code

---

## 1. What is a Function?

A **function** is a *named block of code* that performs a specific task.

It’s like creating your **own custom command** that can be reused anytime.

---

### Real-World Analogy:

Think of a function as a **machine** in a factory:

* You send it *inputs* (materials)
* It performs *a process*
* It gives you *outputs* (finished products)

---

### Example:

```python
def greet():
    print("Hello, welcome to Python!")
```

To *run* (call) the function:

```python
greet()
```

**Output:**

```
Hello, welcome to Python!
```

---

## 2. Function Structure

```
def function_name(parameters):
    # Code block
    return result
```

### Example:

```python
def add_numbers(a, b):
    result = a + b
    return result

sum_value = add_numbers(5, 10)
print(sum_value)
```

**Output:**

```
15
```

---

## 3. Parameters vs Arguments

| Term          | Meaning                      | Example            |
| ------------- | ---------------------------- | ------------------ |
| **Parameter** | Variable inside the function | `def greet(name):` |
| **Argument**  | Actual value you pass        | `greet("Ada")`     |

---

### Example:

```python
def greet_user(name):
    print(f"Hello, {name}!")

greet_user("John")
greet_user("Mary")
```

**Output:**

```
Hello, John!
Hello, Mary!
```

---

## 4. Default Parameters

You can set default values for parameters.

```python
def greet(name="friend"):
    print(f"Hello, {name}!")

greet()        # Hello, friend!
greet("AG")    # Hello, AG!
```

---

## 5. Return Statement

The `return` keyword sends a value *back* to where the function was called.

```python
def square(x):
    return x ** 2

print(square(4))  # 16
```

Without `return`, the function only prints — it doesn’t “hand back” a value.

---

### Quick Quiz

What’s the difference between `print()` and `return` inside a function?

**A)** `print` outputs to screen, `return` sends data back 
**B)** `print` stores data, `return` displays it
**C)** Both are same

---

## 6. Scope: Where Variables Live

Scope defines *where a variable can be accessed.*

There are **two main types**:

* **Local scope** → Inside a function
* **Global scope** → Outside all functions

---

### Example:

```python
x = 10  # Global variable

def my_function():
    y = 5  # Local variable
    print("Inside function:", x, y)

my_function()
print("Outside function:", x)
# print(y) ❌ ERROR: y is local
```

---

### Rule of Thumb:

> Variables created inside a function are **temporary** and die when the function ends.

---

## 7. Modifying Global Variables

If you really need to modify a global variable from inside a function, use `global`.

```python
count = 0

def increment():
    global count
    count += 1

increment()
increment()
print(count)  # 2
```

But in clean code, avoid this when possible. Prefer **returning** values instead.

---

## 8. Why Functions Matter: Reusability

Imagine writing a data analysis script that needs to calculate averages in 10 different places.

Without functions:

```python
numbers = [10, 20, 30, 40]
average = sum(numbers) / len(numbers)
```

With a function:

```python
def average(numbers):
    return sum(numbers) / len(numbers)

scores = [70, 80, 90]
temps = [25, 30, 35]

print(average(scores))
print(average(temps))
```

**Less code, fewer errors, more clarity.**

---

## 9. Real-World Example: Grading System

```python
def calculate_grade(score):
    if score >= 70:
        return "A"
    elif score >= 60:
        return "B"
    elif score >= 50:
        return "C"
    else:
        return "F"

student_scores = [72, 65, 48, 90]

for s in student_scores:
    print(f"Score: {s} → Grade: {calculate_grade(s)}")
```

---

## 10. Challenge Tasks

1️⃣ Write a function `is_even(num)` that returns `True` if a number is even.
2️⃣ Write a function `factorial(n)` using a loop.
3️⃣ Write a function `reverse_string(s)` that returns the reversed text.
4️⃣ Write a function `count_vowels(s)` that counts vowels in a string.
5️⃣ (Advanced) Write a function `fibonacci(n)` that prints the first *n* Fibonacci numbers.

---

## Final Quiz

1️⃣ What is a function?

2️⃣ What happens if a function doesn’t have a `return`?

3️⃣ What’s the difference between global and local scope?
---

## Mini Project: Modular Temperature Analyser

Create a program that:

1. Has a function to convert Celsius → Fahrenheit
2. Another to convert Fahrenheit → Celsius
3. Another way to determine if the temperature is “Cold”, “Warm”, or “Hot”
4. A main function that asks the user for a choice and prints the results

---

 *Hint:*
Structure it like this:

```python
def c_to_f(c): ...
def f_to_c(f): ...
def classify_temp(temp, scale): ...
def main(): ...
```

Call `main()` at the bottom.
