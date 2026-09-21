# Git Crew Sync Workflow

## 1. What did the rejected push message say, and why?

The rejected push message said that the remote contains work that I do not have locally. This happened because another clone pushed a newer commit to the same branch before I tried to push my changes. My local branch was behind the remote branch, so Git rejected the push to prevent the remote changes from being overwritten.

## 2. What is the difference between the merge in Task 3 and the rebase in Task 4?

In Task 3, I used a **merge** to combine the changes from Clone A and Clone B. Git created a merge commit after I manually resolved the conflict.

In Task 4, I used a **rebase** instead of a merge. Git moved my Clone B commit on top of the newer changes from the remote branch. After resolving the conflict, the history became more linear without creating another merge commit.

## 3. What habit would have avoided both rejected pushes?

A habit that could have avoided both rejected pushes is to **pull or fetch the latest changes before starting work and before pushing**. This helps make sure the local branch is up to date with the remote branch.

## 4. Which approach would you default to on a shared team branch and why?

I would default to **merge** on a shared team branch because it preserves the actual history of how different branches were combined. It is also easier to understand when multiple people are working on the same branch. For my own feature branches, I would use rebase when I want to keep the history more linear before merging it into the shared branch.