# Leela's Merge Conflict Report

## 1. What is a merge conflict?

A merge conflict happens when two branches have different changes in the same part of a file, and Git cannot decide automatically which change should be kept.

In my case, the conflict happened because the same line in `scenarios/scenario-1.md` was changed differently on the two branches.

Git stopped the merge so that we could manually decide what the final version should be.

---

## 2. Why did your team's conflict happen?

Our team was working on:

`scenarios/scenario-1.md`

The original line was:

`The project uses Git for version control.`

Nikita changed this line in her branch.

I also worked on the same part of the file, so the two branches contained different versions of the same line.

Because the changes were overlapping, Git could not automatically combine them.

This created the merge conflict.

The important point is that the conflict happened because both branches changed the same line, not simply because we were working on the same file.

---

## 3. What did Git show you when the conflict occurred?

When I tried to merge the branches, Git reported that there was a conflict in the scenario file.

I first used:

`git status`

This showed me that the repository was in the middle of a merge and that there was a file with unresolved changes.

I then used:

`git diff`

to understand what was different between the two versions.

When I opened the conflicted file, Git showed conflict markers around the changed section.

These markers helped me see which version came from my branch and which version came from the other branch.

---

## 4. What do these markers mean?

Git uses three types of conflict markers:

`<<<<<<< HEAD`

This shows the beginning of the changes from my current branch.

`=======`

This separates my changes from the changes coming from the other branch.

`>>>>>>> branch-name`

This shows the end of the incoming changes.

These markers are only used by Git to show the conflicting parts. They should not remain in the final file after resolving the conflict.

---

## 5. How did you decide what the final version should contain?

I first compared both versions instead of immediately selecting one side.

I checked what I had changed and what Nikita had changed.

Since the conflict was created because both of us modified the same line, I needed to decide which wording should be the final version.

I kept the version that made the most sense for the assignment and removed the conflict markers.

After resolving the conflict, I checked the file again to make sure the final content was readable and that I had not accidentally removed any required information.

I also used `git diff` to review the final changes before completing the merge.

---

## 6. What would have happened if both developers had changed different lines?

If we had changed different lines of the file, Git would most likely have been able to combine both changes automatically.

For example, if I changed the introduction and Nikita changed a different section, the changes would not overlap.

In that situation, there would usually be no merge conflict.

This showed me that two developers can work on the same file without necessarily creating a conflict.

The conflict usually happens when their changes overlap.

---

## 7. Why shouldn't you blindly choose "Accept Current" or "Accept Incoming"?

We should not blindly choose either option because both versions may contain useful changes.

If I choose "Accept Current", I may accidentally remove the other developer's work.

If I choose "Accept Incoming", I may accidentally remove my own changes.

The correct choice depends on what the final version of the file is supposed to contain.

Therefore, I should first understand both changes and then decide whether to keep one version or combine the changes.

---

## 8. What would you do if this happened while working on a real company project?

If this happened in a real company project, I would first investigate the conflict instead of immediately choosing one version.

I would use:

`git status`

to see which files were affected.

Then I would use:

`git diff`

to understand the changes.

I would compare both versions and decide what the correct final result should be.

If I was not sure which change was required, I would discuss it with the other developer or the person responsible for that part of the project.

After resolving the conflict, I would review the final diff and test the changes before completing the merge.

---

## 9. What was the most confusing part of resolving the conflict?

The most confusing part for me was understanding the conflict markers and knowing which changes belonged to which branch.

At first, seeing:

`<<<<<<<`

`=======`

and:

`>>>>>>>`

made the file look confusing.

After checking the branch names and using `git diff`, I understood that Git was simply showing both versions of the same section.

Once I understood which version belonged to my branch and which belonged to Nikita's branch, it became easier to decide what the final content should be.

---

## 10. What do you understand about merge conflicts now that you didn't understand before this exercise?

Before doing this exercise, I understood that merge conflicts could happen, but I did not clearly understand why Git created them or how to investigate them.

Now I understand that a merge conflict happens when Git finds overlapping changes that it cannot safely combine automatically.

I also learned that resolving a conflict is not just about removing the red error or choosing an option in GitHub.

I need to understand both changes first and then decide what the final version should contain.

The main workflow I learned is:

1. Check `git status`.
2. Use `git diff` to inspect the changes.
3. Open the conflicted file.
4. Understand both versions.
5. Decide the correct final content.
6. Remove the conflict markers.
7. Check the final changes again.
8. Run `git status`.
9. Add the resolved file.
10. Commit and push the resolution.

This exercise helped me understand the reason behind merge conflicts instead of only memorising Git commands.

---

## 11. Create Your Own Additional Conflict

After completing the assigned Scenario 1, I created another conflict to understand the process better.

I used separate branches and made changes that affected the same part of a file.

When I tried to merge the branches, Git detected that the changes overlapped and created a conflict.

I investigated it using:

`git status`

and:

`git diff`

I then opened the conflicted file, compared the two versions, and manually decided what the final version should contain.

After removing the conflict markers, I checked the final file and verified that the conflict was completely resolved.

Finally, I staged the file, committed the resolution, and pushed the changes.

This additional conflict helped me understand the process more clearly because I created and resolved the conflict myself.