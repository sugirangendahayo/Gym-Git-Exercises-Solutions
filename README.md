# Gym Git Exercise Solutions

## BUNDLE 1

## BUNDLE 1 - Exercise 1 

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

## BUNDLE 1 - Exercise 2

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

## BUNDLE 2 - Exercise 1

### Create a new branch named 'ft/bundle-2-v2'

```bash
git checkout -b ft/bundle-2-v2
```

### Create a new page named 'services.html'

```bash
touch services.html
```

### Stage the new file for commit

```bash
git add services.html
```

### Check the status to confirm the file is staged

```bash
git status
```

### Commit the changes with a descriptive message

```bash
git commit -m "Add services.html page for Bundle 2"
```

### Push the new branch to the remote repository and set upstream

```bash
git push -u origin ft/bundle-2-v2
```

## BUNDLE 2 - Exercise 2

# Checkout main and pull the latest changes

git checkout main
git pull origin main

# Create a new branch for the service redesign

git checkout -b ft/service-redesign

### Edit services.html (make your redesign changes)

### For example, open services.html in your editor and make changes

### Stage and commit the redesign changes

```bash
git add services.html
git commit -m "Redesign services.html page for Exercise 2"
```

### Push the new branch to the remote repository and set upstream

```bash
git push -u origin ft/service-redesign
```

### Switch back to main to make conflicting changes

```bash
git checkout main
```

### Edited the same lines in services.html (different changes from redesign)

### Stage and commit the conflicting changes on main

```bash
git add services.html
git commit -m "Update services.html on main branch for conflict demo"
git push origin main
```

### Switch back to the feature branch to merge main

```bash
git checkout ft/service-redesign
```

### Merge main into your feature branch to handle conflicts

```bash
git merge main
```

### If conflicts appear, open services.html and resolve them manually

### After resolving conflicts, stage and commit

```bash
git add services.html
git commit -m "Resolve merge conflicts with main in services.html"
```

### Push the updated feature branch

```bash
git push
```

### Now the PR can be merged into main with all changes
