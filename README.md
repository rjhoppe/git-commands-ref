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

Committing repo changes
```
git add .
git status
git commit -a
git push [repo name]
```
Note: 'git status' shows you all active changes made to your current repo
 
Managing remote repos
```
git remote add origin [remote origin]
git remote -v
git remote rm origin
```

Resolve 'fatal: refusing to merge unrelated histories' error
```
git pull origin master --allow-unrelated-histories
```
Then try pushing to remote repo again

