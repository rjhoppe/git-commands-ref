# Commands for the Git tag functionality

List all the tags in a repo
```
git tag
```

List all the tags and what commit they are pointing to
** VERY Helpful **
```
git show-ref --tags
```

List all the tags pointing at a commit
```
git tag --points-at [commit]
```

Looking at the tag or tagged contents
```
git show [tag-name]
```

Reverse look up a tag by referencing the SHA of a commit
```
git tag --points-at [first few digits of commit SHA]
```

Create an annotated tag with meta data
** VERY Helpful **
```
git tag -a [annotated tag name] -m ['tag message']
```
