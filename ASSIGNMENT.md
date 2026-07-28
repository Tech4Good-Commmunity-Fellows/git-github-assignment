# Workshop Assignment

## Overview

In this workshop, you will contribute to a shared documentation repository by working through a realistic Git and GitHub collaboration flow. Your goal is to make a well-scoped set of documentation updates, review a peer’s work, and learn how to stay in sync with the main branch.

## Tasks

Complete the following steps in order:

1. Clone the repository to your local machine.
2. Create a feature branch using the repository convention: `feature/<your-name>`.
3. Complete your profile in the `participants/` folder.
4. Improve one documentation file inside `docs/`.
5. Complete part of `resources/commands.md`.
6. Make at least three meaningful commits.
7. Push your feature branch to GitHub.
8. Open a pull request using the repository template.
9. Review another participant’s pull request.
10. Pull the latest changes after another pull request is merged.
11. Resolve merge conflicts if they occur.
12. Delete your feature branch after your pull request is merged.

## Suggested Workflow

### 1. Clone the Repository

```bash
git clone <repository-url>
cd git-github-workshop
```

### 2. Create a Feature Branch

```bash
git switch -c feature/<your-name>
```

### 3. Make Your Required Changes

- Complete your participant profile.
- Add useful content or placeholders to one file in `docs/`.
- Fill in part of the command reference in `resources/commands.md`.

### 4. Commit Your Work

Make at least three meaningful commits. Keep each commit focused on one idea.

Example commit sequence:

- `Add participant profile`
- `Improve branching documentation`
- `Start Git command reference`

### 5. Push and Open a Pull Request

```bash
git push -u origin feature/<your-name>
```

Then open a pull request and use the repository template to summarize your work.

### 6. Review a Peer Pull Request

Read one other participant’s pull request and leave a constructive review comment.

### 7. Stay Up to Date

If another pull request is merged before yours, update your branch from the latest main branch and resolve any conflicts.

### 8. Finish Cleanly

After your pull request is merged, delete your feature branch locally and remotely.

## Submission Checklist

- [ ] I cloned the repository.
- [ ] I created a branch named `feature/<your-name>`.
- [ ] I completed my participant profile.
- [ ] I improved one file in `docs/`.
- [ ] I completed part of `resources/commands.md`.
- [ ] I made at least three meaningful commits.
- [ ] I pushed my branch to GitHub.
- [ ] I opened a pull request using the template.
- [ ] I reviewed another participant’s pull request.
- [ ] I pulled the latest changes after another PR was merged.
- [ ] I resolved merge conflicts if needed.
- [ ] I deleted my feature branch after merge.

## Evaluation Rubric

| Criterion | What We Look For | Points |
| --- | --- | --- |
| Branch setup | Correct branch name and clean workflow | 10 |
| Participant profile | Completed with thoughtful, accurate information | 15 |
| Documentation improvement | Clear, useful contribution to a docs file | 20 |
| Command reference contribution | Meaningful completion of the table entries | 15 |
| Commit quality | At least three focused, descriptive commits | 15 |
| Pull request quality | Clear summary and complete template | 10 |
| Peer review | Constructive feedback on another PR | 5 |
| Merge conflict handling | Correct resolution if a conflict occurs | 10 |

## Bonus Challenges

Choose one or more of the following if you finish early:

- Improve a second documentation file in `docs/`.
- Add a helpful example to `resources/glossary.md`.
- Suggest an improvement to the workshop instructions in a pull request comment.
- Add a new common command to `resources/commands.md` and leave its description for later completion.
- Review a second pull request and compare approaches.

## Notes

> TODO: Replace this section with facilitator-specific submission instructions if needed.

> TODO: Explain how grading or verification will be handled in your workshop session.
