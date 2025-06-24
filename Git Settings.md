### Settings

- Name
- Email
- Default Editor
- Line ending

### Configuration Levels

- System
- Global
- Local

**Specifying Levels**: 
```bash
git config --global user.name="name" #Within double quotes cause of space b/w names
git config --global user.email=email
```

### End of Lines:

![[Git Settings-20250528115132438.png]]

To prevent end of line issues in git, we configure the end of line properly with ```core.autocrlf ``` which stands for **carriage return line feed**

*Carriage Return Line Feed. It's a combination of two control characters used to indicate the end of a line in text and protocols, especially in HTTP.*

![[Git Settings-20250528115611163.png]]


By using core.autocrlf git adds/modifies end of line only when storing any code in the repo.
Setting for **Windows: true**
Setting for **Mac: input**

#### Setting default code editor

---

## 🎯 1. Set VS Code as the **default Git editor**

```bash
git config --global core.editor "code --wait"
```

> ✅ This makes Git open commit messages, rebase instructions, etc., in VS Code.

---

## 🎯 2. Set VS Code as the **default Git difftool**

```bash
git config --global diff.tool vscode
git config --global difftool.vscode.cmd "code --wait --diff \"$LOCAL\" \"$REMOTE\""
git config --global difftool.prompt false
```

> ✅ This opens side-by-side diffs in VS Code when you run `git difftool`.

---

## 🎯 3. (Optional) Set VS Code as the **default Git mergetool**

```bash
git config --global merge.tool vscode
git config --global mergetool.vscode.cmd "code --wait \"$MERGED\""
```

> ✅ This allows you to resolve merge conflicts in VS Code using `git mergetool`.

---

Let me know if you'd like a `.gitconfig` snippet instead or want to undo any of these later.