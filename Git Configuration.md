## ✅ 1. **View all Git configurations**

```bash
git config --list
```

🔹 Shows all settings (user name, email, editor, diff/merge tools, etc.), including system, global, and local.

---

## ✅ 2. **Check a specific configuration value**

```bash
git config --get <key>
```

📝 Examples:

```bash
git config --get core.editor
git config --get user.name
git config --get diff.tool
```

---

## ✅ 3. **See global Git config**

```bash
git config --global --list
```

🔹 Shows settings stored in `~/.gitconfig` (applies to all repos for your user).

---

## ✅ 4. **See local Git config (per repository)**

```bash
git config --local --list
```

🔹 Shows settings stored in `.git/config` (only applies to current repo).

---

## ✅ 5. **See system-wide Git config**

```bash
git config --system --list
```

🔹 Shows settings for all users (may require `sudo`).

---

## 📄 Bonus: View the config file directly

### Global config file:

```bash
code ~/.gitconfig
```

### Local repo config:

```bash
code .git/config
```

> Replace `code` with `notepad`, `vim`, etc., if you're not using VS Code.

---

Let me know if you'd like help interpreting any of your config values!