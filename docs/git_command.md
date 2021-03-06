
# git command

## commands

### get head commit id
```
git rev-parse HEAD
```

### add tag
```
git push v1.0
```

### push tag
```
git push origin --tags
```

### push head to origin master drafts
```
git push origin HEAD:refs/drafts/master
```

### push head to origin master
```
git push origin master
```

### drop all your work
```
git reset --hard origin/master
```

### stash all your work
```
git stash
```

### pop out your stash 
```
git stash pop
```

### remove the HEAD commit
```
git reset --hard HEAD^
```

### remove the HEAD commit softly, all change will be in stage
```
git reset --soft HEAD^
```

### get the deleted commits log, it is helpful to restore them if you use git reset --hard wrongly
```
git reflog
```

### set head to the specified commit
```
git reset --hard commit_id
```

### revert the specified commit
```
git revert commit_id
```

### merge commit into this branch from other branches
```
git cherry-pick 00940ac970b9ddab63bff928479668bbfa293aaf
```

### merge one file into this branch from other branches
```
git checkout feature/new1.1 -- usercontroller.php
```

### create new branch
```
git checkout -b mywork origin
```

### switch branch
```
git checkout develop
```

### delete branch
```
git branch -d feature-discuss
```

### rebase current branch on origin branch
```
git rebase origin
```

### merge another branch with this branch, will generate a merge commit on top
```
git merge another_branch
```

### merge another branch with this branch without fast forward
```
git merge --no-ff another_branch
```


### show diff
```
git diff

git diff HEAD HEAD^

git diff HEAD HEAD^ --name-only

git show HEAD --name-only
```

### position who make revision
```
git blame xxx
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






