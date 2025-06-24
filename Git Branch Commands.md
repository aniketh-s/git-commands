
---

## 🧠 `git branch` – Overview

This command is used to **create, list, rename, and delete branches**.

---

## 🔹 1. **List All Branches**

### Command:

```bash
git branch
```

### Description:

Shows all local branches in the repo. The current branch will be highlighted with an asterisk `*`.

### Example:

```
* main
  feature-login
  bugfix-crash
```

To list **remote branches**:

```bash
git branch -r
```

To list **all (local + remote)**:

```bash
git branch -a
```

---

## 🔹 2. **Create a New Branch**

### Command:

```bash
git branch <branch-name>
```

### Example:

```bash
git branch feature-login
```

Creates a new branch called `feature-login`, but does **not switch** to it.

---

## 🔹 3. **Switch to a Branch**

### Command:

```bash
git checkout <branch-name>
```

### Example:

```bash
git checkout feature-login
```

Switches to the `feature-login` branch.

**Shortcut to create and switch in one command** (Git 2.23+):

```bash
git switch -c <branch-name>
```

---

## 🔹 4. **Create and Switch (Combined)**

### Command:

```bash
git checkout -b <branch-name>
```

### Example:

```bash
git checkout -b feature-payment
```

Creates and switches to the `feature-payment` branch in one step.

---

## 🔹 5. **Rename a Branch**

### Command:

```bash
git branch -m <new-name>
```

If you’re on the branch you want to rename:

```bash
git branch -m new-name
```

### Example:

```bash
git branch -m feature-authentication
```

Renames current branch to `feature-authentication`.

---

## 🔹 6. **Delete a Branch**

### Command:

```bash
git branch -d <branch-name>
```

### Example:

```bash
git branch -d feature-login
```

Deletes the `feature-login` branch **if it is fully merged**.

To force delete (e.g., not merged):

```bash
git branch -D <branch-name>
```

---

## 🔹 7. **See Last Commit on Each Branch**

### Command:

```bash
git branch -v
```

### Example:

```
* main               9a1bc3a Initial commit
  feature-login      a24edfc Added login form
```

---

## 🔹 8. **Track a Remote Branch Locally**

### Command:

```bash
git checkout -b <branch> origin/<branch>
```

### Example:

```bash
git checkout -b feature-payment origin/feature-payment
```

Creates a local branch tracking a remote one.

Or use:

```bash
git switch --track origin/<branch>
```

---

## 🔹 9. **Set Upstream Tracking (Link Local to Remote)**

### Command:

```bash
git branch --set-upstream-to=origin/<branch> <local-branch>
```

### Example:

```bash
git branch --set-upstream-to=origin/main main
```

---

## 🔹 10. **Merge a Branch into Current**

### Command:

```bash
git merge <branch-name>
```

### Example:

```bash
git merge feature-login
```

Merges `feature-login` into your current branch (like `main`).

---

## 🔹 11. **Rebase a Branch**

### Command:

```bash
git rebase <branch-name>
```

### Example:

```bash
git rebase main
```

Reapplies your current branch's commits on top of `main`.

---

## 🔹 12. **Compare Two Branches**

### Command:

```bash
git diff <branch1>..<branch2>
```

### Example:

```bash
git diff main..feature-login
```

Shows differences between `main` and `feature-login`.

---

## 🔹 13. **Push a Branch to Remote**

### Command:

```bash
git push origin <branch-name>
```

### Example:

```bash
git push origin feature-login
```

To set the upstream the first time:

```bash
git push -u origin feature-login
```

---

## 🔹 14. **Delete a Remote Branch**

### Command:

```bash
git push origin --delete <branch-name>
```

### Example:

```bash
git push origin --delete feature-login
```

---

## 🧭 Summary Table

|Task|Command Example|
|---|---|
|List branches|`git branch`|
|Create branch|`git branch feature-x`|
|Create + switch|`git checkout -b feature-x`|
|Switch branch|`git checkout feature-x`|
|Rename branch|`git branch -m new-name`|
|Delete branch|`git branch -d feature-x`|
|Force delete|`git branch -D feature-x`|
|View last commit|`git branch -v`|
|Track remote|`git checkout -b feature-x origin/feature-x`|
|Set upstream|`git branch --set-upstream-to=origin/x x`|
|Merge branch|`git merge feature-x`|
|Rebase branch|`git rebase main`|
|Push branch|`git push origin feature-x`|
|Delete remote branch|`git push origin --delete feature-x`|

---
##### Delete a GitHub repo branch from git bash
```bash
git push origin --delete master
```

