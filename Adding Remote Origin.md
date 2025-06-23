```bash
git add remote origin 'link_to_repo'
```

#### Pushing changes to github
```shell
git push -u origin main
```

Where -u is to: Set an "upstream" tracking relationship between your local `main` and remote `origin/main`.

So next time we can use `git pull` or `git push` instead of specifying `git push origin main`.