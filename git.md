# git
> git gud

## commit message verbs
* Add ...
* Remove ...
* Update ...
* Refactor ...
* Fix ...

## git commands
```
# fetch and removes local branches with deleted remote branch
git fetch --prune

# if possible; pull without merge commit and fast forward changes
git pull --ff-only

# pull without committing merge commit
git pull --no-commit

# skip git commit hooks >:)
git commit --no-verify

# get root directory absolute path
git rev-parse --show-toplevel

# get staged file(s) name
git diff --staged --named-only HEAD

# Windows-specific
# enter git credentials
git config -global credential.helper wincred
```