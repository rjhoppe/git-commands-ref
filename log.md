Only show git logs for a particular time period
```
git log --since="yesterday"
git log --since="2 weeks ago"
```

Search commit messages that match a regular expression
EX:
```
git log --grep=mail --author=rick --since=2.weeks
```

Selectively include or exclude specific types of files
EX: (A)dded, (D)eleted, (M)odified, (R)efactored (?)
```
git log --diff-filter=R --stat
```

Use the ~ or ^ to reference previously commits relative to the location of HEAD
EX: The previous commit
```
git log HEAD~1
```
EX: Two previous commits back
```
git log HEAD~2
```
