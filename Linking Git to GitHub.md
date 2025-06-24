
#### Adding the remote repo link
```bash
git remote add origin 'link_to_repo'
```

#### Pushing changes to GitHub
```shell
git push -u origin main
```

Where -u is to: Set an "upstream" tracking relationship between your local `main` and remote `origin/main`.

So next time we can use `git pull` or `git push` instead of specifying `git push origin main`.
