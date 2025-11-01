## LESSON 3: Operators (Arithmetic, Comparison, Logical)

---

### What You’ll Learn

By the end of this lesson, you’ll be able to:

* Perform calculations using **arithmetic operators**.
* Compare values using **comparison operators**.
* Combine logic using **logical operators** (`and`, `or`, `not`).
* Understand operator *precedence* and how Python evaluates expressions.

---

### 1. What Are Operators?

Operators are **symbols** or **keywords** that perform operations on values (operands).

Think of them as the verbs of Python’s language.

---

## 🔹 A. Arithmetic Operators

| Operator | Meaning             | Example   | Result |
| -------- | ------------------- | --------- | ------ |
| `+`      | Addition            | `5 + 3`   | `8`    |
| `-`      | Subtraction         | `9 - 4`   | `5`    |
| `*`      | Multiplication      | `2 * 3`   | `6`    |
| `/`      | Division            | `10 / 4`  | `2.5`  |
| `//`     | Floor Division      | `10 // 4` | `2`    |
| `%`      | Modulus (Remainder) | `10 % 4`  | `2`    |
| `**`     | Exponentiation      | `2 ** 3`  | `8`    |

**Try this:**

```python
a, b = 15, 4
print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Floor Division:", a // b)
print("Modulus:", a % b)
print("Exponentiation:", a ** b)
```

💡 *`//` and `%` are extremely useful in loops, modular arithmetic, and index operations.*

---

### Mini Exercise: “Last Digit Finder”

Use modulus to get the **last digit** of a number:

```python
num = 2597
print(num % 10)  # Output: 7
```

Can you modify it to get the *second to last digit*?

---

## 🔹 B. Comparison Operators

Comparison operators always return a **Boolean** (`True` or `False`).

| Operator | Meaning          | Example  | Result  |
| -------- | ---------------- | -------- | ------- |
| `==`     | Equal to         | `5 == 5` | `True`  |
| `!=`     | Not equal to     | `3 != 2` | `True`  |
| `>`      | Greater than     | `7 > 3`  | `True`  |
| `<`      | Less than        | `2 < 9`  | `True`  |
| `>=`     | Greater or equal | `7 >= 7` | `True`  |
| `<=`     | Less or equal    | `3 <= 2` | `False` |

**Try it:**

```python
x, y = 10, 5
print(x == y)
print(x != y)
print(x > y)
print(x <= y)
```

💡 *Comparison operators are the foundation for conditionals (`if`, `else`) and loops.*

---

### ⚠️ Beware of `=` vs `==`

* `=` → assignment (`x = 10`)
* `==` → comparison (`x == 10`)

They look similar, but their purposes are *completely different.*

---

## 🔹 C. Logical Operators

Combine conditions for more complex logic.

| Operator | Meaning                      | Example              | Result  |
| -------- | ---------------------------- | -------------------- | ------- |
| `and`    | True if both are True        | `(5 > 2 and 10 > 3)` | `True`  |
| `or`     | True if at least one is True | `(5 > 10 or 3 < 5)`  | `True`  |
| `not`    | Negates the condition        | `not (5 > 3)`        | `False` |

**Try this:**

```python
x = 7
print(x > 5 and x < 10)  # True
print(x < 5 or x == 7)   # True
print(not (x == 7))      # False
```

---

### 🔍 Operator Precedence (Execution Order)

When multiple operators are combined, Python follows a priority order.

| Priority | Operator                           |
| -------- | ---------------------------------- |
| 1        | `()` Parentheses                   |
| 2        | `**` Exponent                      |
| 3        | `*`, `/`, `//`, `%`                |
| 4        | `+`, `-`                           |
| 5        | Comparisons (`==`, `<`, `>`, etc.) |
| 6        | Logical (`not`, `and`, `or`)       |

**Example:**

```python
result = 5 + 2 * 3 > 10 and not False
# Step 1: 2 * 3 → 6
# Step 2: 5 + 6 → 11
# Step 3: 11 > 10 → True
# Step 4: True and not False → True
print(result)
```

✅ Output: `True`

💡 *When unsure, use parentheses to make your logic explicit.*

---

###  QUIZ — Think Fast

**Q1:**
What’s the output?

```python
print(10 // 3)
```

* A. 3.33
* B. 3
* C. 4

---

**Q2:**
What does this return?

```python
5 > 2 and 10 < 8
```

* A. True
* B. False

---

**Q3:**
What’s printed?

```python
not (3 == 3 or 2 > 5)
```

---

### CHALLENGE: “Smart Grader”

Write a small script that:

1. Asks for a student’s score (0–100).
2. Checks and prints:

   * `"Excellent"` if score ≥ 80
   * `"Good"` if 60 ≤ score < 80
   * `"Needs Improvement"` otherwise
3. Uses **comparison** and **logical** operators.

Try running it interactively, then modify it into a script file.

---

### 🔍 KEY TAKEAWAYS

* **Arithmetic** handles math.
* **Comparison** checks conditions.
* **Logical** combines conditions for decisions.
* Operator **precedence** controls order — use parentheses to clarify.

---

