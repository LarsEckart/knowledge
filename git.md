# Git

## Merge without auto-commit

```
$ git merge my_feature_branch --no-commit --no-ff
```

## Unstage a file

```
$ git rm --cached file_name
```

## Push new local branch to remote

```
$ git push -u origin branch_name
```

## Create new local branch and switch to it

```
$ git checkout -b new_branch_name
```

## How to keep forked projects up to date

```
$ git remote -v
$ git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
$ git fetch upstream
$ git checkout master
$ git merge upstream/master
```

## Execute command in all git folders

[so link](http://stackoverflow.com/questions/3497123/run-git-pull-over-all-subdirectories)

```
find . -type d -depth 1 -exec git --git-dir={}/.git --work-tree=$PWD/{} pull origin master \;
```
