# Nandhini - Merge Conflict Reflection

## 1. What is a merge conflict?

A merge conflict happens when Git tries to combine changes from two branches but cannot automatically decide which changes should be kept. The conflict usually happens when both branches make overlapping changes to the same part of a file. Git then asks the developer to manually decide what the final version should contain.

## 2. Why did your team's conflict happen?

Our team was Team 3, Mahima and Nandhini. Our assigned scenario was Delete vs Modify. My branch deleted a section from `scenario-3.md`, while Mahima's branch modified content in the same section. Because both branches made changes to the same part of the file, Git could not automatically determine whether the section should be deleted or kept with Mahima's modifications. This caused the merge conflict.

## 3. What did Git show you when the conflict occurred?

When I tried to merge Mahima's branch into my branch using `git merge origin/feature-mahima`, Git reported a content conflict in `scenario-3.md`. Git showed that the automatic merge failed and that the conflict needed to be fixed manually. When I ran `git status`, it showed that there were unmerged paths and that `scenario-3.md` was both modified. I then used `git diff` to inspect the conflicting changes.

## 4. What do these markers mean?

The `<<<<<<< HEAD` marker shows the changes from my current branch.

The `=======` marker separates my changes from the changes coming from the other branch.

The `>>>>>>> origin/feature-mahima` marker shows the changes coming from Mahima's branch.

These markers help the developer understand which parts of the file came from each branch.

## 5. How did you decide what the final version should contain?

I compared the changes from both branches and checked what each developer had changed. I then decided which content should remain in the final version and removed the conflict markers. After resolving the conflict, I used `git add` to mark the file as resolved and committed the resolution. I also checked the repository status to make sure the working tree was clean.

## 6. What would have happened if both developers had changed different lines?

If both developers had changed different lines or different non-overlapping sections of the same file, Git could usually combine the changes automatically. In that situation, a merge conflict would normally not occur because Git can determine where each change belongs.

## 7. Why shouldn't you blindly choose "Accept Current" or "Accept Incoming"?

We should not blindly choose "Accept Current" or "Accept Incoming" because either choice could accidentally remove useful changes made by another developer. We should first compare both versions, understand why the changes were made, and decide what the correct final version should contain. Sometimes the best solution is to combine parts of both changes instead of accepting only one version.

## 8. What would you do if this happened while working on a real company project?

If this happened in a real company project, I would first check `git status` and use `git diff` to understand the conflict. I would carefully compare both versions and determine what the intended final result should be. If I was unsure about the requirements, I would discuss the changes with the other developer or team member before resolving the conflict. After resolving it, I would verify the final file, test the changes, commit the resolution, and push the branch for review.

## 9. What was the most confusing part of resolving the conflict?

The most confusing part was understanding the conflict markers and identifying which content belonged to my branch and which content came from Mahima's branch. At first, the `<<<<<<<`, `=======`, and `>>>>>>>` markers were confusing. After using `git diff` and comparing both versions, I understood how Git displayed the conflicting changes.

## 10. What do you understand about merge conflicts now that you didn't understand before this exercise?

Before this exercise, I did not fully understand why merge conflicts happened or how Git showed the conflicting changes. Now I understand that a merge conflict is not simply Git breaking. It means Git found overlapping changes and needs a developer to make a decision. I learned how to use `git status` and `git diff` to investigate a conflict, how to understand conflict markers, how to manually resolve the conflict, and how to complete the merge after verifying the final result.
