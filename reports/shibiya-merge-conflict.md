# Shibiya - Merge Conflict Report

## 1. What is a merge conflict?

A merge conflict happens when Git cannot automatically combine changes from two branches. This usually happens when two developers change the same or overlapping parts of a file.

## 2. Why did your team's conflict happen?

Our team was assigned Team 2. We worked on the same file, `scenarios/scenario-2.md`, but we changed different sections of the file. I modified the Introduction section while my teammate modified a different section. Because our changes did not overlap, Git was able to combine the changes automatically. Therefore, our assigned scenario did not produce a merge conflict.

## 3. What did Git show you when the conflict occurred?

In our Team 2 scenario, Git did not show a merge conflict because the changes were made in different sections of the file. Git automatically combined the changes during the merge.

## 4. What do these markers mean?

`<<<<<<<` marks the beginning of the current branch's changes.

`=======` separates the current branch's changes from the incoming branch's changes.

`>>>>>>>` marks the end of the incoming branch's changes.

These markers appear when Git cannot automatically decide which changes should be kept.

## 5. How did you decide what the final version should contain?

Since the two developers changed different sections, both changes were useful and could be kept. Git automatically combined the changes, so there was no need to remove either developer's work.

## 6. What would have happened if both developers had changed different lines?

If both developers changed different lines or sections, Git would usually combine the changes automatically without creating a conflict. This is what happened in our Team 2 scenario because I modified the Introduction while my teammate modified a different section.

## 7. Why shouldn't you blindly choose "Accept Current" or "Accept Incoming"?

We should not blindly choose either option because we may accidentally remove useful changes made by the other developer. We should first understand both changes and decide what the final version should contain.

## 8. What would you do if this happened while working on a real company project?

I would first use `git status` and `git diff` to understand the conflict. I would compare both changes, discuss with the other developer if necessary, resolve the conflict carefully, test the final result, and then commit the resolution.

## 9. What was the most confusing part of resolving the conflict?

The most confusing part was understanding how Git identifies the changes from the current branch and the incoming branch. This exercise helped me understand how Git represents different changes during a merge.

## 10. What do you understand about merge conflicts now that you didn't understand before this exercise?

Before this exercise, I thought that changing the same file would automatically create a merge conflict. Now I understand that Git can automatically combine changes when developers modify different sections or lines. A conflict usually happens when changes overlap and Git cannot determine which version should be used.

## Additional Conflict I Created

For additional practice, I created two branches that modified the same line of a file in different ways. This created a real merge conflict.

I investigated the conflict using `git status` and `git diff`. I examined the conflict markers in the file and compared the changes from both branches. I then manually combined the useful changes, removed all conflict markers, verified the final file, and completed the merge.

This additional exercise helped me understand how a real merge conflict occurs and how to resolve it manually.

## Part 10 — Self-Created Merge Conflict

For additional practice, I created a separate merge conflict using `scenarios/my-conflict.md`.

First, I created the branch `feature/shibiya/conflict-a` and changed the line:

> Git helps developers collaborate.

to:

> Git helps developers collaborate effectively.

I committed this change.

Next, I returned to `feature/shibiya/merge-conflict` and created another branch called `feature/shibiya/conflict-b`. On this branch, I changed the same line to:

> Git helps developers collaborateacroos teams.

I committed this change separately.

I then merged `feature/shibiya/conflict-a` into my `feature/shibiya/merge-conflict` branch. After that, I tried to merge `feature/shibiya/conflict-b`.

Git reported:

`CONFLICT (content): Merge conflict in scenarios/my-conflict.md`

I used `git status` and `git diff` to investigate the conflict. The file contained the conflict markers `<<<<<<<`, `=======`, and `>>>>>>>`, showing the two different versions.

I manually resolved the conflict by combining the useful meaning from both changes and correcting the text to:

> Git helps developers collaborate effectively across teams.

I removed all conflict markers and used `git add` to mark the conflict as resolved. I then verified the staged changes using `git diff --cached`.

Finally, I completed the merge with:

`git commit -m "Resolve self-created merge conflict"`

The merge was successfully completed, and `git status` showed:

`nothing to commit, working tree clean`

This exercise helped me understand that a merge conflict occurs when Git cannot automatically decide between overlapping changes, and that the developer must intentionally decide what the final content should be.