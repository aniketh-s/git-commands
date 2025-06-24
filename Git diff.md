List of commonly used `git diff` commands with examples to help you understand how to view differences in Git at various stages:

---

## 🔍 Basic `git diff` Commands

### 1. **View unstaged changes (Working Directory vs Index)**

```bash
git diff
```

📝 **Shows changes** you've made but haven't staged with `git add`.

---

### 2. **View changes in a specific file**

```bash
git diff <filename>
```

📝 Example:

```bash
git diff index.html
```

---

### 3. **View staged changes (Index vs Last Commit)**

```bash
git diff --cached
```

or

```bash
git diff --staged
```

📝 Example:

```bash
git diff --cached main.py
```

---

### 4. **View all changes (Working Directory vs Last Commit)**

```bash
git diff HEAD
```

📝 Includes both staged and unstaged changes.

---

### 5. **Compare two commits**

```bash
git diff <commit1> <commit2>
```

📝 Example:

```bash
git diff abc123 def456
```

---

### 6. **Compare commit vs working directory**

```bash
git diff <commit>
```

📝 Example:

```bash
git diff HEAD~1
```

---

### 7. **Compare two branches**

```bash
git diff branch1..branch2
```

📝 Example:

```bash
git diff main..feature-xyz
```

---

### 8. **Compare file changes between commits**

```bash
git diff <commit1> <commit2> -- <filename>
```

📝 Example:

```bash
git diff abc123 def456 -- config.yaml
```

---

## 🛠️ Additional Options

### 9. **Ignore whitespace differences**

```bash
git diff -w
```

### 10. **View only names of changed files**

```bash
git diff --name-only
```

### 11. **View names and status (added, modified, deleted)**

```bash
git diff --name-status
```

---

### 12. **View diff for a particular directory**

```bash
git diff <directory>/
```

📝 Example:

```bash
git diff src/
```

---

### 13. **Color the output**

```bash
git diff --color
```

---

### 14. **View word-by-word difference**

```bash
git diff --word-diff
```

---

## 🧪 Bonus: Diff Against Remote

### 15. **Compare local branch with remote**

```bash
git diff origin/main
```

---

## 🗂 Summary Table

|Command|Compares|Use Case|
|---|---|---|
|`git diff`|Working directory vs Staging|See what’s changed before staging|
|`git diff --cached`|Staging vs Last commit|See what’s about to be committed|
|`git diff HEAD`|Working directory vs Last commit|All current changes|
|`git diff <commit1> <commit2>`|Two commits|View historical changes|
|`git diff <branch1>..<branch2>`|Two branches|See changes between branches|
|`git diff --name-only`|-|File names only|
|`git diff --word-diff`|-|Fine-grained word changes|

---

#### Opening with default editor
```bash
git difftool
```
