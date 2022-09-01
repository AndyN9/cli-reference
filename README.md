# cli-reference
Reference sheet for various CLI tools' commands

## git
> git gud

### commit message verbs
* Add ...
* Remove ...
* Update ...
* Refactor ...
* Fix ...

### commands
```
# fetch and removes local branches with deleted remote branch
git fetch --prune

# if possible; pull without merge commit and fast forward changes
git pull --ff-only

# pull without committing merge commit
git pull --no-commit

# pull and ignore the edit commit message
git pull --no-edit

# pull and create a merge commit
git pull --no-ff

# skip git commit hooks >:)
git commit --no-verify

# empty commit; useful to re-run automation
git commit -m 're-run checks' --allow-empty

# get root directory absolute path
git rev-parse --show-toplevel

# get staged file(s) name
git diff --staged --named-only HEAD

# change commit author and email https://www.git-tower.com/learn/git/faq/change-author-name-email
git filter-branch --env-filter '
WRONG_EMAIL="wrong@example.com"
NEW_NAME="New Name Value"
NEW_EMAIL="correct@example.com"

if [ "$GIT_COMMITTER_EMAIL" = "$WRONG_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$NEW_NAME"
    export GIT_COMMITTER_EMAIL="$NEW_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$WRONG_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$NEW_NAME"
    export GIT_AUTHOR_EMAIL="$NEW_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags

# Windows-specific
# enter git credentials
git config -global credential.helper wincred
```

## nvm
> Node.js version manager

### commands
```
# update latest Node.js for system / default
nvm install node --reinstall-packages-from=node

# update lts Node.js
nvm install "lts/*" --reinstall-packages-from="$(nvm current)"
```

## Homebrew
> hmmm coffee

https://devhints.io/homebrew

### commands
```
# update casks and formulate
brew update
brew outdated
brew upgrade
```
