\# Learning Notes: Git Commands



1\. `git status`

Shows which files are modified, staged, or untracked in your working directory.

&#x20;

Before making a commit, running `git status` to confirm which files I actually changed and whether I accidentally edited something I didn’t mean to.



2\. `git add` 

Moves changes from the working directory into the staging area, preparing them to be committed.

&#x20; 

When I finish a logical piece of work (like adding my profile), I run `git add participants.md` to stage just that file instead of everything.



3\. `git commit`

Creates a new snapshot (commit) of the staged changes with a message describing what changed.



After staging my profile changes, I run `git commit -m "Add participant profile"` so the history clearly shows what this commit is about.



4\. `git pull`  

Fetches changes from a remote branch and merges them into your current branch.

&#x20; 

Before starting work each day, I run `git pull upstream main` on my local `main` branch to make sure I’m starting from the latest code.



5\. `git push` 

Uploads your local commits to a remote repository (usually your fork).

&#x20;

After committing my changes on a feature branch, I run `git push -u origin feature/your-name/profile` so I can open a pull request from GitHub.

