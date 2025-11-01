# Week 1 – Python Setup & GitHub Intro

### 🎯 Objective
Welcome to your first week!  
You’ll learn how to:
- Install Python and a code editor  
- Write your first Python program  
- Create and upload a project to GitHub  

By the end of this week, you’ll have your **first repository live on GitHub!**

---

## 🧩 Step-by-Step Tasks

---

###  1. Install Your Tools

####  Install Python
1. Go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Download the latest version (≥3.10)
3. During installation, **check the box** that says **“Add Python to PATH”**
4. After installation, open your terminal (or Command Prompt) and type:
   ```bash
   python --version
Here’s your guide rewritten in clean, professional **Markdown (`.md`)** format — perfect for a `README.md` file:

---

#  Getting Started with Python & VS Code

##  1. Verify Python Installation

Open your terminal or command prompt and type:

```bash
python --version
```

You should see something like:

```
Python 3.12.1
```

✅ If you see this — Python is installed successfully.

---

##  2. Install Visual Studio Code (VS Code)

1. Go to [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Download and install **VS Code**
3. Open VS Code and click the **Extensions** icon (square icon on the left sidebar)
4. Search and install the following extensions:

   * **Python** (by Microsoft)
   * **Jupyter** *(optional, for later weeks)*

###  Connect to GitHub

Click the **Settings** section in VS Code and connect your GitHub account.

---

##  3. Write Your First Python Script

### Step 1 — Fork and Clone the Repository

1. Fork this repository
2. Click **Code → Copy the URL**
3. Open **VS Code** → open the **Command Palette** (`Ctrl + Shift + P`)  
→ type **Git: Clone** → paste the link.  
4. Choose where to save the folder and open it when done.

---
### Step 2 — Create a New Python File

In VS Code:

* Click **New File**
* Name it: `hello_datascience.py`

### Step 3 — Add Your First Code

Type the following:

```python
print("Hello, Data Science World!")
print("My name is <Your Name>")
print("I’m excited to start my data science journey.")
```

### Step 4 — Run Your Code

**Option 1:** Click the small ▶️ “Run” button in VS Code
**Option 2:** Open the terminal and type:

```bash
python hello_datascience.py
```

### Expected Output:

```
Hello, Data Science World!
My name is John Doe
I’m excited to start my data science journey.
```

 Congratulations — you’ve just written your first Python program!

---

##  4. Add a Project Description

Create a new file named `README.md`  and write a short description, for example:

```markdown
# My First Step into Data Science

This project marks the beginning of my data science journey.  
It includes my first Python program: `hello_datascience.py`,  
where I print a welcome message to the data science world!
```

## Step 5: Stage and Commit Your Changes

### Option 1 — Using VS Code GUI (easiest)
1. Click the **Source Control** icon (branch symbol) on the left panel.
2. You’ll see a list of changed files.
3. Click the **+** icon beside each file to **stage** it.
4. In the message box at the top, type a short message like:
```

Week 1 – My first Python script

````
5. Click the  **Commit** button.

### Option 2 — Using the Terminal
1. Open the VS Code terminal.
2. Run these commands:

```bash
git add .
git commit -m "Week 1 – My first Python script"
````

✅ This saves your changes locally.

---

##  Step 5: Push Your Changes to GitHub

In VS Code terminal, type:

```bash
git push origin main
```

If it’s your first time pushing, you may be asked to log in.
After that, refresh your GitHub page and your new files will appear.

---

## Step 6: Create a Pull Request (PR)

Now you’ll submit your assignment back to the main repository.

1. Go to your forked repo on GitHub.
2. Click **Contribute → Open Pull Request.**
3. Make sure:

   * **Base repository** → main class repo (e.g., `organisation/data-science-assignments`)
   * **Head repository** → your fork (`your-username/data-science-assignments`)
4. Title your PR like this:

   ```
   Week 1 – <Your Name>
   ```
5. Click **Create Pull Request**

 Your submission is live!
The instructor can now view, review, or comment on your work.

---

##  Step 7: Keep Your Fork Updated

Before starting a new week’s assignment:

1. Go to your forked repo on GitHub.
2. Click the **Sync fork** button → **Update branch**
   (This pulls the latest updates from the main repo).
3. Then clone or pull again locally:

   ```bash
   git pull origin main
   ```

---

## Quick Recap

| Action        | Command / Button          | Purpose                             |
| ------------- | ------------------------- | ----------------------------------- |
| Stage changes | `git add .`               | Prepares files for commit           |
| Commit        | `git commit -m "message"` | Saves changes locally               |
| Push          | `git push origin main`    | Uploads to GitHub                   |
| Create PR     | via GitHub interface      | Submits your assignment             |
| Sync Fork     | "Sync fork" button        | Updates your repo with main changes |

---

 **You’ve mastered the full Git workflow!**
From now on, you’ll use the same process every week to submit your assignments.


**You’re now fully set up to begin your data science journey with Python!**



---




