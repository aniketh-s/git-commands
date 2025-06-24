
---

## 🧠 What Is a Commit?

A **commit** in Git is a snapshot of your changes. It saves the current state of your working directory (tracked files) and records a message describing what changed.

---

## 🔹 1. **Basic Commit**

### Command:

```bash
git commit -m "Your commit message"
```

### Example:

```bash
git commit -m "Added login feature"
```

Creates a commit with a message.

---

## 🔹 2. **Commit All Tracked Files**

### Command:

```bash
git add .
git commit -m "Message"
```

Or:

```bash
git commit -a -m "Message"
```

### Example:

```bash
git commit -a -m "Fixed typo in home page"
```

Commits all modified (already tracked) files, skipping `git add`.

---

## 🔹 3. **Commit Specific File**

### Command:

```bash
git add filename
git commit -m "Message"
```

### Example:

```bash
git add index.html
git commit -m "Updated hero section"
```

---

## 🔹 4. **Amend Last Commit**

### Command:

```bash
git commit --amend
```

### Example:

```bash
git commit --amend -m "Corrected commit message"
```

Useful if you forgot to include a file or want to edit the last commit message.

---

## 🔹 5. **Empty Commit (No Changes)**

### Command:

```bash
git commit --allow-empty -m "Trigger build"
```

Creates a commit with no changes — useful for triggering CI/CD or tagging.

---

## 🔹 6. **Commit with Date**

### Command:

```bash
GIT_COMMITTER_DATE="2024-01-01T12:00:00" git commit --date "2024-01-01T12:00:00" -m "Backdated commit"
```

---

## 🔹 7. **View Commit History**

### Command:

```bash
git log
```

Other useful formats:

```bash
git log --oneline
git log --graph --all --decorate
```

---

## 🔹 8. **View a Specific Commit**

### Command:

```bash
git show <commit-hash>
```

### Example:

```bash
git show a1b2c3d
```

---

## 🔹 9. **Revert a Commit**

### Command:

```bash
git revert <commit-hash>
```

### Example:

```bash
git revert 12ab34cd
```

Creates a new commit that undoes the changes from the specified commit.

---

## 🔹 10. **Reset to a Previous Commit**

### Command:

```bash
git reset --hard <commit-hash>
```

### Example:

```bash
git reset --hard a1b2c3d4
```

⚠️ This **deletes commits** after that point from local history. Use with care.

For a soft reset (keep changes in working directory):

```bash
git reset --soft <commit-hash>
```

---

## 🔹 11. **Cherry-pick a Commit**

### Command:

```bash
git cherry-pick <commit-hash>
```

### Example:

```bash
git cherry-pick 3f9a7b2
```

Applies a specific commit from another branch.

---

## 🔹 12. **Interactive Rebase (Edit Commits)**

### Command:

```bash
git rebase -i HEAD~<number>
```

### Example:

```bash
git rebase -i HEAD~3
```

Interactively edit, squash, or reorder the last 3 commits.

---

## 🔹 13. **Tag a Commit**

### Command:

```bash
git tag -a v1.0 -m "Version 1.0" <commit-hash>
```

Or:

```bash
git tag v1.0
```

Tags the latest commit with a label like `v1.0`.

---

## 🔹 14. **View Commit Differences**

### Command:

```bash
git diff <commit1> <commit2>
```

### Example:

```bash
git diff HEAD~1 HEAD
```

Shows changes between the last commit and the one before.

---

## 🔹 Summary Table

|Task|Command Example|
|---|---|
|Basic commit|`git commit -m "message"`|
|Commit tracked changes|`git commit -a -m "message"`|
|Commit specific file|`git add file && git commit -m "message"`|
|Amend last commit|`git commit --amend -m "new message"`|
|Empty commit|`git commit --allow-empty -m "CI trigger"`|
|View history|`git log --oneline`|
|View full commit|`git show <hash>`|
|Revert commit|`git revert <hash>`|
|Reset to previous commit|`git reset --hard <hash>`|
|Soft reset|`git reset --soft <hash>`|
|Cherry-pick commit|`git cherry-pick <hash>`|
|Interactive rebase|`git rebase -i HEAD~3`|
|Tag a commit|`git tag -a v1.0 -m "Version 1.0"`|
|Diff between commits|`git diff HEAD~1 HEAD`|

---

Would you like a visual cheat sheet (image/PDF), or want to try these in a practice repo?