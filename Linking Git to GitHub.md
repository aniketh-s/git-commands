
#### Adding the remote repo link
```bash
git remote add origin 'link_to_repo'
```

#### Verify remote origin by
```bash
git remote -v
```

#### Pushing changes to GitHub
```shell
git push -u origin main
```

Where -u is to: Set an "upstream" tracking relationship between your local `main` and remote `origin/main`.

So next time we can use `git pull` or `git push` instead of specifying `git push origin main`.

#### Setting an upstream(tracking) relationship

```bash
git branch --set-upstream-to=origin/<branch_name> <local_repo_branch>
```

**If already in the branch**

```bash
git branch --set-upstream-to=origin/<branch_name>
```
