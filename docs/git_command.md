
# git command

## commands

### get head commit id
```
git rev-parse HEAD
```

### add tag
```
git tag <tagname>
# Git will create a tag at the current revision but will not prompt you for an annotation. It will be tagged without a message (this is a lightweight tag).

git tag -a <tagname>
# Git will prompt you for an annotation unless you have also used the -m flag to provide a message.

git tag -a -m <msg> <tagname>
# Git will tag the commit and annotate it with the provided message.

git tag -m <msg> <tagname>
# Git will behave as if you passed the -a flag for annotation and use the provided message.
```

### push tag
```
git push origin --tags
```





