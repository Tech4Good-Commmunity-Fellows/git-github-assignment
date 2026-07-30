# Git Recovery Challenge

## Steps Performed

1. Created a branch named `experiment`
2. Created `temporary.txt`
3. Committed the file
4. Reverted the commit using `git revert`

## Commands Used

```bash
git checkout -b experiment
touch temporary.txt
git add temporary.txt
git commit -m "Add temporary file"
git revert <commit-id>