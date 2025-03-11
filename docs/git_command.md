
# git command

- [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [git-flow cheatsheet](http://dominhhai.github.io/git-flow-cheatsheet/index.html)

## commands

### get head commit id
```
git rev-parse HEAD
```

### view remote repo
```
git remote -v

git remote set-url origin git@github.com:fanqingsong/vanna-flask.git
git remote set-url --push origin git@github.com:fanqingsong/vanna-flask.git

git remote show origin

git branch -r
```


### local branches
```
git branch

git checkout -b xxx
```


### alias
```
git config --global alias.st status
git config --global alias.ci commit
git config --global alias.co checkout


example:
git config --global alias.unstage 'reset HEAD'
git unstage test.py
git reset HEAD test.py
```

### add tag
```
git push v1.0
```

### push tag
```
git push origin --tags
git push origin tagname
```

### push to origin
```
git push origin master:refs/for/master

git push origin HEAD:refs/drafts/master

git push origin master:refs/heads/master
```

### git push review
```
git remote add review https://xxxx
git config remote.review.pushurl https://xxx
git config remote.review.push 'HEAD:refs/drafts/master'
```

### push head to origin master or dev
```
git push origin master
git push origin dev
```

### drop all your work
```
git reset --hard origin/master

git reset --soft origin/master
```

### git add all but exclude some one file
```
git add -u
git reset -- static/js/dashboard.js
```


### stash all your work
```
git stash
git stash list
```

### pop out your stash 
```
git stash pop
git stash apply xxx
git stash drop xxx
```

### git patch
```
git diff > patch
git diff HEAD HEAD^ > patch
git format-patch HEAD^ 
git format-patch commit_new commit_old

git apply patch
git apply --check patch
```

### remove the HEAD commit
```
git reset --hard HEAD^
git reset --hard HEAD~100
git reset --hard 3628164
```

### remove the HEAD commit softly, all change will be in stage
```
git reset --soft HEAD^
```

### get logs
```
git log --graph --pretty=oneline --abbrev-commit
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

git cherry-pick commit1..commit100
```

### merge one file into this branch from other branches
```
git checkout feature/new1.1 -- usercontroller.php
```

### create new branch
```
git checkout -b mywork origin
```

### create new branch with remote branch
```
git checkout -b dev origin/dev
```

### switch branch
```
git checkout develop
```

### delete branch
```
git branch -d feature-discuss

// 删除本地分支
git branch -d localBranchName

// 删除远程分支
git push origin --delete remoteBranchName
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

git diff readme.txt
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

### delete tag
```
git tag -d v1.0
```

### config
```
git config --global user.email "qsfan@qq.com"
git config --global user.user "fanqingsong"

git config --global credential.helper store

git config --global credential.helper

git config --unset credential.helper

git credential-store clean
```


### update locally
```
git pull origin next

==
git fetch origin master
git merge FETCH_HEAD 
```




