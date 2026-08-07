## Advanced Git Commands

### 6. `git branch`

Lists, creates, or deletes branches.

**Real-world use case:**

Before starting a new feature, I create a separate branch using `git branch feature/login` so my work doesn't affect the main branch.

---

### 7. `git checkout`

Switches between branches.

**Real-world use case:**

When I need to continue working on another feature, I use `git checkout feature/profile` to switch to that branch.

---

### 8. `git checkout -b`

Creates a new branch and switches to it in one command.

**Real-world use case:**

Instead of creating and switching separately, I run `git checkout -b feature/dashboard` to start working on a new feature immediately.

---

### 9. `git fetch`

Downloads the latest changes from the remote repository without merging them.

**Real-world use case:**

Before updating my branch, I use `git fetch upstream` to check if there are any new changes available.

---

### 10. `git diff`

Shows the differences between files or commits.

**Real-world use case:**

Before committing, I run `git diff` to review exactly what changes I have made.

---

### 11. `git log`

Displays the commit history.

**Real-world use case:**

When I need to understand previous changes or find an older commit, I use `git log`.

---

### 12. `git stash`

Temporarily saves uncommitted changes.

**Real-world use case:**

If I need to switch branches urgently without committing unfinished work, I run `git stash`.

---

### 13. `git stash pop`

Restores the most recently stashed changes.

**Real-world use case:**

After returning to my feature branch, I use `git stash pop` to continue my unfinished work.

---

### 14. `git merge`

Combines changes from one branch into another.

**Real-world use case:**

After completing a feature, I merge it into the `main` branch using `git merge feature/login`.

---

### 15. `git rebase`

Moves your commits on top of another branch to keep the commit history clean.

**Real-world use case:**

Before opening a Pull Request, I run `git rebase main` to include the latest changes from the main branch.

---

### 16. `git cherry-pick`

Applies a specific commit from another branch.

**Real-world use case:**

When I need only one bug fix from another branch, I use `git cherry-pick <commit-hash>` instead of merging the entire branch.

---

### 17. `git revert`

Creates a new commit that reverses an earlier commit.

**Real-world use case:**

If a commit introduces a bug after it has been shared, I use `git revert` to safely undo it without rewriting history.

---

### 18. `git reset`

Moves the current branch back to a previous commit.

**Real-world use case:**

If I accidentally commit the wrong files, I can use `git reset --soft HEAD~1` to undo the commit while keeping my changes.

---

### 19. `git remote -v`

Displays the configured remote repositories.

**Real-world use case:**

When working with both a fork and the original repository, I use `git remote -v` to verify the `origin` and `upstream` remotes.

---

### 20. `git reflog`

Shows the history of where `HEAD` has pointed.

**Real-world use case:**

If I accidentally delete a branch or reset my commits, I use `git reflog` to recover the lost commit.