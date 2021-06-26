### Git CLI
```
git version
git init

git clone https://github.com/gdmoney/Docker.git

git show
git status

git fetch
git pull
git commit -am blahblahblah
git push

git add FILENAME

// discard changes in working directory
git restore FILENAME

// undo the change made in the last commit
git revert HEAD
git push

// configure and store GitHub credentials in Git
git config --global user.name gdmoney
git config --global user.email george.davitiani@gmail.com
git config --global credential.helper store

// or cache GitHub credentials in Git
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout=28800'

// change local repo name after changing it on GH
git remove -v
git remote set-url origin https://github.com/gdmoney/NEW-NAME
git remote -v
git pull

// delete a file with sensitive data from all commits
git filter-branch --force --index-filter \
  "git rm --cached --ignore-unmatch PATH_TO_FILE_TO_DELETE" \
  --prune-empty --tag-name-filter cat -- --all
git push origin --force --all
```

### GitHub CLI
```
gh auth login

gh repo clone gdmoney/Docker

gh config set git_protocol SSH or HTTPS
gh config get git_protocol

gh workflow run WORKFLOW_NAME.yml

gh run list --workflow=WORKFLOW_NAME.yml
gh run view
gh run watch
```
