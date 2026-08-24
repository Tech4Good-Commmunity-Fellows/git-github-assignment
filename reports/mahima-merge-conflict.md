# Mahima's Git Merge Conflict Report

## Team 3 — Delete vs Modify

### 1. What is a merge conflict?

A merge conflict happens when Git tries to combine changes from two branches but cannot decide automatically which change should be kept. Git does not know what the developer intended, so it stops the merge and asks the developer to make the decision.

I understood this better during this assignment because I created the conflict myself with my teammate Nandhini. Instead of Git breaking, it was actually asking me to decide what the final version should be.

### 2. Why did my team's conflict happen?

My team was Team 3, which was assigned the Delete vs Modify scenario. I worked with Nandhini.

In my branch, I deleted the `scenario-3.md` file and committed and pushed that change. At the same time, Nandhini had modified the same `scenario-3.md` file in her branch.

Later, I fetched Nandhini's branch and tried to merge it into my branch. Git found that I had deleted the file while Nandhini had modified it. Git could not automatically decide whether the file should remain deleted or whether Nandhini's modified version should be kept, so it created a merge conflict.

### 3. What did Git show me when the conflict occurred?

I first used `git fetch origin` to get information about the latest remote branches. I then checked the remote branches using `git branch -r` and found Nandhini's branch.

I used `git merge origin/feature/nandhini/merge-conflict` to merge her work into my branch.

Git showed me:

`CONFLICT (modify/delete): scenario-3.md deleted in HEAD and modified in origin/feature/nandhini/merge-conflict.`

After that, I ran `git status`. Git showed:

`You have unmerged paths`

and:

`deleted by us: scenario-3.md`

This helped me understand that my branch had deleted the file and Nandhini's branch had modified it.

### 4. What do the conflict markers mean?

The conflict markers show the different versions involved in a conflict.

`<<<<<<< HEAD` shows the changes from my current branch.

`=======` separates the two versions.

`>>>>>>> branch-name` shows the incoming changes from the other branch.

These markers are temporary. They help the developer see the conflicting versions and decide what the final content should be.

### 5. How did we decide what the final version should contain?

I decided to keep Nandhini's modified version of `scenario-3.md`.

I understood that my change was deleting the file, while Nandhini had made useful modifications to the same file. For this exercise, so we decided that the modified file should be kept instead of deleting it.

I used `git checkout --theirs scenario-3.md` to choose the incoming version. After that, I used `git add scenario-3.md` to tell Git that I had resolved the conflict.

I then checked the status and Git showed that all conflicts were fixed but the merge was still in progress. I completed the merge with a commit and pushed the result to GitHub.

### 6. What would have happened if both developers had changed different lines?

If both developers had changed different lines of the same file, Git could often combine the changes automatically.

For example, if I changed the introduction and Nandhini changed the conclusion, Git would usually be able to keep both changes because they do not overlap.

This taught me that changing the same file does not automatically create a conflict. Conflicts usually happen when changes overlap or when one person deletes something that another person changes.

### 7. Why shouldn't I blindly choose "Accept Current" or "Accept Incoming"?

I should not blindly choose one side because I might accidentally remove useful work from another developer.

Before resolving a conflict, I should understand what both developers changed and what the project is supposed to contain.

During my conflict, I first looked at the Git status and the file before deciding what to keep. This helped me make an intentional decision instead of just selecting an option without understanding it.

### 8. What would I do if this happened in a real company project?

If this happened in a real project, I would first check the conflict carefully and understand what both developers were trying to achieve.

If I was not sure which change should be kept, I would talk to the other developer instead of making a random decision. After resolving the conflict, I would inspect the final changes, run the required tests, check the file again, and then commit and push the resolution.

I would also make sure the Pull Request clearly explains the resolution if the conflict was important.

### 9. What was the most confusing part of resolving the conflict?

The most confusing part for me was understanding what Git meant by "deleted by us" and what `ours` and `theirs` meant during a merge.

I also initially had to understand the difference between fetching a remote branch and having a local branch.

### 10. What do I understand about merge conflicts now that I didn't understand before?

Before this exercise, I knew some basic Git commands such as `git add`, `git commit`, `git push`, and `git status`, but I did not fully understand how merge conflicts happened.

Now I understand that a merge conflict is Git asking a developer to make a decision when it cannot safely combine two different changes.

I learned how to fetch another branch, inspect its commits, merge it into my branch, use `git status` to investigate the conflict, understand conflict information, choose a version, stage the resolved file, complete the merge commit, and push the result.

I also learned that `git status` is very useful during a conflict because it tells me what Git expects me to do next.

## My Team 3 Conflict Summary

My conflict happened because I deleted `scenario-3.md` in my branch while Nandhini modified the same file in her branch.

The important commands I used were:

- `git fetch origin` — get information about remote branches.
- `git branch -r` — view remote branches.
- `git log --oneline` — inspect commit history.
- `git merge` — combine another branch with my current branch.
- `git status` — investigate the conflict.
- `git checkout --theirs scenario-3.md` — choose Nandhini's version.
- `git add scenario-3.md` — mark the conflict as resolved.
- `git commit` — complete the merge.
- `git push` — upload the resolved merge to GitHub.

The final merge was completed successfully and my working tree was clean.

## Additional Conflict

As required by the assignment, I will create one additional merge conflict after completing the Team 3 exercise. I will create the conflict intentionally, investigate it using `git status` and `git diff`, understand the conflicting changes, resolve it manually, verify the final file, commit the resolution, and push it to GitHub.

I will document that additional conflict and what I learned from it as part of this assignment.