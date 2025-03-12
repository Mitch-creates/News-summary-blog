## Procedure for working on this project, since there's an automation script creating blogposts. Doing automatic push, pull, merge

git checkout master
git pull origin master  # Get the latest live version
git checkout -b feature/manual-edits  # Create a new branch for manual changes
# Make your changes...
git add .
git commit -m "Manually updated blog content"
git push origin feature/manual-edits  # Push changes to remote

## Do this everytime you start working on it to ensure the automation script's changes are loaded
git checkout master
git pull origin master
git merge develop  # Merge automation updates
git push origin master