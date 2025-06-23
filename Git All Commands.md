- Initiating a Git repo

```bash
git init
```
This creates a .git folder containing all the metadata such as branches, hooks etc.

- Adding a file to staging area

```bash
git add file_name
```

- Committing changes

```bash
git commit -m "message"
```

For multiline comments

```bash
git commit
# This opens the default editor where we can add large messages
```

Skipping the staging area

```bash

git commit -a -m "message"
```

View files in staging area

```bash
git ls-files
```

Removing a file

```bash
git rm file_name
```

Renaming a file

```bash
git mv old_name new_name
```

