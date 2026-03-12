Below is a **clear structure you can use for a report** about **Version Control (Git & GitHub)** focusing on **Git Reset** and **Git Tags**. You can copy this directly into **Word / PDF** and expand it if needed.

---

# Version Control Using Git & GitHub

## Reset and Tags

## 1. Introduction to Version Control

Version Control Systems (VCS) are tools used to track changes in files and coordinate work among multiple developers. They allow developers to keep a history of modifications, revert to previous versions, and collaborate efficiently.

One of the most widely used version control systems is **Git**, which is a distributed version control system. Developers use platforms like **GitHub** to host Git repositories and collaborate with teams.

Git provides many powerful features, including **reset** for undoing changes and **tags** for marking important versions.

---

# 2. Git Reset

## 2.1 What is Git Reset?

`git reset` is a command used to **undo commits or move the repository back to a previous state**.
It allows developers to modify the commit history by moving the **HEAD pointer** to another commit.

Git reset affects three areas:

1. **HEAD** – pointer to the current commit
2. **Staging Area (Index)** – files prepared for commit
3. **Working Directory** – actual files in the project

---

## 2.2 Types of Git Reset

### 1. Soft Reset

The **soft reset** moves the HEAD pointer to a previous commit but keeps changes in the staging area.

Command:

```bash
git reset --soft <commit-id>
```

Behavior:

* Moves HEAD
* Keeps changes staged
* Useful when you want to redo the last commit

Example:

```bash
git reset --soft HEAD~1
```

This removes the last commit but keeps the changes staged.

---

### 2. Mixed Reset (Default)

This is the **default reset mode**. It moves HEAD and resets the staging area but keeps the working directory unchanged.

Command:

```bash
git reset --mixed <commit-id>
```

Behavior:

* Moves HEAD
* Unstages files
* Keeps file changes in the working directory

Example:

```bash
git reset HEAD~1
```

This removes the last commit and unstages the files.

---

### 3. Hard Reset

Hard reset removes everything including commits, staging area, and working directory changes.

Command:

```bash
git reset --hard <commit-id>
```

Behavior:

* Moves HEAD
* Clears staging area
* Deletes all local changes

Example:

```bash
git reset --hard HEAD~1
```

This deletes the last commit and all its changes permanently.

⚠ Warning: Hard reset can permanently delete work if not used carefully.

---

## 2.3 When to Use Git Reset

Git reset is commonly used when:

* Undoing the last commit
* Fixing a wrong commit message
* Removing commits before pushing to remote repositories
* Cleaning the staging area

---

# 3. Git Tags

## 3.1 What are Git Tags?

Git tags are used to **mark specific points in a repository's history**, usually to represent important versions such as releases.

For example:

* Version 1.0
* Version 2.0
* Stable releases

Tags help developers easily identify and return to important versions of the project.

---

## 3.2 Types of Git Tags

### 1. Lightweight Tags

A lightweight tag is simply a reference to a commit.

Command:

```bash
git tag v1.0
```

Characteristics:

* Just a pointer to a commit
* No extra information stored

---

### 2. Annotated Tags

Annotated tags store additional information such as:

* Tagger name
* Email
* Date
* Message

Command:

```bash
git tag -a v1.0 -m "First stable release"
```

Annotated tags are recommended for official releases.

---

## 3.3 Viewing Tags

List all tags:

```bash
git tag
```

View tag details:

```bash
git show v1.0
```

---

## 3.4 Tagging Previous Commits

You can add a tag to an older commit using the commit ID.

```bash
git tag -a v1.0 <commit-id>
```

---

## 3.5 Pushing Tags to GitHub

Tags are not pushed automatically with commits.
You must push them manually.

Push a specific tag:

```bash
git push origin v1.0
```

Push all tags:

```bash
git push origin --tags
```

---

# 4. Importance of Reset and Tags

Both features are important in Git workflows:

| Feature | Purpose                          |
| ------- | -------------------------------- |
| Reset   | Undo or modify commit history    |
| Tags    | Mark important versions/releases |

Developers often use **tags to mark releases** and **reset to fix mistakes before sharing code**.

---

# 5. Conclusion

Git provides powerful tools to manage project history efficiently.
The **reset command** helps developers undo or adjust commits, while **tags** allow teams to mark important versions of their software.

Understanding these features improves project management, collaboration, and release tracking in modern software development.

---

✅ If you want, I can also help you:

* Turn this into a **well-formatted Word report (with headings, table of contents, and screenshots)**
* Add **GitHub practical examples with images** (which usually makes the report look much better).
