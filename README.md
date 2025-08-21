# Gym Git Exercise Solutions
# Exercise 1 - Gym Git Exercises

# Initialize repo
mkdir gym-git-exercises
cd gym-git-exercises
git init
touch index.html index.js

# Rename branches
git branch -m master main
git branch -m main master
git branch -m master main

# Stage & commit
git add .
git commit -m "Initial commit"

# Create dev branch and test branch
git branch dev
git checkout dev
git branch test
git checkout dev
git branch -d test
