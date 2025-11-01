## LESSON 5: Loops (`for`, `while`)

---

### What You’ll Learn

By the end of this lesson, you’ll be able to:

* Write and control **for** and **while** loops.
* Understand how iteration works behind the scenes.
* Use **break**, **continue**, and **range()** effectively.
* Automate repetitive logic cleanly.

---

### 1. What Is a Loop?

A **loop** repeats a block of code multiple times.
Instead of writing the same thing again and again, you let Python do it for you.

💡 *Think of it like a “repeat until done” instruction.*

---

## 🔹 A. The `for` Loop — Iterating Over a Sequence

`for` loops are best when you *know* how many times you need to repeat.

**Syntax:**

```python
for variable in sequence:
    # do something
```

**Example:**

```python
for i in range(5):
    print("Iteration:", i)
```

 Output:

```
Iteration: 0
Iteration: 1
Iteration: 2
Iteration: 3
Iteration: 4
```

💡 `range(5)` generates numbers from **0 to 4** (stop value is excluded).

---

###  Using `range(start, stop, step)`

```python
for i in range(2, 10, 2):
    print(i)
```

Output:

```
2
4
6
8
```

💡 *Perfect for loops that count in steps (e.g., every 2nd or 5th item).*

---

### Looping Through Lists

You can iterate directly over lists, tuples, strings, and sets.

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

Output:

```
apple
banana
cherry
```

💡 *No index math needed — Python handles it for you.*

---

### Enumerate — When You Need Index + Value

```python
fruits = ["apple", "banana", "cherry"]

for index, fruit in enumerate(fruits):
    print(index, fruit)
```

 Output:

```
0 apple
1 banana
2 cherry
```

---

## 🔹 B. The `while` Loop — Repeat Until a Condition Is False

Use `while` when you *don’t know* how many times to loop —
You stop only when a condition changes.

**Example:**

```python
count = 0
while count < 5:
    print("Count:", count)
    count += 1
```

Output:

```
Count: 0
Count: 1
Count: 2
Count: 3
Count: 4
```

💡 *The condition is checked before every iteration.*

---

### ⚠️ Infinite Loops (Be Careful)

If the condition never becomes False → loop runs forever.

```python
while True:
    print("Press Ctrl+C to stop!")  # don't actually run this here 😅
```

Always ensure something inside the loop changes the condition.

---

## 🔹 C. Loop Control Statements

Sometimes you need to **skip**, **stop**, or **restart** inside a loop.

---

### ➤ `break` — Stop the Loop Early

```python
for num in range(10):
    if num == 5:
        break
    print(num)
```
 Output:

```
0
1
2
3
4
```

💡 *Loop exits completely when `num` hits 5.*

---

### ➤ `continue` — Skip This Iteration

```python
for num in range(6):
    if num == 3:
        continue
    print(num)
```
 Output:

```
0
1
2
4
5
```

💡 *Skips only the current iteration and continues.*

---

### ➤ `else` in Loops — Rare but Powerful

Python allows an optional `else` after a loop, which runs **only if** the loop *didn’t break*.

```python
for i in range(5):
    print(i)
else:
    print("Loop completed without break.")
```

If a `break` occurs, the `else` block is skipped.

---

##  QUIZ — Quick Checks

**Q1:**
What does `range(3, 8)` produce?


---

**Q2:**
What will this print?

```python
count = 0
while count < 3:
    print(count)
    count += 1
```


---

**Q3:**
What’s wrong here?

```python
for i in range(5)
    print(i)
```

---

## CHALLENGE 1: “Even Number Finder”

Print all even numbers between 1 and 20 using:

1. `for` + `range()`
2. `while` loop

💪 *Use modulus (`%`) to test for evenness.*

---

## CHALLENGE 2: “Guess the Number Game”

Write a program that:

1. Generates a random number between 1 and 10.
2. Asks the user to guess it.
3. Keeps looping until the user guesses right.
4. Prints how many tries it took.

💡 *Use `import random` and `while True` with `break`.*

---

## CHALLENGE 3: “Multiplication Table”

Ask the user for a number and print its multiplication table (up to 12).

Example:

```
Enter number: 5
5 x 1 = 5
5 x 2 = 10
...
5 x 12 = 60
```

💡 *Perfect way to test nested loops.*

---

### 🔍 KEY TAKEAWAYS

* **for** = when you know how many times.
* **while** = when you don’t know how many times.
* `break` stops loops early, `continue` skips one iteration.
* Be careful with **infinite loops** — always update your condition.
* Use loops to automate repetitive tasks and iterate over collections.

---


