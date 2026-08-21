# Recovery Challenge

## Commands Used

```bash
git checkout -b experiment
touch temporary.txt
git add temporary.txt
git commit -m "Add temporary file"
git revert HEAD
Commands used:
git checkout -b experiment
echo "temp" > temporary.txt
git add temporary.txt
git commit -m "Add temporary file for recovery test"
git checkout main
git branch -D experiment

Why this is safe: the commit (b2e6e97) still exists in Git's internal history and is recoverable via `git reflog` until garbage collected — deleting the branch just removes the pointer to it, not the commit itself. Since `experiment` was never merged into `main`, deleting the branch doesn't affect `main`'s history at all. This is a safe way to fully discard experimental work without touching the shared branch.
