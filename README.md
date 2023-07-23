# git-commands-ref
List of my commonly used Git commands


Create a new repo on the command line
```
echo "# git-init" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:rjhoppe/git-init.git
git push -u origin main
```

Push from an existing repo
```
git remote add origin git@github.com:rjhoppe/git-init.git
git branch -M main
git push -u origin main
```

