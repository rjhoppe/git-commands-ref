**WARNING: DESTRUCTIVE OPERATION**  
This will replace the working area copy with the version from the current staging area
```
git checkout --file
```
Be very careful with this command.  
If you need to run this, be sure to stash any commits that are at risk

Three different options for "git reset"
Option 1: Move HEAD, previous files can be considered a dangling commit
```
git reset --soft HEAD~
```

Option 2: Move HEAD, Copy files to staging area
```
git reset HEAD~
```
OR
```
git reset --mixed HEAD~
```

Option 3: (BE CAREFUL) - Move HEAD, Copy files to staging and working area
```
git reset --hard HEAD~
```

Undo a "git reset" operation
```
git reset ORIG_HEAD
```
