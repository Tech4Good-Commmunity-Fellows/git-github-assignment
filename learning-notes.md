# Learning Notes

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