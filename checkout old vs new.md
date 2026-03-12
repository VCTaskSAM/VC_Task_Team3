## Task3 - Git Checkout (Old vs New)

### Old
`git checkout` was used for multiple purposes such as switching branches or viewing old commits.

Example:

git checkout commit_id  
Used to view old commits (detached HEAD state)

git checkout branch-name  
git checkout -b new-branch  

### New
New Git versions introduced clearer commands.

git switch branch-name  
git switch -c new-branch  

git restore file.txt