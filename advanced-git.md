# Advanced Git Commands

## git stash

### Purpose
Temporarily saves uncommitted changes without creating a commit.

### Syntax
git stash

### Example
git stash

### When You Would Use It
When you need to switch branches but your current work is not ready to commit.

---

## git revert

### Purpose
Creates a new commit that safely undoes a previous commit.

### Syntax
git revert <commit-id>

### Example
git revert a1b2c3d

### When You Would Use It
When a commit has introduced a mistake and you want to undo it without deleting Git history.

---

## git reflog

### Purpose
Shows a record of all recent HEAD and branch movements.

### Syntax
git reflog

### Example
git reflog

### When You Would Use It
When you need to recover a lost commit or find a previous repository state.