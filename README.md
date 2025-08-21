# Gym Git Exercise Solutions
## BUNDLE 1
## Exercise 1 - Gym Git Exercises

### Initialize repo
```bash
mkdir gym-git-exercises
cd gym-git-exercises
git init
touch index.html index.js
```
### Rename branches
```bash
git branch -m master main
git branch -m main master
git branch -m master main
```
### Stage & commit
```bash
git add .
git commit -m "Initial commit"
```
### Create dev branch and test branch
```bash
git branch dev
git checkout dev
git branch test
git checkout dev
git branch -d test
```


## Exercise 2

### Create and modify home.html, then stash changes:
```bash
touch home.html
git add home.html
git stash push -m "Home page changes"
```

### Create and modify about.html, then stash changes:
```bash
touch about.html
git add about.html
git stash push -m "About page changes"
```
### Create and modify home.html, then stash changes:
```bash
touch team.html
git add team.html
git stash push -m "Team page changes"
```
### Restore about.html changes using stash pop:
```bash
git stash list
git stash pop stash@{1}  # restore about.html
```
### Restore home.html changes using stash index:
```bash
git stash pop stash@{1}  # restore home.html
```
### Commit current changes:
```bash
git add .
git commit -m "Exercise 2: Restored and committed home and about pages"
git push
```
### Restore team.html changes using stash index:
```bash
git stash pop stash@{0}  # restore team.html
```
### Reset the current changes (remove team.html):
```bash
git reset --hard HEAD
```

## BUNDLE 2
## Exercise 1
# Create a new branch named 'ft/bundle-2-v2'
git checkout -b ft/bundle-2-v2

# Create a new page named 'services.html'
touch services.html

# Stage the new file for commit
git add services.html

# Check the status to confirm the file is staged
git status

# Commit the changes with a descriptive message
git commit -m "Add services.html page for Bundle 2"

# Push the new branch to the remote repository and set upstream
git push -u origin ft/bundle-2-v2

