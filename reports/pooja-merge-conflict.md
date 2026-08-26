# Pooja — Merge Conflict Reflection

## 1. What is a merge conflict?

A merge conflict happens when Git cannot automatically combine changes from two branches because both branches modified the same lines or one branch deleted content that the other modified. Git stops the merge and asks a developer to decide the final content.

## 2. Why did our team's conflict happen?

Our scenario involved overlapping edits to the same file. Two teammates and I changed the same section of `scenario-1.md` at the same time. When I attempted to merge their branch into mine, Git could not decide which edits should be kept.

## 3. What did Git show when the conflict occurred?

I ran `git merge origin/feature/teammate-branch` and Git reported a conflict. Running `git status` showed `both modified: scenario-1.md` and that there were unmerged paths. The file contained conflict markers:

```
<<<<<<< HEAD
...my changes...
=======
...their changes...
>>>>>>> origin/feature/teammate-branch
```

## 4. What do the conflict markers mean?

`<<<<<<< HEAD` indicates the version in my current branch. `=======` separates the two versions. `>>>>>>> branch-name` shows the incoming changes from the branch being merged. These markers are temporary helpers for manual resolution.

## 5. How I investigated the conflict

- I ran `git status` to identify which files were unmerged.
- I used `git diff` to inspect differences between the versions.
- I opened `scenario-1.md` in the editor to read both changes and understand intent.

## 6. How I resolved the conflict

I compared both sets of changes and decided which parts from each version should be kept. Instead of choosing one side entirely, I combined useful lines from both changes into a single coherent paragraph, removed the conflict markers, and saved the file.

Then I marked the resolution and completed the merge:

- `git add scenario-1.md`
- `git commit` (which completed the merge commit)
- `git push` to update the remote branch

## 7. What I learned about resolving conflicts safely

- Never accept a side blindly—review both versions first.
- Use `git diff` and an editor to understand intent.
- Run the test suite or a quick smoke check after resolving a conflict to catch regressions.
- If unsure, ask the author of the incoming changes instead of guessing.

## 8. What would I do differently next time?

- Communicate before force-pushing large changes.
- Break large edits into smaller commits to reduce overlapping changes.
- Rebase interactively on top of the latest `main` locally to surface conflicts earlier and in a controlled environment.

## 9. Useful commands (summary)

- `git fetch origin`
- `git merge origin/branch-name` or `git rebase origin/main`
- `git status`
- `git diff` and `git diff --staged`
- `git checkout --ours <file>` / `git checkout --theirs <file>` (use cautiously)
- `git add <file>` then `git commit`

## 10. Final notes

Resolving merge conflicts is a normal part of collaborative development. The important parts are understanding what changed, making an intentional resolution, testing the result, and communicating the outcome to teammates.
