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

## BUNDLE 3

## BUNDLE 3 - Exercise 1

### Ensure we're on the main branch and up-to-date

```bash
git checkout main
git pull origin main
```

### Create and checkout ft/team-page branch

```bash
git checkout -b ft/team-page
```

### Create team.html with sample content

```bash
touch team.html
```

### Stage and commit changes

```bash
git add team.html
git commit -m "Add team.html with initial content"
```

### Push ft/team-page to GitHub

```bash
git push origin ft/team-page
```

### Note: Create a Pull Request for ft/team-page on GitHub manually

### Checkout main branch

```bash
git checkout main
```

### Create and checkout ft/contact-page branch

```bash
git checkout -b ft/contact-page
```

### Go back to ft/team-page to get the last commit hash

```bash
git checkout ft/team-page
```

### View git log to copy the last commit hash (for cherry-pick later)

```bash
git log -1 --pretty=%H
```

### Output example: 6d842d406... (copy this hash manually for later use)

### Go back to ft/contact-page

```bash
git checkout ft/contact-page
```

### Cherry-pick the last commit from ft/team-page (replace abc123 with actual hash)

```bash
git cherry-pick abc123
```

### Create contact.html with sample content

```bash
touch contact.html
```

### Stage and commit new contact page changes

```bash
git add contact.html
git commit -m "Add contact.html with initial content"
```

### Push ft/contact-page to GitHub

```bash
git push origin ft/contact-page
```

### Note: Create a Pull Request for ft/contact-page on GitHub manually

### Create and checkout ft/faq-page branch from ft/contact-page

```bash
git checkout -b ft/faq-page
```

### Create faq.html with sample content

```bash
touch faq.html
```

### Stage and commit faq.html changes

```bash
git add faq.html
git commit -m "Add faq.html with initial content"
```

### Push ft/faq-page to GitHub

```bash
git push origin ft/faq-page
```

### Note: Create a Pull Request for ft/faq-page on GitHub manually

### Go back to ft/team-page for revert

```bash
git checkout ft/team-page
```

### Revert the last commit on ft/team-page (replace abc123 with the same hash used earlier)

```bash
git revert 6d842d406ca55138954be759eb4defdb2c8b5521
```

### Push the revert commit to GitHub

```bash
git push origin ft/team-page
```

### Note: Create a Pull Request for the revert on ft/team-page on GitHub manually

## BUNDLE 4 - Exercise 1: Push to Two Remotes

### Checkout main branch

```bash
git checkout main
```

### Pull latest changes from origin

```bash
git pull origin main
```

### Add new GitHub repo as second remote named git-copy

```bash
git remote add git-copy https://github.com/sugirangendahayo/gym-git-exercises-copy.git

```

### Update home.html with new changes

echo "<p>Updated home page content</p>" >> home.html

### Stage the new changes

```bash
git add home.html
```

### Commit the changes with a descriptive message

```bash
git commit -m "Update home.html with new content"
```

### Push changes to origin remote

```bash
git push origin main
```

### Push changes to git-copy remote

```bash
git push git-copy main
```

## BUNDLE 4 - Exercise 2: Footer and Squashing Commits

### Checkout a new branch named 'ft/footer'

```bash
git checkout -b ft/footer
```

### Add changes to footer in a file (for example in index.html)

```bash
echo "<footer>First footer update</footer>" >> index.html
```

### Stage the new changes

```bash
git add index.html
```

### Commit the changes with a descriptive message

```bash
git commit -m "Add initial footer content to index.html"
```

### Add more changes to footer in the same file

```bash
echo "<footer>Updated footer with additional content</footer>" >> index.html
```

### Stage the additional changes

```bash
git add index.html
```

### Commit the additional changes with a descriptive message

```bash
git commit -m "Update footer content in index.html"
```

### Push the new branch to the remote repository

```bash
git push -u origin ft/footer
```

### Checkout main branch

```bash
git checkout main
```

### Create a new branch named 'ft/squashing'

```bash
git checkout -b ft/squashing
```

### Squash merge changes from ft/footer branch

```bash
git merge --squash ft/footer
```

### Stage the squashed changes

```bash
git add .
```

### Commit the squashed changes with a new message

```bash
git commit -m "footer changes squashing"
```

### Push the new branch to the remote repository

```bash
git push -u origin ft/squashing
```

## BUNDLE 5

## BUNDLE 5 - Exercise 1: Enable GitHub Pages

### Ensure on main branch

```bash
git checkout main
```

### Pull latest changes from origin

```bash
git pull origin main
```

### Note: Enable GitHub Pages manually in the GitHub UI

### Go to gym-git-exercises repository on GitHub

### Verify the GitHub Pages site is live

### Visit https://sugirangendahayo.github.io/gym-git-exercises

### Check if the site is publicly visible by opening the link in an incognito browser

## BUNDLE 5 - Exercise 2: Fork and Update Git Cafe Exercise

### Fork the repository manually on GitHub

### Go to https://github.com/TheGymRwanda/git-cafe-exercise

### Click "Fork", tick "Copy the main branch only", and create fork

### Clone the forked repository to a new folder

```bash
git clone https://github.com/<your-username>/git-cafe-exercise.git ~/desktop/gym-apps/git-cafe-exercise
```

### Navigate to the cloned repository

cd ~/desktop/gym-apps/git-cafe-exercise

### Ensure on main branch

```bash
git checkout main
```

### Edit index.html to change the text

### Stage the changes

```bash
git add index.html
```

### Commit the changes with a descriptive message

```bash
git commit -m "Update welcome text in index.html"
```

### Push the changes to your forked repository

```bash
git push origin main
```

### Create a Pull Request to the original repository manually

### Go to the forked repository on GitHub

### Click "Contribute" and "Open pull request"

### Add description

### Create PR to TheGymRwanda/git-cafe-exercise
