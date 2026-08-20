# Advanced Git Commands

## 1. git stash

**Purpose:** Temporarily shelves changes I haven't committed yet, so I can switch branches or pull updates without losing my in-progress work and without committing something half-finished.

**Syntax:**
git stash
git stash pop
git stash list

**Example:**
git stash
git checkout main
git pull
git checkout feature/nikita-sarma/profile
git stash pop

**When I'd use it:** If I'm in the middle of editing a file and suddenly need to switch to `main` to check something (or pull a teammate's update), I don't want to commit unfinished work just to switch branches. `git stash` saves it aside, and `git stash pop` brings it back once I'm ready to continue.

## 2. git revert

**Purpose:** Creates a brand new commit that undoes the changes from a previous commit, without deleting or rewriting history. This makes it safe to use on branches other people are also working from, like `main`.

**Syntax:**
git revert <commit-hash>

**Example:**
git revert 4c2b316

**When I'd use it:** If a commit that's already been merged into `main` turns out to have a mistake, I can't just delete it without messing up history for everyone else pulling from that branch. `git revert` adds a new commit that cancels it out, keeping the full history intact and visible — which is safer for shared branches than something like `git reset`.

## 3. git reflog

**Purpose:** Shows a log of everywhere `HEAD` has pointed over time — including commits that are no longer part of any branch, like the ones I "deleted" in the Recovery Challenge.

**Syntax:**
git reflog

**Example:**
git reflog
git checkout b2e6e97

**When I'd use it:** In the Recovery Challenge, I deleted the `experiment` branch after committing `temporary.txt`. That commit doesn't disappear immediately — `git reflog` would let me find its hash and recover it if I ever changed my mind, since Git keeps orphaned commits around for a while before garbage-collecting them.