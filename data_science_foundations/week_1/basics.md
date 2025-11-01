

---

## LESSON 1: Running Python (Interpreter, Script, Notebook)

---

### What You’ll Learn

By the end of this lesson, you’ll be able to:

* Run Python code using **three environments**: Interpreter, Script, and Jupyter Notebook.
* Understand **when and why** to use each.
* Debug and test small code snippets efficiently.

---

### 1. The Python Interpreter

The **interpreter** runs Python *line by line*, directly from your terminal or command prompt.

**Try this:**

```bash
python
```

You’ll see something like:

```
Python 3.12.1 (default, ...)
>>> 
```

The `>>>` means Python is waiting for you to type something.

**Now type:**

```python
print("Hello, Python!")
```

Output:

```
Hello, Python!
```

 *Think of the interpreter as your quick calculator or testing pad.*

**Why use it?**

* Fast feedback.
* Ideal for testing small code snippets or debugging.
* Perfect when experimenting interactively.

---

### 2. Python Script (.py file)

When you want to **save and run** multiple lines of code (like a program or project), use a **script**.

**Example:**
Create a file called `hello.py` and add:

```python
print("Hello, World!")
name = input("What’s your name? ")
print(f"Welcome, {name}!")
```

Then run it from your terminal:

```bash
python hello.py
```

Output:

```
Hello, World!
What’s your name? "whatever your input was"
Welcome, "whatever your input was"!
```

 *Scripts are reusable, and you can modify and rerun them without retyping everything.*

---

###  3. Jupyter Notebook / Kaggle Notebook

This is where **learning meets interactivity**.
You can write code, run it, and document your thoughts — all in one place.

Run this inside a Jupyter cell or Kaggle cell:

```python
print("Welcome to Jupyter!")
```

Then add a **Markdown cell** (click "+ Text" in Kaggle):

```
### Why Jupyter?
- Ideal for learning, data exploration, and tutorials.
- Lets you mix code, output, and explanation.
```

 *Data scientists and AI engineers use notebooks daily for analysis and prototyping.*

---

### ⚙️ Quick Comparison

| Mode        | Best For                | How to Run         | Persistence       |
| ----------- | ----------------------- | ------------------ | ----------------- |
| Interpreter | Quick tests             | `python`           | Lost after exit   |
| Script      | Reusable code           | `python script.py` | Saved as file     |
| Notebook    | Learning, data analysis | Jupyter/Kaggle     | Saved as notebook |

---

###  QUIZ 1 — Spot the Right Tool

**Question 1:**
You want to quickly test if `5 + 3 * 2` gives 11. Which environment is best?

* A. Script
* B. Interpreter
* C. Jupyter Notebook


---

**Question 2:**
You’re writing a 200-line Python project. Which is ideal?

* A. Interpreter
* B. Script
* C. Notebook



---

**Question 3:**
You want to mix code, explanations, and charts. Which environment fits best?

* A. Interpreter
* B. Script
* C. Notebook



---

### Challenge: “Three Ways to Say Hello”

Create a `hello_world` program that:

1. Prints your name using the interpreter.
2. Runs as a script (`hello.py`).
3. Displays a welcome message inside a Jupyter cell.

*Goal:* Experience all three execution methods hands-on.

---

### 🔍 Key Takeaways

* **Interpreter** → Instant testing.
* **Script** → Saved, reusable programs.
* **Notebook** → Interactive exploration and documentation.

Mastering how to *run* Python properly saves time and makes debugging easier.

---


