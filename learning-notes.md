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

# Learning Notes
# Git Learning Notes

## 1. git clone

**What it does:**
Copies a GitHub repository to my computer.

**When I use it:**
When I want to start working on an existing project.
Creates a copy of a remote Git repository on your local computer.

**Real-world use:**
I used `git clone` to download my forked GitHub repository to my laptop before starting the assignment.

---

## 2. git status

**What it does:**
Shows which files have changed and whether they are staged.

**When I use it:**
Before every commit to check my work.
Shows the current state of the repository, including modified, staged, and untracked files.

**Real-world use:**
I used `git status` many times to check whether my changes were ready to commit.

---

## 3. git add

**What it does:**
Moves selected changes to the staging area.

**When I use it:**
Before creating a commit.
Moves file changes to the staging area before committing.

**Real-world use:**
I used `git add` after editing my participant profile and documentation files.

---

## 4. git commit

**What it does:**
Saves my staged changes with a message.

**When I use it:**
After finishing a small logical task.
Creates a snapshot of the staged changes with a meaningful message.

**Real-world use:**
I used `git commit` after completing each logical task, such as updating my profile and documentation.

---

## 5. git push

**What it does:**
Uploads my commits to GitHub.

**When I use it:**
After committing my work so others can see it.
Uploads local commits to the remote GitHub repository.

**Real-world use:**
I used `git push` to update my feature branch and keep my Pull Request up to date.
# Learning Notes

Notes on Git commands I used and learned while working through this assignment.

## 1. git clone

**What it does:** Copies a repository from GitHub down onto my own computer, so I have a full local copy to work with — including all its history.

**When I'd use it:** Today, when I forked the workshop repo and needed to actually start editing files, I ran `git clone` to get my fork onto my laptop before I could do anything else.

## 2. git checkout -b

**What it does:** Creates a brand new branch and switches to it in one step, instead of creating a branch and then separately switching to it.

**When I'd use it:** I used this to create `feature/nikita-sarma/profile` so I could make my changes separately from `main`, without risking breaking anything for other people working on the same repo.

## 3. git add

**What it does:** Stages a file, tells Git "I want this specific change included in my next commit." It doesn't save the change permanently yet, it just marks it as ready.

**When I'd use it:** After editing `participants/nikita.md`, I ran `git add participants/nikita.md` to stage just that file before committing, so my commit only contained that one change and nothing else I might have been mid-editing.

## 4. git commit

**What it does:** Takes everything that's staged and saves it as a permanent snapshot in the repo's history, along with a message explaining what changed.

**When I'd use it:** After staging my profile changes, I committed with a clear message like "Add nikita's profile" so anyone looking at the history later understands exactly what that snapshot changed and why.

## 5. git push

**What it does:** Uploads my local commits to the remote repository on GitHub, so the changes exist online and other people (or a Pull Request) can see them.

**When I'd use it:** Once I've made my commits locally, I'll push my branch to my fork on GitHub so I can open a Pull Request from it and nothing shows up on GitHub until I push.
