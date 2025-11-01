Excellent. Let’s continue —
Here’s **Lesson 2: Variables and Data Types**, written in the same **Kaggle-style interactive format** — practical, visual, and hands-on.

---

## LESSON 2: Variables and Data Types (int, float, str, bool)

---

### What You’ll Learn

By the end of this lesson, you’ll be able to:

* Understand what a **variable** really is in Python.
* Declare and use variables properly.
* Identify and use Python’s **four primitive data types**: `int`, `float`, `str`, `bool`.
* Perform type conversions and avoid common pitfalls.

---

###  1. What Is a Variable?

Think of a **variable** as a *container* that stores data in memory.

**Example:**

```python
age = 25
name = "Emmanuel"
height = 1.78
is_student = True
```

 **Behind the scenes:**
Python stores these values in memory and tags them with the variable names.
So whenever you call `name`, Python fetches `"Emmanuel"` from memory.

---

###  2. Variable Naming Rules

✅ Valid:

```python
user_name = "Ahmed"
userAge = 25
height_in_m = 1.75
```

❌ Invalid:

```python
2name = "Bianca"       # starts with a number ❌
my-name = "Samson"     # hyphens not allowed ❌
class = "student"  # reserved keyword ❌
```

💡 **Tips:**

* Use **snake_case** for variable names: `user_age`, `account_balance`
* Be descriptive — `temperature_celsius` is clearer than `t`

---

### 3. Python’s Core Data Types

Python automatically understands data types. You don’t declare them manually like in C or Java.

---

#### 🔢 Integer (`int`)

Whole numbers — positive, negative, or zero.

```python
age = 25
print(type(age))
```

Output:

```
<class 'int'>
```

---

#### Float (`float`)

Numbers with decimal points.

```python
height = 1.75
pi = 3.14159
print(type(height))
```

Output:

```
<class 'float'>
```

---

#### String (`str`)

Text data inside quotes.

```python
name = "Emmanuel"
print(type(name))
```

Output:

```
<class 'str'>
```

You can use **single** or **double** quotes:

```python
message = 'Hello, Python!'
```

Or **triple quotes** for multi-line text:

```python
bio = """ I love data,
         adn i breathe it."""
```

---

#### Boolean (`bool`)

Represents `True` or `False`.

```python
is_robot = False
is_learning = True
print(type(is_learning))
```

💡 *Booleans come from logic — often used in decisions and loops.*

---

### 4. Type Conversion (Casting)

Convert between types easily:

```python
age = "25"
age = int(age)  # Convert string to integer
print(age + 5)
```

Output:

```
30
```

```python
height = 1.75
print(str(height))  # Convert float to string
```

---

### ⚠️ Common Mistake

Mixing incompatible types:

```python
age = 25
name = "AG"
print(name + age)
```

❌ This throws an error: *TypeError: can only concatenate str (not "int") to str*

✅ Fix:

```python
print(name + str(age))
```

---

### 5. Check a Variable’s Type

Use `type()` to see what Python thinks it is:

```python
a = 10
b = 2.5
c = "Hello"
d = True

print(type(a), type(b), type(c), type(d))
```

---

### QUIZ 1 — Quick Checks

**Q1:** What’s the type of `3.0`?

* A. int
* B. float
* C. str
 

---

**Q2:** Which is a valid variable name?

* A. 3value
* B. user-name
* C. user_name
  ✅ **Answer:** C. user_name

---

**Q3:** What will this print?

```python
age = "20"
print(age + 5)
```

* A. "205"
* B. 25
* C. Error
 

---

### CHALLENGE: “Data Collector”

Create a script that:

1. Asks the user for their **name**, **age**, and **height**.
2. Converts `age` and `height` to numbers.
3. Prints something like:

```
Hello Simeon! You are 25 years old and 1.75 meters tall.
```

💪 *Try to print it in one line using f-strings.*

---

### 🔍 KEY TAKEAWAYS

* Python is **dynamically typed** — you don’t need to declare types.
* Variables store data and can change types easily.
* Learn to check and convert types — it prevents bugs later.
* `type()`, `int()`, `float()`, `str()`, and `bool()` are your friends.

---
