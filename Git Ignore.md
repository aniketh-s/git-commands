**Creating a .gitignore file in git bash**

```bash
touch .gitignore
```

**Adding a file into .gitignore**

```bash
echo file/folder >> .gitignore
```



**In case of accidental commit before adding to .gitignore**

1)  Check file if in staging area using command.

List files:
```bash
git ls-files
```

2) Remove from index using command.
```bash
git rm --cached -r folder
```

`-r: To recursively remove a folder`

3) Commit the removal using
```bash
git commit -m ""
```

4) Add file to .gitignore using
```bash
echo file/folder >> .gitignore
```

