# Git stash can be used to store/save uncommitted work from destructive operations

Stash your changes
```
git stash
```

List all of your stash changes
```
git stash list
```

Show the stash contents
```
git stash show stash@{0}
```

Apply the last stash
```
git stash apply
```

Keep untracked files (stash does not do this by default)
** VERY helpful **
```
git stash --include-untracked
```

Keep all files (even ignored ones!)
```
git stash --all
```

Name stashes for easy reference
EX:
```
git stash save "WIP: making progress on foo"
```

Start a new branch from a stash
```
git checkout [name of branch] -- [file name]
```

Remove the last stash and apply changes
```
git stash pop
```

Remove the last stash
```
git stash drop
```

Remove the nth stash
```
git stash drop stash@{n}
```

Remove ALL stashes
```
git stash clear
```
