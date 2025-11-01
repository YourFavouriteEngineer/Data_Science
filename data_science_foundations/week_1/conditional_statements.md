##  LESSON 4: Conditional Statements (`if`, `elif`, `else`)

---

### What You’ll Learn

By the end of this lesson, you’ll be able to:

* Write decision-making code using `if`, `elif`, and `else`.
* Understand indentation, conditions, and flow control.
* Combine conditions logically.
* Build real-world logic like grading systems or access control.

---

### 1. Why Conditional Statements?

Every program eventually needs to **make decisions**.

Think of it as your code asking:

> “Should I do this or that?”

Python uses **if statements** to let your code *branch* depending on conditions.

---

###  2. Basic `if` Statement

**Syntax:**

```python
if condition:
    # code runs if condition is True
```

**Example:**

```python
temperature = 35

if temperature > 30:
    print("It's a hot day!")
```

 Output:

```
It's a hot day!
```

💡 *Notice the colon (`:`) and indentation. That indentation is how Python groups code blocks.*

---

### 3. `if-else` — Two-Way Decision

**Syntax:**

```python
if condition:
    # if True
else:
    # if False
```

**Example:**

```python
is_raining = False

if is_raining:
    print("Take an umbrella.")
else:
    print("Enjoy the sunshine!")
```

 Output:

```
Enjoy the sunshine!
```

---

### 4. `if-elif-else` — Multiple Conditions

**Syntax:**

```python
if condition1:
    # if True
elif condition2:
    # if True
else:
    # if all above False
```

**Example:**

```python
score = 75

if score >= 80:
    print("Excellent")
elif score >= 60:
    print("Good")
else:
    print("Needs Improvement")
```

Output:

```
Good
```

💡 *`elif` means “else if” — Python checks conditions in order, top to bottom.*

---

###  5. Nested Conditions

You can put an `if` inside another `if`.

**Example:**

```python
age = 20
has_id = True

if age >= 18:
    if has_id:
        print("Access granted.")
    else:
        print("Please bring your ID.")
else:
    print("You must be at least 18.")
```

 Output:

```
Access granted.
```

💡 *Keep nesting clean — too many nested `ifs` can make code messy.*

---

###  6. Combining Conditions

You can merge logic using `and`, `or`, and `not`.

**Example:**

```python
age = 22
is_student = False

if age < 18:
    print("Minor")
elif age >= 18 and is_student:
    print("Adult student")
else:
    print("Adult non-student")
```

Output:

```
Adult non-student
```

---

### ⚠️ 7. Indentation and Scope

Python uses indentation to define **which code belongs where**.
You *must* indent consistently (usually 4 spaces).

❌ Wrong:

```python
if True:
print("Hello")  # IndentationError
```

✅ Correct:

```python
if True:
    print("Hello")
```

---

###  QUIZ — Think Like Python

**Q1:**
What happens here?

```python
x = 10
if x > 5:
    print("A")
if x > 8:
    print("B")
```

---

**Q2:**
What prints?

```python
x = 10
if x > 5:
    print("A")
elif x > 8:
    print("B")
```

---

**Q3:**
Which is valid syntax?

* A. `if x > 5 then:`
* B. `if (x > 5):`
* C. `if x > 5:`
 
---

### Challenge: “Smart Login System”

Create a program that:

1. Asks for a username and password.
2. If both match your preset credentials (`admin`, `1234`), print `"Access Granted"`.
3. If username is correct but password is wrong → `"Wrong Password"`.
4. If username is wrong → `"User not found"`.

💪 *Use `if`, `elif`, and `else` cleanly.*

---

###  Bonus Challenge: “Weather Bot”

Ask the user for temperature:

* If > 30 → `"It's hot."`
* If 20–30 → `"It's warm."`
* If 10–19 → `"It's cool."`
* Else → `"It's cold."`

💡 *Think logically — your conditions must not overlap.*

---

### 🔍 KEY TAKEAWAYS

* `if`, `elif`, `else` let your code make decisions.
* Python checks conditions *top to bottom* and stops when one is True.
* Indentation defines structure — no curly braces.
* Use `and`, `or`, `not` to combine logic.
* Always test your conditions with print statements.
