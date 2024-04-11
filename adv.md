See history of all git operations that you have done
```
git reflog
```

Use reflog to reset your client-side logs
```
git reset --hard [commit event ID]
```

Send an empty commit to retrigger any relevant GitHub actions
```
git commit --allow-empty -m "Trigger rebuild" && git push
```

Enable git rerere globally
```
git config --global rerere.enabled true
```

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
