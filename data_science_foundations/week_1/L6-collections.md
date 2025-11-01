# Lesson 6: Collections (Lists, Tuples, Sets, Dictionaries)

---

## Objective

By the end of this lesson, you should:

* Know the **4 main collection types** in Python.
* Understand **when to use each** (list, tuple, set, dict).
* Be able to **create, modify, and iterate** through them.
* Write simple programs that use them efficiently.

---

## 1. Lists — The All-Purpose Workhorse 

### What is a List?

A **list** is an ordered, mutable collection of items.

Think of it like a **dynamic shelf** — you can rearrange, replace, or add things anytime.

```python
fruits = ["apple", "banana", "mango"]
print(fruits)
```

**Output:**

```
['apple', 'banana', 'mango']
```

---

### Key Features:

* Ordered ✅
* Mutable (can be changed) ✅
* Allows duplicates ✅

---

### Common Operations

| Operation   | Example                    | Explanation            |
| ----------- | -------------------------- | ---------------------- |
| Add item    | `fruits.append("orange")`  | Adds to the end        |
| Insert item | `fruits.insert(1, "kiwi")` | Adds at specific index |
| Remove item | `fruits.remove("banana")`  | Removes by value       |
| Pop item    | `fruits.pop()`             | Removes last item      |
| Access item | `fruits[0]`                | Access by index        |
| Slice       | `fruits[1:3]`              | Access sub-list        |
| Loop        | `for f in fruits:`         | Iterate over list      |

---

### 💡 Pro Tip:

Lists are your go-to for **sequences of similar data** — e.g. sensor readings, student scores, or file names.

---

### Quick Challenge

```python
numbers = [10, 20, 30, 40]
# Add 50 to the list
# Remove 20
# Print the sum of all numbers in the list
```

---

## 2. Tuples — The Locked Box 

### What is a Tuple?

A **tuple** is an ordered, *immutable* collection. Once created, it **cannot change**.

```python
coordinates = (10.5, 20.7)
print(coordinates)
```

---

### Key Features:

* Ordered ✅
* Immutable ❌
* Allows duplicates ✅

---

### 💡 Use Case:

Tuples are best when data **shouldn’t be changed**, like:

* GPS coordinates
* Database record keys
* RGB color values

---

### Example:

```python
student = ("John", 24, "Engineering")
print(student[0])  # 'John'
```

---

### Quiz:

**Q:** What happens if you try to do this?

```python
coordinates[0] = 15.5
```

**A)** Changes first value
**B)** Creates a new tuple
**C)** Throws an error ✅


---

## 3. Sets — The Unique Club 🏛️

### What is a Set?

A **set** is an unordered collection of **unique** items.

```python
unique_ids = {101, 102, 103, 101}
print(unique_ids)
```

**Output:**

```
{101, 102, 103}
```

---

### ✅ Key Features:

* Unordered ❌
* Mutable ✅
* No duplicates ✅

---

### Common Operations

| Operation    | Example                  |       |
| ------------ | ------------------------ | ----- |
| Add item     | `unique_ids.add(104)`    |       |
| Remove item  | `unique_ids.remove(102)` |       |
| Union        | `set1                    | set2` |
| Intersection | `set1 & set2`            |       |
| Difference   | `set1 - set2`            |       |

---

### 💡 Use Case:

Use sets when you care about **membership** and **uniqueness** — like:

* Unique visitors on a website
* Unique error codes in logs

---

### Challenge

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}
# Find common elements
# Find elements in a but not in b
# Find union of both sets
```

---

## 4. Dictionaries — The Key-Value Engine 🔑

### What is a Dictionary?

A **dictionary** stores data in **key-value pairs**.

```python
person = {
    "name": "Ada",
    "age": 29,
    "city": "Lagos"
}
```

**Accessing:**

```python
print(person["name"])  # Ada
```

---

### Key Features:

* Unordered (Python 3.7+ preserves order by insertion) ✅
* Mutable ✅
* No duplicate keys ✅

---

### Common Operations

| Operation  | Example                                               |
| ---------- | ----------------------------------------------------- |
| Access     | `person["age"]`                                       |
| Add/Update | `person["email"] = "ada@mail.com"`                    |
| Remove     | `person.pop("city")`                                  |
| Loop       | `for key, value in person.items(): print(key, value)` |

---

### 💡 Use Case:

Use dictionaries when you need **mapping** — e.g.:

* Sensor → value
* Student → score
* Config → parameter

---

### Challenge

```python
scores = {
    "John": 85,
    "Mary": 90,
    "Paul": 78
}
# Add "Lucy": 95
# Change "Paul" score to 80
# Print all student names with scores above 80
```

---

## When to Use Each

| Type      | Ordered | Mutable | Duplicates  | Use Case           |
| --------- | ------- | ------- | ----------- | ------------------ |
| **List**  | ✅       | ✅       | ✅           | Sequence of items  |
| **Tuple** | ✅       | ❌       | ✅           | Fixed data         |
| **Set**   | ❌       | ✅       | ❌           | Unique items       |
| **Dict**  | ✅       | ✅       | Keys unique | Key-value mappings |

---

## Quiz Time (Final Review)

1️⃣ Which collection automatically removes duplicates?
**A)** List
**B)** Set ✅
**C)** Tuple
**D)** Dict

2️⃣ Which collection is immutable?
**A)** List
**B)** Set
**C)** Tuple ✅
**D)** Dict

3️⃣ Which collection lets you use key-value pairs?
**A)** Dict ✅
**B)** List
**C)** Tuple
**D)** Set

---

## 🏁 Final Project for This Lesson

### Build a “Student Record System”

**Task:**
Create a dictionary where:

* Each student name is a key.
* The value is a dictionary containing `age`, `department`, and `scores` (a list).

Perform:

1. Add new student records.
2. Print all students in a loop.
3. Print average score for each student.
4. Show department-wise average score.

**Hint:**
Use loops and dictionary methods (`.items()`, `.values()`).
