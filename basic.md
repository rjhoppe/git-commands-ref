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

Create a new repo branch and then pull it into your local repo
```
git remote add [new branch name] [git repo name/ url]
git fetch [new branch name]
```

Create a new branch and switch to it
```
git checkout -b [branch name]
```

List all the branches of a repo
```
git branch -r
git branch -r -v
```

Pull new branches into local
```
git fetch
```

Clean out outdated branches
```
git fetch --prune 
```
OR to globally ensure that Git always automatically prunes
```
git config --global fetch.prune true
```

Committing repo changes
```
git add .
git status
git commit -a
git push [repo name]
```
Note: 'git status' shows you all active changes made to your current repo

After initial commit use this to add changes from previous staged files:
```
git add -u
```

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


Search the repo for mentions of a particular string
Use the second option to search for mentions of a particular string in filenames
```
git grep [file name]
git grep -l 
```

This command shows the difference introduced by a particular commit or blob:
This will default to showing the last commit if another commit is not specified
```
git show
git show -m HEAD
```
If searching for a specific commit id:
```
git log
git show [commit id]
```
