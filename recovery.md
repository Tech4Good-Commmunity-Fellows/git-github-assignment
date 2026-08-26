# Git Recovery Challenge

## Steps Performed

1. Created a branch named `experiment`
2. Created `temporary.txt`
3. Committed the file
4. Reverted the commit using `git revert`
\# Recovery Challenge



\## Commands used



git checkout main

git checkout -b experiment

echo "temp" > temporary.txt

git add temporary.txt

git commit -m "Add temporary file for recovery test"

git checkout main

git branch -D experiment



\## What I did



I created a new branch called `experiment` off `main`, added a file called `temporary.txt`, and committed it. Then I switched back to `main` and force deleted the `experiment` branch using `-D`, since it hadn't been merged and a normal `git branch -d` would have refused to delete it.



\## Why this approach is safe



Deleting a branch in Git doesn't actually delete the commits on it — it just removes the pointer (the branch name) that was pointing to those commits. The commit I made on `experiment` still technically exists in Git's internal object database, and I could find it again using `git reflog` if I ever needed to recover it, at least until Git eventually runs garbage collection and cleans up truly unreachable commits.



Because `experiment` was never merged into `main`, deleting it also had zero effect on `main`'s history or on anyone else working from the shared repository. This is different from something like `git reset --hard` on a shared branch, which can rewrite history other people are relying on. Here, the "damage" was fully contained to a throwaway branch only I knew about, so deleting it was a clean, low-risk way to fully discard the experiment without touching real repository history.

# Recovery Challenge

## Commands Used

```bash
git checkout -b experiment
touch temporary.txt
git add temporary.txt
git commit -m "Add temporary file"
git revert <commit-id>
git revert HEAD
Commands used:
git checkout -b experiment
echo "temp" > temporary.txt
git add temporary.txt
git commit -m "Add temporary file for recovery test"
git checkout main
git branch -D experiment

Why this is safe: the commit (b2e6e97) still exists in Git's internal history and is recoverable via `git reflog` until garbage collected — deleting the branch just removes the pointer to it, not the commit itself. Since `experiment` was never merged into `main`, deleting the branch doesn't affect `main`'s history at all. This is a safe way to fully discard experimental work without touching the shared branch.
